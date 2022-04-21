<template>
  <header>
    <!--inserire contenuto componente-->
    <div>
      <img src="../assets/img/Spotify_icon.svg" alt="Logo Spotify">
    </div>
    
  </header>
</template>

<script>
  

  export default {
    //Cambiare il nome con quello del componente creato
    name: 'HeaderComp',
    
    data(){
      return {
        selectChoice: ''
      }
    }
  }
</script>

<style scoped lang="scss">
  /*Inserire style componente*/
  header {
    background-color: #29333D;
    padding: 10px 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    div {
      img {
        width: 50px;
        margin-left: 20px;
      }
    }
  }
</style>