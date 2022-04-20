<template>
  <div>
      <img :src="poster" alt="">
      <h3>{{title}}</h3>
      <h6>{{author}}</h6>
      <h6>{{year}}</h6>
  </div>
</template>

<script>


export default {
  //Cambiare il nome con quello del componente creato
  name: 'Card',
  props: {
      title: String,
      year: String,
      poster: String,
      author: String
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/
 
</style>