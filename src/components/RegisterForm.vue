<template>

<div>
   <h2 class="modal-heading">Register</h2>
    <form  action="">

    <div class="container">
       <label for="runame"><b>Username</b></label>
       <input type="text" placeholder="Enter Username" id="runame" required/>
       <span class="fa fa-user-circle-o fontawesome_span"></span>

       <label for="email"><b>Email</b></label>
       <input type="email" placeholder="Enter Email" id="email" required/>
       <span class="fa fa-envelope fontawesome_span"></span>

       <label for="confirm-email"><b>Confirm Email</b></label>
       <input type="email" placeholder="Confirm Email" id="confirm-email" required/>
       <span class="fa fa-envelope fontawesome_span"></span>

       <label for="rpsw"><b>Password</b></label>
       <input type="password" placeholder="Enter Password" id="rpsw" required/>
       <span class="fa fa-lock fontawesome_span"></span>

       <label for="confirm-psw"><b>Confirm Password</b></label>
       <input type="password" placeholder="Confirm Password" id="confirm-psw" required/>
       <span class="fa fa-lock fontawesome_span"></span>

       <a class="btn" href="#" @click="removeModal">Register</a>
      </div>

     </form>

  </div>


</template>

<script>
export default {
  name: 'RegisterForm',
  data () {
    return {};
  },
  props:['removeModal']
}
</script>
