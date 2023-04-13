<template>
    <div class="father">

        <div class="tarjeta">
                <p>{{nombre}} </p>

                <p v-for="i in poke.abilities" :key="i.name">
                    {{i.ability.name}}
                </p>

                <p v-for="i in poke.stats" :key="i.stat.name">
                    {{i.stat.name}} : {{i.base_stat}}
                </p>

                <img :src="url1" alt="">

                <div>

                </div>
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
            url1:'',
            url2:'',
            url3:'',
            url4:'',
            }
        },

        methods: {
            async getInfo(){
                const {data} = await this.$axios.get(`pokemon/${this.$route.params.pokemon}`)    
                this.poke=data
                console.log(data)
                console.log(this.poke.sprites)
                this.url1=this.poke.sprites.other.dream_world.front_default
            }
        },
}
</script>

<style>
</style>

