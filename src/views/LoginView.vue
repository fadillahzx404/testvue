<template>
  <NavbarCom />
  <div id="login">
    <div class="container vh-100">
      
      
      <div class="row">
        <div class="col-md-6 d-none d-md-block">
          
          <div class="container image">
          <img class="animate__animated animate__fadeInDown leaf" src="../assets/leaf.png" alt="" />
          <img class="img-fluid" src="../assets/Tree.jpg" alt=""/>
          </div>
          
        </div>
        <div class="col-md-4 mx-auto align-self-center">
          <div class="col heading">
            <h2 class="pb-2">
              <img
                class="imageLog"
                width="30"
                height="24"
                src="../assets/logo.png"
                alt=""
              />
              Login
            </h2>
            <p class="pb-3">Please login into your account !</p>
          </div>

          <div class="mb-3">
            <label for="exampleInputEmail1" class="form-label"
              >Email address</label
            >
            <input
              type="email"
              class="form-control"
              id="exampleInputEmail1"
              aria-describedby="emailHelp"
              v-model="email"
            />
            <div id="emailHelp" class="form-text">
              We'll never share your email with anyone else.
            </div>
          </div>
          <div class="mb-5">
            <label for="exampleInputPassword1" class="form-label"
              >Password</label
            >
            <input
              type="password"
              class="form-control"
              id="exampleInputPassword1"
              v-model="password"
            />
          </div>
          <div class="d-grid">
            <button
              @click="$router.push('dashboard')"
              class="btn btn-success mb-2"
            >
              Login
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <FooterCom />
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import "animate.css/animate.css";
import NavbarCom from "@/components/Navbar.vue";
import FooterCom from "@/components/Footer.vue";

export default {
  name: "LoginView",
  components: {
    NavbarCom,
    FooterCom,
  },
};
</script>

<script setup>
import { ref } from "vue";

const email = ref("user@test.com");
const password = ref("12345678");
</script>

<style >
#login {
  padding-top: 100px;

  @media (min-width: 1440px) {


    @-webkit-keyframes mymove  {
    
       0% {
        top:0px;
    }
    25% {
        top:200px;
    }
    50% {
        top:100px;
    }
    75% {
        top:200px;
    }
    100% {
        top:0px;
    }
      
    }

    .leaf{
      position:absolute;
      width: 24px;

    -webkit-animation: mymove 2s infinite;
    animation: mymove 2s infinite;
    }
    
    /* .leaf {
      position: absolute;
      
      padding-left: 8px;
      top: 200;
      width: 24px;
      transform: rotate(-200deg);
      -webkit-animation: leafanimation;
      -webkit-animation-duration: 2s;  
      z-index: 1; 
    } */
    

    .img-fluid{
      z-index: -1;
    }
    

    
  }
}
</style>
