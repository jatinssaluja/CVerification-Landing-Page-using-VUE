<template>

<div>
     <h2 class="modal-heading">Login</h2>
      <form  action="">

      <div class="container">
         <label for="luname"><b>Username</b></label>
         <input type="text" placeholder="Enter Username" id="luname" required/>
         <span class="fa fa-user-circle-o fontawesome_span"></span>

         <label for="lpsw"><b>Password</b></label>
         <input type="password" placeholder="Enter Password" id="lpsw" required/>
         <span class="fa fa-lock fontawesome_span"></span>

         <a class="btn" href="#" @click="removeModal">Let's go</a>
         <a class="forgot-password" href="#">Forgot your password?</a>
        </div>

       </form>

    </div>

</template>

<script>
export default {
  name: 'LoginForm',
  data () {
    return {};
  },
  props:['removeModal']
}
</script>
