<template>
    <nuxt-link class="diosito" :to='nombre'>

        <div class="Tarjeta">
            <img :src="url" alt="">
            <div class="nombre"> {{nombre}} </div>
        </div>

    </nuxt-link>
</template>


<script>
export default {
data(){
    return {
        response: []
    }
},

  props:{
      nombre: {
          type: String,
          required: true
      },

      url: {
          type: String,
          required: true
      }
    },
    
}
</script>

<style>

.diosito{
    display: flex;
}

img{
    height: 300px;
}

.nombre{
    font-size: 30px;
    font-weight: 800px;
    text-align: center;
}

.Tarjeta{
    padding: 20px;
    border: 3px solid white;
    border-radius: 5px;
    width: 100%;
    height: auto;
    color: black;
    background: linear-gradient(45deg,blue,green,yellow,red,purple,black);
    background-size: 400% 400%;
    animation: cambiar 10s ease-in-out infinite;
    }

    @keyframes cambiar{
        0%{background-position: 0 25%;}
        50%{background-position: 100% 5%;}
        100%{background-position: 0 25%;}
    }
</style>