<template>
  <div>
    <app-stock v-for="stock in stocks" :stock="stock"></app-stock>
  
  </div>
</template>

<script>
import Stock from './Stock.vue';

export default {
  components:{
    appStock: Stock
  },
  data(){
    return{
      stocks:[
        {id: 1, name: 'BMW', price: 110},
        {id: 2, name: 'Apple', price: 200},
        {id: 3, name: 'Google', price: 250},
        {id: 4, name: 'Twitter', price: 80},
      ]
      
    }
  }
}
</script>