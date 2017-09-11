<template>
  <form action="/addPlayers" method="POST" @submit.prevent="onSubmit">
    <b-field label="Name">
      <b-input 
        placeholder="Enter your first and last name..."
        icon="user-circle"
        v-model="name">  
      </b-input>
    </b-field>

    <b-field label="Email"
      type="is-danger"
      message="This email is invalid">
      <b-input type="email"
        placeholder="Enter your email..."
        v-model="email"
        icon="envelope"
        maxlength="30">
      </b-input>
    </b-field>

    <b-field label="Username"
      type="is-success"
      message="This username is available">
      <b-input 
        value="johnsilver"
        placeholder="Enter a username"
        icon="id-card" 
        v-model="username"     
        maxlength="30"></b-input>
    </b-field>

    <b-field label="Password"
      type="is-warning"
      :message="['Password is too short', 'Password must have at least 8 characters']">
      <b-input 
        value="123" 
        type="password"
        icon="lock" 
        v-model="password"
        maxlength="30"></b-input>
    </b-field>
    <b-field>
      <p class="control">
        <button class="button is-primary">
          Submit
        </button>
      </p>
    </b-field>
    <!-- <b-field label="Subject">
      <b-select placeholder="Select a subject">
        <option value="1">Option 1</option>
        <option value="2">Option 2</option>
      </b-select>
    </b-field> -->
  </form>
</template>

<script>

import axios from 'axios'

export default {
  data () {
    return {
      name: '',
      email: '',
      username: '',
      password: ''
    }
  },
  methods: {
    onSubmit: function () {
      axios.post('../middleware/addPlayers.js', this.$data)
        .then(respones => alert('success'))
        .catch(error => alert(error.response.data))
    }
  }
}
</script>

<style>

</style>
