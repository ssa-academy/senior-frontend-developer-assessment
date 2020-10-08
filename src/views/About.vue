<template>
  <div class="about">
    <h1 v-text="'About Page'"></h1>

    <HelloWorld />
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  components: {
    HelloWorld
  }
}
</script>
