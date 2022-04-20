<template>
  <div>
      <Card v-for="(element, index) in songArray.response" :key="index"
      :title="element.title"
      :year="element.year"
      :poster="element.poster"
      :author="element.author"/>
  </div>
</template>

<script>
import axios from 'axios';
import Card from './Card.vue'

export default {
  //Cambiare il nome con quello del componente creato
  name: 'CardsSongs',
  components: {
      Card
  },
  data(){
      return{
          songArray : []
      }
  }, 

  created(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then( (res) =>{
            console.log(res.data)
            this.songArray = res.data
        } )
        console.log(this.songArray)
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/
 
</style>