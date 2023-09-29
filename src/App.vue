<template>
  <div id="app">
    <camisasProductos />
    <GorrasProductos />
    <HoodiesProductos />
    <PosillosProductos />
  </div>
</template>


<script>
// Ejemplo de actualización de importación en App.vue
import camisasProductos from './components/camisasProductos.vue';
import GorrasProductos from './components/GorrasProductos.vue';
import HoodiesProductos from './components/HoodiesProductos.vue';
import PosillosProductos from './components/PosillosProductos.vue';

export default {
  components: {
    camisasProductos,
    GorrasProductos,
    HoodiesProductos,
    PosillosProductos,
  },
};

</script>

<style scoped>
/* Estilos CSS globales para la aplicación */
body {
  font-family: Arial, sans-serif;
  background-color: #f0f0f0;
  margin: 0;
  padding: 0;
}

#app {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.product-list {
  margin: 20px;
}

.product {
  background-color: #fff;
  border-radius: 5px;
  padding: 20px;
  margin: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  max-width: 300px;
}

.product img {
  max-width: 100%;
}

.product h3 {
  margin-top: 10px;
}

.product a {
  display: inline-block;
  margin-top: 10px;
  text-decoration: none;
  color: #007bff;
}
</style>
