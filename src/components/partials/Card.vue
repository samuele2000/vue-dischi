<template>
    <div>
        <img :src="poster" alt="">
        <h3>{{title}}</h3>
        <h4>{{author}}</h4>
        <h4>{{year}}</h4>
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
            author: String,
            genere: String
        }
    }
</script>

<style scoped lang="scss">
    /*Inserire style componente*/
    div{
        background-color: #29333D;
        text-align: center;
        width: calc((100% / 5) - 10px);
        margin: 10px 5px;
        padding: 20px 10px 10px 10px;
        h3{
            color: white;
            font-size: 1.3em;
            margin-bottom: 20px;
        }
        h4{
            color: gray;
            
        }
    }
        img{
            width: 150px;
        }
    
</style>