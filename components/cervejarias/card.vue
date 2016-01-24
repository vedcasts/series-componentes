<script>
    export default {
        props: ['dados'],

        computed: {
            hasDescript () {
                return this.dados.descript != ''
            },
            location () {
                return this.dados.city + '/' + this.dados.state;
            }
        },

        methods: {
            sendDetails () {
                if(this.hasDescript) {
                    this.$dispatch('details', { dados: this.dados })
                }
            }
        }
    }
</script>

<template>
    <div 
        class="card"
        :class="{ 'has-descript': hasDescript }"
        @click="sendDetails">
        <img src="/link.png" class="link" v-if="hasDescript">
        <h3>{{ dados.name }}</h3>
        <p>{{ location }}</p>
    </div>
</template>

<style scoped>
    .link {
        width: 20px;
        height: 20px;
        position: absolute;
        right: 10px;
        top: 10px;
    }
    .card {
        position: relative;
        background-color: #f4f4f4;
        border: #ccc 1px solid;
        border-radius: 6px;
        padding: 10px;
        margin: 10px;
    }
    .has-descript {
        cursor: pointer;
    }
</style>



