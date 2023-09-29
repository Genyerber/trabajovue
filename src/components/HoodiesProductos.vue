<template>
    <div class="product-list">
      <h2>Hoodies</h2>
      <div v-for="hoodie in hoodies" :key="hoodie.id" class="product">
        <img :src="require(`@/assets/hoodies/${hoodie.imagen}`)" alt="Hoodie">
        <h3>{{ hoodie.nombre }}</h3>
        <p>{{ hoodie.descripcion }}</p>
        <a :href="hoodie.enlace">Ver detalles</a>
      </div>
    </div>
  </template>
  
  <script>
  import data from '@/data.json';
  
  export default {
    data() {
      return {
        hoodies: data.hoodies,
      };
    },
  };
  </script>
  
  <style scoped>
  /* Estilos CSS para el componente Hoodies */
  </style>
  