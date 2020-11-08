<template>
   <div class="content">
      <h1 class="page-title">Log In</h1>
      <form class="login-form" v-on:submit.prevent="login">
         <div class="form-group">
            <label for="username">User Name</label>
            <input type="text" class="form-control" id="username" />
         </div>
         <div class="form-group">
            <label for="password">Password</label>
            <input type="password" class="form-control" id="password" />
         </div>
         <div class="form-group form-check">
            <input type="checkbox" class="form-check-input" id="remember_me" />
            <label class="form-check-label" for="remember_me">Remember Me</label>
         </div>
         <button type="submit" class="btn btn-primary">Submit</button>
      </form>
   </div>
</template>

<script>
export default {
   methods: {
      login() {
         this.$router.push("/");
      },
   },
};
</script>

<style scoped>
.login-form {
   margin-top: 15px;
}
</style>
