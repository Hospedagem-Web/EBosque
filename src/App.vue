<script setup lang="ts">

import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import Banner from './components/Banner.vue'

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.png" width="525" height="525" />
<!---
    <div>
      <div>
        <Banner src="assets/logo.png">

        </Banner>
      </div>  

    </div> 
-->
  </header>

  <main>
    <div class="wrapper">
      <HelloWorld msg="Portal EBosque" />
    </div>
    <TheWelcome />
  </main>
</template>
,

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
