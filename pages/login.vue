<template>
  <div>
    <div>
      login
    </div>
    <div>
      <form @submit.prevent="userLogin">
        <div>
          <label>Username</label>
          <input type="text" v-model="login.username" />
        </div>
        <div>
          <label>Password</label>
          <input type="text" v-model="login.password" />
        </div>
        <div>
          <button type="submit">Submit</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  auth: false,
  data() {
    return {
      login: {
        username: "test@example.com",
        password: "123456"
      }
    };
  },
  methods: {
    async userLogin() {
      // try {
      // let response = await this.$auth.loginWith("local", { data: this.login });
      // let response = await this.$axios.post("auth/sign_in", this.login);
      let response = await this.$axios.get("apa");
      console.log(response);
      // } catch (err) {
      // console.log(err)
      // }
    }
  }
};
</script>
