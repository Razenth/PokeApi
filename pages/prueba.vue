<template>
    <div>
        <p>{{nombre}}</p>
        <img src="https://nextluxury.com/wp-content/uploads/cursed-images-20.jpg" alt="" v-if="mostrar == true">
        <button @click="cambiar">Cambiar nombre</button>    
    </div>
</template>

<script>
export default {
  name: 'PruebaPage',
  data() {
      return {
          nombre: 'Santiago',
          mostrar: false,
      }
  },
  methods: {
      cambiar(){
          if(this.nombre == 'Santiago'){
            this.nombre = 'González Agudelo'
            this.mostrar = true

          }else{
              this.nombre = 'Santiago'
              this.mostrar = false
          }
      }
  }
}
</script>

<style>
    p{
        background-color: black;
        color: white;
    }
</style>
