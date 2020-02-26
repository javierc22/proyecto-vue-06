<template>
  <div>
    <h3>Vuelidate</h3>
    <form @submit.prevent="submit">
      <h4>Email</h4>
      <input type="email" placeholder="Ingresa un email" class="form-control my-3" v-model="$v.email.$model" :class="{'is-invalid' : $v.email.$error}">
      <p class="text-danger" v-if="!$v.email.email">Este email es incorrecto</p>
      <p class="text-danger" v-if="!$v.email.required">Campo requerido</p>
      <p>{{ $v.email }}</p>

      <h4>Contraseña</h4>
      <input type="password" placeholder="Ingresa contraseña" class="form-control my-3" v-model="$v.password.$model" :class="{'is-invalid' : $v.password.$error}">
      <p class="text-danger" v-if="!$v.password.minLength">Mínimo 5 carácteres</p>
      <input type="password" placeholder="Repite contraseña" class="form-control my-3" v-model="$v.repeatPassword.$model" :class="{'is-invalid' : $v.repeatPassword.$error}">
      <p class="text-danger" v-if="!$v.repeatPassword.sameAsPassword">La contraseña no coincide</p>

      <b-button variant="primary" type="submit" :disabled="$v.$invalid">Enviar</b-button>

      {{ $v.$invalid }}
    </form>
  </div>
</template>

<script>
import { required, email, sameAs, minLength } from 'vuelidate/lib/validators'

export default {
  data() {
    return {
      email: '',
      password: '',
      repeatPassword: '',
    }
  },
  validations: {
    email: { required, email},
    password: {
      required, 
      minLength: minLength(5)
    },
    repeatPassword: {
      sameAsPassword: sameAs('password')
    }
  },
  methods: {
    submit(){
      console.log('submit!');
      this.$v.$touch()
      if (this.$v.$invalid) {
        console.log('Se generó un error!');
      } else {
        console.log('Todos los campos correctos');
        console.log('Enviando información...' + this.$v.email.$model + ' ' + this.$v.password.$model);
      }
    }
  },
}
</script>