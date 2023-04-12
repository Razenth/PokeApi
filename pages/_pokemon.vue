<template>
    <div class="father">

        <div class="tarjeta">
            <!-- <choosePoke v-for="i in poke.abilities" :key="i.key" :nombre='nombre' 
                :hp='i.stats[0].base_stat' 
                :atack='i.stats[1].base_stat'
                :defense='i.stats[2].base_stat'
                :special_atack='i.stats[3].base_stat'
                :special_defense='i.stats[4].base_stat'
                :speed='i.stats[5].base_stat'
                /> -->
                <p v-for="i in poke.abilities" :key="i.name">
                    {{i.ability.name}}
                </p>

                <p v-for="i in poke.stats" :key="i.stat.name">
                    {{i.stat.name}} : {{i.base_stat}}
                </p>

                <img :src="url" alt="">
        </div>
    </div>
</template>


<script>
    export default {
        name: 'PaginadelPokemon',

        mounted(){
            // console.log(this.$route);
            this.getInfo()
        },
    
        data(){
            return{
            poke: [],
            nombre:this.$route.params.pokemon,
            url:''
            }
        },

        methods: {
            async getInfo(){
                const {data} = await this.$axios.get(`pokemon/${this.$route.params.pokemon}`)    
                this.poke=data
                console.log(data)
                console.log(this.poke.sprites)
                this.url=this.poke.sprites.other.dream_world.front_default
            }
        },
}
</script>

<style>
</style>

