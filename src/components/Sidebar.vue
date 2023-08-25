<template>
  
<aside :class="`${is_expanded && 'is-expanded'}`">
<div class="logo">
    <img  src="../assets/logo.png" alt="">
</div>

<div class="menu-toggle-wrap">
    <button  class="menu-toggle" @click="ToggleMenu">
        <span class="material-symbols-outlined">
double_arrow
</span>
    </button>
</div>

<h6><b>Menu</b></h6>
<div class="menu">
    <router-link to="/dashboard" class="button">
        <span class="material-symbols-outlined">
home
</span>
        <span class="title">About</span>
    </router-link>
    <router-link to="/about" class="button">
        <span class="material-symbols-outlined">
person
</span>
        <span class="title">Profile</span>
    </router-link>
    <hr>
    <router-link to="/" class="button">
        <span class="material-symbols-outlined">
logout
</span>
        <span class="title">Logout</span>
    </router-link>
</div>




</aside>
  
</template>


<script setup>
import { ref } from 'vue';

const is_expanded = ref(false)


const ToggleMenu = () => {
    is_expanded.value = !is_expanded.value
}
</script>

<script>
import "bootstrap/dist/css/bootstrap.css";


export default {
  name: "SidebarCom",
};
</script>

<style lang="scss" scoped>

aside{
    min-height: 100vh;
    background-color: var(--green);
    color: var(--dark);
    display: flex;
    flex-direction: column;
    width: calc(2rem + 40px);
    padding: 1rem;
    overflow: hidden;

    transition: 0.2s ease-out;
    .logo{
        margin-left: 0.2rem;
        margin-bottom: 1rem;
        img{
            width: 2rem;
            
        }
    }
    .menu-toggle-wrap{
    display: flex;
    justify-content: center;

    margin-bottom: 1rem;
    position: relative;
    top: 0;
    transition: 0.2s ease-out;
    
    .menu-toggle{
        transition: 0.2 ease-out;
        border: 0;
        padding: 0;
        margin: 0;
        background-color: var(--green);

        span{
            color: var(--dark);
        }
        
    }

    }
    h6, .button .title{
        opacity: 0;
        transition: 0.3s ease-out;
    }
    
    

    &.is-expanded {
        width: var(--sidebar-width);
        
        .menu-toggle-wrap{
            display: flex;
            justify-content: flex-end;
            top: -3rem;
            .menu-toggle{
                transform: rotate(-180deg);
            }
        }
        h6, .button, .title{
            opacity: 1;
        }
        h6{
            color: var(--grey);
            font-size: 0.875rem;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
        }
        .menu{
            .button{
                margin-bottom: 1rem;
            .title{
                display: inline;
                color: var(--dark);
                transition: 0.2s ease-out;
                padding-left: 1rem;
            }

            &:hover{
                border-radius:10px;
                background-color: var(--light);
                transition: 1 ease-out;
                
            }
            }
        }
        
    }

    .menu{
        margin: 0 -0.9rem;
        .button {
            display: flex;
            align-items: center;
            text-decoration: none;

            padding: 0.5rem 1rem;
            transition: 0.2s ease-out;
        
            .title{
                display: none;
                color: var(--light);
                transition: 0.2s ease-out;
            }
            &:hover, &.router-link-exact-active{
                background-color: var(--greentea);
                
                
                
                .material-symbols-outlined, .title{
                    color: var(--darker);
                }
            }
            &.router-link-exact-active{
                border-right: 5px solid var(--dark);
            }
        }
        }


    @media (max-width: 425px) {
        position: fixed;
        z-index: 99;
    }

    .material-symbols-outlined {
        font-size: 2rem;
        color: var(--dark);
  font-variation-settings:
  'FILL' 1,
  'wght' 300,
  'GRAD' 0,
  'opsz' 48
}

}


</style>
