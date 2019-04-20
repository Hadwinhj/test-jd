<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/test-pic.jpg" style="width: 100%;display: block;">
        <!--<HelloWorld msg="通话记录"/>-->
        <contact-list title="通话记录"/>
    </div>
</template>

<script>
    import ContactList from './components/contact_list.vue'

    export default {
        name: 'app',
        components: {
            // HelloWorld,
            ContactList
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
