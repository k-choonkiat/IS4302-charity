<template>
  <div>
    <div class="login-for-beneficiaries">
      <h3>Sign in for Beneficiaries</h3>
      <input type="text" placeholder="Email">
      <br>
      <input type="password" placeholder="password">
      <br>
      <button @click="loginB">Log In</button>
    </div>
    <br>

    <div class="login-for-donors">
      <h3>Sign in for Donors</h3>
      <input type="text" placeholder="Email">
      <br>
      <input type="password" placeholder="password">
      <br>
      <button @click="loginD">Log In</button>
    </div>
    <br>

    <div class="login-for-charity">
      <h3>Sign in for Charity</h3>
      <input type="text" placeholder="Email">
      <br>
      <input type="password" placeholder="password">
      <br>
      <button @click="loginC">Log In</button>
      <p>
        You don't have an account ? You can
        <router-link to="Signup">create one</router-link>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {};
  },
  methods: {
    loginB: function() {
      //console.log("pushed")
      this.$router.push({ name: "Beneficiary" });
    },
    loginD: function() {
      this.$router.replace("Donor");
    },
    loginC: function() {
      this.$router.replace("Charity");
    }
  }
};
</script>

<style scoped>
.login {
  margin-top: 40px;
}
input {
  margin: 10px 0;
  width: 20%;
  padding: 15px;
}

button {
  margin-top: 20px;
  width: 10%;
  cursor: pointer;
}

p a {
  text-decoration: underline;
  cursor: pointer;
}
</style>