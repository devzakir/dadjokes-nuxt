<template>
  <div class="row">
    <div class="col-12 text-center pt-5 pb-5">
      <h1 class="mb-5">Welcome to best corny dad jokes app on the web</h1>
      <nuxt-link to="/about" class="btn btn-primary">About the App</nuxt-link>
      <nuxt-link to="/jokes" class="btn btn-warning"> Browse Jokes</nuxt-link>
    </div>
  </div>
</template>

<script>

export default {
  head(){
      return {
          title: 'Home',
          meta: [
              {
                  name: 'description',
                  content: 'best place for corny dad jokes',
              },
              
          ]
      }
  },
  components: {

  },
}
</script>

<style>
</style>
