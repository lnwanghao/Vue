<template>
    <div class="login">
        <form>
            <input v-model="username" placeholder="username">
            <input type="password" v-model="password" placeholder="password">
            <button type="submit" @click="login">登陆</button>
        </form>
    </div>
</template>
<script>
export default {
  name: "Login",
  data() {
    return {
      username: "",
      password: ""
    };
  },
  methods: {
    login: function(e) {
      e.preventDefault();
      console.log(this.username, this.password);
    }
  },
  created: function() {
    console.log("Login Page");
  }
};
</script>

<style scoped>
.login {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 400px;
  height: 300px;
  margin: 0 auto;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}
input {
  display: block;
  width: 300px;
  height: 30px;
  margin: 0 auto;
  margin-bottom: 15px;
  border: 1px solid #ddd;
  border-radius: 4px;
  text-indent: 5px;
  transition: all 0.2s ease-in-out;
}
input:focus {
  border-color: #4990e2;
}
button {
  width: 300px;
  height: 30px;
  background-color: #4990e2;
  color: #fff;
  border-radius: 4px;
  border: 0;
  font-size: 14px;
  font-weight: bold;
}
button:active {
  box-shadow: inset 1px 1px 2px rgba(0, 0, 0, 0.3);
}
</style>

