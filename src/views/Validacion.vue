<template>
  <div>
    <h3>Vuelidate</h3>
    <form>
      <input type="email" placeholder="Ingresa un email" class="form-control my-3" v-model="$v.email.$model" :class="{'is-invalid' : $v.email.$error}">
      <p class="text-danger" v-if="!$v.email.email">Este email es incorrecto</p>
      <p class="text-danger" v-if="!$v.email.required">Campo requerido</p>
      <p>{{ $v.email }}</p>
    </form>
  </div>
</template>

<script>
import { required, email } from 'vuelidate/lib/validators'

export default {
  data() {
    return {
      email: '',
    }
  },
  validations: {
    email: { required, email}
  }
}
</script>