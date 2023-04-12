<template>
    <div class="father">
        <h1>PokeDex</h1>
        <input type="text" placeholder="Buscar a un Pokemón">

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
      response: []
    }
  },

  mounted(){
        this.getInfo()
    },

  methods: {
      async getInfo(){
        for (let i=1; i<20; i++){
          const {data} = await this.$axios.get(`pokemon/${i}`)    
          this.response.push(data)
        }
      },
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
        background-color: white;
        color: rgb(130, 74, 175);
        width: 50%;
        height: 100px;
        text-align: center;
        font-size: 75px;
        font-weight: 700;
        border-radius: 10px;
        margin-bottom: 20px;
    }

    input{
        align-self: flex-start;
        height: 25px;
        margin-bottom: 15px;
    }

    .cartas{
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 40px;
    }
</style>