<template>
  <div>
    <Header></Header>
    <div class="container">
      <nuxt />
    </div>
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
export default {
    components: {
      Header,
    }
}
</script>

<style>

</style>
