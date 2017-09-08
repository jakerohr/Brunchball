<template>
  <section>
    <b-field label="Name">
      <b-input 
        placeholder="Enter your first and last name..."
        icon="user-circle">  
      </b-input>
    </b-field>

    <b-field label="Email"
      type="is-danger"
      message="This email is invalid">
      <b-input type="email"
        placeholder="Enter your email..."
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
        maxlength="30"></b-input>
    </b-field>

    <b-field label="Password"
      type="is-warning"
      :message="['Password is too short', 'Password must have at least 8 characters']">
      <b-input 
        value="123" 
        type="password"
        icon="lock" 
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
  </section>
</template>

<script>
export default {
  // data () {
  //   return {
  //     isActive: false
  //   }
  // },
  // methods: {
  //   toggleBurger: function () {
  //     this.isActive = this.isActive === false
  //     return this.isActive
  //   }
  // }
}
</script>

<style>

</style>
