<template>
    <div id="app">
        <Entries :entries="data"/>
    </div>
</template>

<script>
    import Entries from './components/Entries.vue'

    export default {
        name: 'App',
        components: {
            Entries
        },
        data: function () {
            return {
                data: [
                    {
                        id: 2,
                        title: "My entry #2",
                        date: "2020-12-31 14:15:16",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book."
                    },
                    {
                        id: 4,
                        title: "My entry #4",
                        date: "2021-01-01 01:10:07",
                        image: "https://picsum.photos/id/1018/200/150",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book."
                    },
                    {
                        id: 3,
                        title: "My entry #3",
                        date: "2020-12-31 20:18:00",
                        image: "https://picsum.photos/id/1016/200/150",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book."
                    },
                    {
                        id: 1,
                        title: "My entry #1",
                        date: "2020-12-31 04:15:16",
                        image: "https://picsum.photos/id/1020/200/150",
                        text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book."
                    }
                ]
            }
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>