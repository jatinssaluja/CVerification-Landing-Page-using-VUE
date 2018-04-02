<template>
  <div id="app">

    <header>
      <Backdrop v-if="loginModalSelected || registerModalSelected" :remove-modal="remove"/>
      <nav>
          <div class="logo">
              <img src="./assets/logo-dark.png" alt="CVerification Logo"/>
             </div>
         <ul class="flex-nav">
          <li><a href="#" @click="loginModalSelected=true">Login</a></li>
          <li><a href="#" @click="registerModalSelected=true">Register</a></li>
          <li><a href="#">Dashboard</a></li>
         </ul>

           </nav>

           <Modal v-show="loginModalSelected">
                  <LoginForm :remove-modal="remove"/>
                </Modal>

                <Modal v-show="registerModalSelected">
                  <RegisterForm :remove-modal="remove"/>
                </Modal>

    </header>

  </div>
</template>

<script>

import Backdrop from './components/Backdrop';
import Modal from './components/Modal';
import LoginForm from './components/LoginForm';
import RegisterForm from './components/RegisterForm';


export default {
  name: 'App',
  data () {
    return {
      loginModalSelected:false, registerModalSelected:false
    }
  },

  methods:{

          remove: function(){

           this.loginModalSelected = false;
           this.registerModalSelected = false;
          }

         },
  components: {

  Backdrop,
  Modal,
  LoginForm,
  RegisterForm

  }
}
</script>

<style>

*{
  margin: 0;
  padding: 0;
  font-family: "Roboto Condensed", sans-serif;
  box-sizing: border-box;
}

html{

font-size: 20px;
font-weight: 300;

}



header{

  background-size:cover;
  background-position: center;
  background: url('./assets/bg-home.jpg') no-repeat;
  height: 100vh;

}


input[type=text], input[type=password],input[type=email] {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: none transparent;
    border-radius: 5px;
    box-sizing: border-box;
    background-color: #f1f1f1;
}


.modal-heading{

  padding: 12px 20px;
  margin: 8px 0;
  font-weight:lighter;

}

.fontawesome_span{

 float:right;
 margin-right: 6px;
 margin-top:-30px;
 position:relative;
 z-index: 2;


}




.btn:link,
.btn:visited{

 display:table;
 padding:10px 30px;
 font-weight: 300;
 text-decoration: none;
 background-color: #636e72;
 border-radius: 200px;
 color: #fff;
 margin: 20px auto;
 text-align: center;
 transition: background-color 0.2s;

}

.btn:hover,
.btn:active{

 background-color: #242829;

}

.forgot-password:link,
.forgot-password:visited{

  display:table;
  font-weight: 300;
  text-decoration: none;
  color:#e84393;
  text-align: center;
  margin: 5px auto;
  transition: color 0.2s;

}

.forgot-password:hover,
.forgot-password:active{

  color:#ce1971;

}



.container {
    padding: 16px;
}


nav{

 display: flex;
 flex-direction: column;

}

.logo{

  text-align: center;
  height:100px;
  width:auto;
  margin-top: 20px;

}

.flex-nav{

 list-style: none;

}

.flex-nav li a:link,
.flex-nav li a:visited{

 display: block;
 text-decoration: none;
 text-align: center;
 color: #fff;
 padding: 8px;
 font-size: 90%;
 border-bottom: 2px solid transparent;
 transition: border-bottom 0.2s;


}



.flex-nav li a:hover,
.flex-nav li a:active{

 border-bottom: 2px solid #e84393;


}

@media only screen and (min-width: 1025px){

   nav{
     display: flex;
     flex-direction: row;
     justify-content: space-between;
     align-items: center;

   }

   nav .flex-nav{
     display: flex;
     align-items: center;
     margin-right: 40px;
   }

   nav .logo{

    margin-left: 40px;

   }


}



@media only screen and (min-width: 769px){

  nav .flex-nav{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-left: 40px;
    margin-right: 40px;
  }


}





</style>
