<template>
  <div>
    <h1>Formulario</h1>

    <form>
      <b-row>
        <b-col md="3">
          <b-form-input type="text" v-model="texto" :state="comprobar"></b-form-input>
          <small>Mínimo 3 carácteres</small>
          <p>Texto: {{ texto }}</p>
        </b-col>

        <b-col md="3"> 
          <b-form-select v-model="select" :options="animales"></b-form-select>
          <p>Selección: {{ select }}</p>
        </b-col>

        <b-col md="3"> 
          <b-form-radio-group v-model="radio" :options="animalesRadio"></b-form-radio-group>
          <p>Radio: {{ radio }}</p>
        </b-col>

        <b-col md="3">
          <b-form-checkbox-group
            v-model="check"
            :options="animalesRadio"
          ></b-form-checkbox-group>
          <p>Múltiple: {{ check }}</p>
        </b-col>
      </b-row>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      texto: '',
      radio: null,
      check: [],
      select: null,
      animales: [
        { value: null, text: 'Seleccione un animal' },
        { value: 'Perro', text: 'Guau Guau :v' },
        { value: 'Gato', text: 'Miau :v' },
        { value: 'Pato', text: 'Que miras pendejo :v' },
      ],
      animalesRadio: [
        { value: null, text: 'Seleccione un animal' },
        { value: 'Perro', text: 'Guau Guau :v' },
        { value: 'Gato', text: 'Miau :v' },
        { value: 'Pato', text: 'Que miras pendejo :v' },
      ]
    }
  },
  computed: {
    comprobar() {
      return this.texto.length > 2 ? true : false;
    }
  }
};
</script>
