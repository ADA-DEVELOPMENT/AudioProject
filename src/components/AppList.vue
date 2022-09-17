<template>
    <section class="list">
        <div class="container">
            <div class="list__inner">
                <ul class="list__items">
                    <app-item 
                        @audioAction="audioAction"
                        v-for="item, id of audioList" 
                        :key="item.id" 
                        :item="item"
                        :id="id"
                        :audioPlayId = "audioPlayId"
                    ></app-item>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
import AppItem from './AppItem.vue'

export default {
    components: {
        AppItem,
    },
    data() {
        return {
            audioList: [
                {
                    id: 1,
                    title: 'Title 1',
                    src: 'https://cdn.pixabay.com/download/audio/2022/08/31/audio_419263fc12.mp3?filename=leonell-cassio-the-blackest-bouquet-118766.mp3',
                },
                {
                    id: 2,
                    title: 'Title 2',
                    src: 'https://cdn.pixabay.com/download/audio/2022/08/31/audio_419263fc12.mp3?filename=leonell-cassio-the-blackest-bouquet-118766.mp3',
                },
            ],
            audioPlayId: null,
        }
    },
    methods: {
        audioAction(id){
            this.audioPlayId = id
        }
    },
}
</script>

<style>

</style>