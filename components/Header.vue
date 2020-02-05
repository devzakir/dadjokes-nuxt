<template>
    <header>
        <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
            
            <div class="container">
                <nuxt-link class="navbar-brand" to="/">Dad Jokes</nuxt-link>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
                    aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>

                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav ml-auto">
                        <li class="nav-item active">
                            <nuxt-link class="nav-link" to="/">Home </nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link class="nav-link" to="/about">About</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link class="nav-link" to="/jokes">Jokes</nuxt-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>

<script>
  export default {

  }
</script>

<style>

</style>