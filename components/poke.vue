<template>
    <div class="diosito">

        <div class="Tarjeta">
            <img :src="url" alt="">
            <div class="nombre"> {{nombre}} </div>
        </div>

    </div>
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
    flex-wrap: wrap;
    gap: 40px;
}

img{
    height: 300px;
    border: 1px solid blue;
}

.Tarjeta{
    padding: 20px;
    background-color: red;
    height: auto;
    color: white;
    border: 3px solid white;
    border-radius: 10px;
}
.nombre{
    font-size: 30px;
    font-weight: 800px;
    text-align: center;
}
</style>