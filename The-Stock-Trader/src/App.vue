<template>
    <div class="container">
      <app-header></app-header>
      <div class="row">
        <div class="col-xs-12">
          <transition name="slide" mode="out-in">
            <router-view></router-view>
          </transition> 
        </div>
      </div>
    </div>
</template>

<script>
import Header from './components/TheHeader.vue';

    export default {
      components:{
        appHeader: Header
      },
      created(){
        this.$store.dispatch('setStocks');
      }
    }
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");

  * {
    box-sizing: border-box;
  }

  html {
    font-family: "Roboto", sans-serif;
  }

  body {
    margin: 0;
  }
  .slide-enter-active{
    animation: slide-in 200ms ease-out forwards;
  }

  .slide-leave-active{
    animation: slide-out 200ms ease-out forwards;
  }

  @keyframes slide-in {
    from{
      transform: translateY(-30px);
    }
    to{
      transform: translateY(0);
      opacity: 1;
    }
    
  }
  @keyframes slide-out {
    from{
      transform: translateY(0);
    }
    to{
      transform: translateY(-30px);
      opacity: 0;
    }
    
  }

</style>
