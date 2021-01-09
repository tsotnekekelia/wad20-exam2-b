<template>
    <div>
        <button @click="reverseOrder()" id="reorder">
            <span v-if="!descending">Newest to Oldest</span>
            <span v-else>Oldest to Newest</span>
        </button>
        <ul>
            <li v-for="entry in sortedEntries" :key="entry.id" class="entry">
                <h2>{{entry.title}}</h2>
                <div>
                    <div>
                        <span class="entry-date">{{entry.date | formatDate}}</span>
                    </div>
                    <div v-if="entry.image">
                        <img :src="entry.image" alt="image" class="entry-image">
                    </div>
                    <div>
                        <p>{{entry.text}}</p>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    import moment from 'moment';

    export default {
        name: 'Entries',
        props: {
            entries: Array
        },
        data() {
            return {
                descending: false
            }
        },
        computed: {
            sortedEntries() {
                return this.sortByDate(this.entries, this.descending);
            }
        },
        filters: {
            formatDate(value) {
                return moment(value).format('LLLL');
            }
        },
        methods: {
            sortByDate(array, descending) {
                return array
                    .map((it) => {
                        it.date = moment(it.date);
                        return it
                    })
                    .sort((a, b) => {
                        return (!descending) ? b.date - a.date : a.date - b.date;
                    });
            },
            reverseOrder() {
                this.descending = !this.descending;
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>