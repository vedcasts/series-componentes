
<script>
    
    import VcCervejaria from './card.vue'
    import VcModal from '../modal.vue'
    
    export default {
        components: {
            VcCervejaria,
            VcModal
        },
        data () {
            return {
                cervejarias: [],
                cervejaria: {}
            }
        },
        ready () {
            this.$http.get('/cervejarias.json').then(
                (req) => this.cervejarias = req.data)
        },
        methods: {
            showDetails (cervejaria) {
                this.cervejaria = cervejaria.dados
            }
        }
    }
</script>

<template>
    <vc-modal 
        :name="cervejaria.name" 
        :descript="cervejaria.descript">
    </vc-modal>
    <h3>Componente de cervejarias!</h3>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quaerat porro error in voluptate facere tempora dolorem deleniti, corporis, fugit unde adipisci voluptas nisi qui atque necessitatibus quo ipsum, modi reprehenderit!</p>
    <vc-cervejaria 
        v-for="cervejaria in cervejarias"
        @details="showDetails"
        :dados="cervejaria">
    </vc-cervejaria>
</template>



