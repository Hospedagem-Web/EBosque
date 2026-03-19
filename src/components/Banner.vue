<template>
  <section class="banner">
    <!-- Imagem recebida pela prop -->
    <img :src="image" alt="Banner Image" class="banner-image" />

    <!-- Conteúdo sobreposto -->
    <div class="banner-content">
      <slot></slot>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: "Banner",
  props: {
    image: {
      type: String,
      required: true
    }
  }
})
</script>

<style scoped>
.banner {
  width: 100%;
  height: 100vh; /* ocupa toda a altura da tela */
  position: relative;
  top: 0; /* garante que fique no topo */
  left: 0;
  overflow: hidden;
}

.banner-image {
  width: 100%;
  height: 100%;
  object-fit: cover; /* cobre toda a área sem distorcer */
  display: block;
}

.banner-content {
  position: absolute;
  top: 50%; /* centraliza verticalmente */
  left: 50%; /* centraliza horizontalmente */
  transform: translate(-50%, -50%);
  color: white;
  font-size: 32px;
  font-weight: bold;
  text-align: center;
}
</style>