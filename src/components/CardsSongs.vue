<template>
    <div class="container">
        <div class="genere">
            <ChoiseGenre @funzioneGenere="metodoGenere"/>
        </div>
        <div class="row">
           <Card v-for="(element, index) in filtraggioGenere()" :key="index" 
           :title="element.title" 
           :year="element.year"
           :poster="element.poster"
           :author="element.author"  
           :genere="element.genre"/>
        </div>
         
    </div> 
      

    

</template>

<script>
    import axios from 'axios';
    import Card from './partials/Card.vue'
    import ChoiseGenre from './partials/ChoiseGenre.vue'

    export default {
        //Cambiare il nome con quello del componente creato
        name: 'CardsSongs',
        components: {
            Card,
            ChoiseGenre
        },
        data() {
            return {
                songArray: [],
                genereScelto: ''
            }
        },

        created() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
                .then((res) => {
                    console.log(res.data)
                    this.songArray = res.data
                })
            console.log(this.songArray)
        },

        // methods
        methods: {
           metodoGenere(selectChoice){
               this.genereScelto = selectChoice
               console.log(this.genereScelto)
           }, 

           filtraggioGenere(){
               if( this.genereScelto === '' ){
                   return this.songArray.response
               } else{
                   return this.songArray.response.filter((element) =>{
                       return element.genre.includes(this.genereScelto)
                   })
               }
           }
        }
    }
</script>

<style scoped lang="scss">
    /*Inserire style componente*/
    .container {
        width: 80%;
        margin: 0 auto;
        padding: 50px 0;
        .row{
            display: flex;
            flex-wrap: wrap;
        }
        .genere{
            text-align: end;
        }
    }
</style>