<script setup>
import {onMounted, ref} from "vue";
import {apiProducts} from './service/neuapp';
import Product from './components/products.vue';


const products = ref([]);

onMounted(async () => {
  loadProducts()
})


async function loadProducts(){
  alert('cargando productos...')
  try{
    let response = await apiProducts()
    if(response.status==200){
      console.log(response.data)
    }
  }catch (err){

  }

}
</script>

<template>
    <div>
    <Product></Product>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
