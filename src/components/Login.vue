<template>
  <form v-on:submit.prevent>
    <div class="error" v-if="validEmail && validPassword">
      Details are Valid
    </div>
    <div class="error" v-else>
      Details are not Valid
    </div>
      <div class="form__item">
        <label for="email">Email Address</label>
        <input type="email" name="email" id="" v-model="newUser.email" v-bind:class="{ form__error: !validEmail }">
      </div>
      <div class="form__item">
        <label for="password">Password</label>
        <input type="password" name="password" id="" v-model="newUser.password" v-bind:class="{ form__error: valid }">
      </div>
      <button type="submit">Send</button>
    </form>
</template>

<script>
export default {
  name: 'LoginPage',
  data() {
    return {
      newUser: {
        email: '',
        password: ''
      },
      valid: false
    }
  },
  computed: {
    validEmail() {
      return this.newUser.email == 'oreoluwa@enyata.com'
    },
    validPassword() {
      return this.newUser.password == 'password'
    }
  }
}
</script>

<style scoped>
.form__error {
  background: black;
  color: red;
}
</style>