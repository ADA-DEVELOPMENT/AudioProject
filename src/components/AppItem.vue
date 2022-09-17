<template>
    <li class="list__item">
        <h4>{{item.title}}</h4>
        <audio ref="audioNode" :src="item.src" controls></audio>
        <button @click="audioAction" class="list__button">
            {{audioPlayId === id ? 'Pause' : 'Play'}}
        </button>
    </li>
</template>

<script>
export default {
    props: {
        item: Object,
        id: Number,
        audioPlayId: Number,
    },
    methods: {
        audioAction(){
            let id = this.id

            if (this.audioPlayId !== this.id){
                this.audioPauseAll()
                this.$refs.audioNode.play()
            } else {
                this.$refs.audioNode.pause()
                id = null
            }

            this.$emit('audioAction', id)
        },
        audioPauseAll(){
            document.querySelectorAll('audio').forEach(audio => {
                audio.pause()
            })
        }
    }
}
</script>

<style>

</style>