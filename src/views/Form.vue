<template>
  <div>
    <h1>Formulario</h1>

    <form>
      <b-row>
        <b-col md="6">
          <b-form-input type="text" v-model="texto" :state="comprobar"></b-form-input>
          <small>Mínimo 3 carácteres</small>
        </b-col>
      </b-row>
    </form>
    <p>Texto: {{ texto }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      texto: '',
    }
  },
  computed: {
    comprobar(){
      return this.texto.length > 2 ? true : false
    }
  },
}
</script>