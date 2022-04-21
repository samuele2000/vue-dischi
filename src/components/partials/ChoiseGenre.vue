<template>
  <div>
    <!-- select -->
    <div class="select">

      <select name="generi" id="generi" v-model="selectChoice">
        <optgroup label="Generi Musicali">
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
        </optgroup>
        <optgroup label="Artisti">
          <option value="Bon Jovi">Bon Jovi</option>
          <option value="Sting">Sting</option>
          <option value="Steve Gadd Band">Steve Gadd Band</option>
          <option value="Iron Maiden">Iron Maiden</option>
          <option value="Eric Clapton">Eric Clapton</option>
          <option value="Deep Purple">Deep Purple</option>
          <option value="Metallica">Metallica</option>
          <option value="Dave Weckl">Dave Weckl</option>
          <option value="Michael Jacjson">Michael Jacjson</option>
        </optgroup>

      </select>

      <button type="button" @click.prevent="$emit('funzioneGenere', selectChoice)">Scegli</button>
    </div>
  </div>
</template>

<script>
  export default {
    //Cambiare il nome con quello del componente creato
    name: 'ChoiseGenre',

    data() {
      return {
        selectChoice: ''
      }
    }
  }
</script>

<style scoped lang="scss">
  /*Inserire style componente*/

  .select {
    margin-bottom: 40px;

    label {
      color: white;
      font-weight: bold;
      font-size: 1.1em;
    }

    select {
      padding: 5px 30px 5px 0;
    }

    button {
      margin-left: 20px;
      padding: 5px 20px 5px;
      background-color: white;
      text-align: center;
      font-weight: bold;
      border: none;
    }
  }
</style>