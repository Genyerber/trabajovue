<template>
    <div class="product-list">
      <h2>Gorras</h2>
      <div v-for="gorra in gorras" :key="gorra.id" class="product">
        <img :src="require(`@/assets/gorras/${gorra.imagen}`)" alt="Gorra">
        <h3>{{ gorra.nombre }}</h3>
        <p>{{ gorra.descripcion }}</p>
        <a :href="gorra.enlace">Ver detalles</a>
      </div>
    </div>
  </template>
  
  <script>
  import data from '@/data.json';
  
  export default {
    data() {
      return {
        gorras: data.gorras,
      };
    },
  };
  </script>
  
  <style scoped lang="scss">
  /* Estilos Sass para el componente Gorras */
  .product-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    
    .product {
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      margin: 16px;
      max-width: 300px;
      padding: 16px;
      text-align: center;
      transition: transform 0.3s ease-in-out;
      
      &:hover {
        transform: scale(1.05);
      }
      
      img {
        max-width: 100%;
        height: auto;
        border-radius: 4px;
      }
      
      h3 {
        margin-top: 8px;
        font-size: 1.5rem;
      }
      
      p {
        margin-top: 8px;
        font-size: 1rem;
        color: #777;
      }
      
      a {
        display: inline-block;
        margin-top: 12px;
        font-size: 1rem;
        text-decoration: none;
        color: #007bff;
        transition: color 0.3s ease-in-out;
        
        &:hover {
          color: #0056b3;
        }
      }
    }
  }
  </style>
  