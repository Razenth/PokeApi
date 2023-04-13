<template>
    <loading v-if="loading"/>
    <div class="father" v-else>
        <h1>PokeDex</h1>
        <form action="" @submit.prevent="busqueda">
          <input type="text" placeholder="Buscar a un Pokemón" v-model="search" class="buscar">
        </form>

        <div class="cartas">
            <poke v-for="i in response" :key="i.name" :nombre='i.name' :url='i.sprites.front_default'/>
        </div>
    </div>
</template>

<script>
export default {
  name: 'PokePage',

  data(){
    return{
      response: [],
      search:"",
      loading: true
    }
  },

  mounted(){
        this.getInfo()
    },

  methods: {
      async getInfo(){

      try {
        for (let i=1; i<20; i++){
          const {data} = await this.$axios.get(`pokemon/${i}`)    
          this.response.push(data)
        }
        setTimeout(() => {
          this.loading = false
        }, 1500);

      } catch (error) {
        
      }
        
      },

      busqueda(){
        this.search = this.search.toLowerCase()
        for (let i=0; i<this.response.length;i++){
          if (this.response[i].name==this.search){
            this.$router.push(`${this.search}`)
          }
        }
      }
  },
}
</script>

<style>
    .father{
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: rgb(34, 34, 34);
        height: 100%;
        padding: 15px;
    }

    h1{
        background-color: transparent;
        color: red;
        width: 50%;
        height: 100px;
        text-align: center;
        font-size: 75px;
        font-weight: 700;
        border-radius: 10px;
        margin-bottom: 20px;
    }

    .buscar{
        align-self: flex-start;
        height: 25px;
        margin-bottom: 15px;
        background-color: transparent;
        outline: none;
        border-bottom: 2px solid white;
        color: white;
        padding: 10px;
    }

    .cartas{
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 40px;
      margin-top: 20px;
    }
</style>