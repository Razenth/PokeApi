<template>
    <div class="conteiner">
        <h1>{{nombre}}</h1>
        
        <p>Stats</p>
        <!-- <ul>
            <li>Hp:{{hp}} </li>
            <li>Attack:{{atack}} </li>
            <li>Defense:{{defense}} </li>
            <li>Special-Attack:{{special_atack}} </li>
            <li>Special-Defense:{{special_defense}}</li>
            <li>Speed:{{speed}}</li>
        </ul> -->
    </div>
</template>


<script>
export default {
data(){
    return {
        poke: []
    }
},

  props:{
      nombre: {
          type: String,
          required: true
      },

      hp: {
          type: Number,
          required: true
      },

      atack: {
          type: Number,
          required: true
      },

     defense: {
         type: Number,
         required: true
     },

     special_atack: {
         type: Number,
         required: true
     },

     special_defense: {
         type: Number,
         required: true
     },

     speed: {
         type: Number,
         required: true
     }




    },
    
}
</script>


:nombre='nombre' 
                :hp='i.stats[0].base_stat' 
                :atack='i.stats[1].base_stat'
                :defense='i.stats[2].base_stat'
                :special_atack='i.stats[3].base_stat'
                :special_defense='i.stats[4].base_stat'
                :speed='i.stats[5].base_stat'