<template>
    <main class="main">
        <app-list></app-list>
    </main>
</template>

<script>
import AppList from './components/AppList.vue'


export default {
    name: 'App',
    components: {
        AppList,
    }
}
</script>

<style>
    /* Basic style */
    * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
    }

    body {
        color: rgba(0, 0, 0, 0.9);
        font-family: Arial, sans-serif;
        line-height: 150%;
    }

    button {
        cursor: pointer;
        background: none;
        border: none;
        border-radius: none;
        font-size: inherit;
    }

    ol, ul {
        list-style: none;
    }

    li {
        margin-bottom: 20px;
    }

    li:last-child {
        margin-bottom: 0;
    }

    section {
        padding: 30px 0;
    }

    .container {
        max-width: 900px;
        margin: 0 auto;
        padding: 0 20px;
    }
</style>
