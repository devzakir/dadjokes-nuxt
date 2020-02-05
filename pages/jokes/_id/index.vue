<template>
  <div class="row">
      <div class="col-12">
          <div class="card mt-5 mb-3">
              <div class="card-header d-flex justify-content-between align-items-center">
                  <p class="mb-0">Joke ID: {{ joke.id }}</p>
                  <nuxt-link to="/jokes" class="btn btn-primary">Back to Jokes</nuxt-link>
              </div>
              <div class="card-body">
                  <h2>{{ joke.joke }}</h2>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
    import axios from 'axios';

    export default {
        data(){
            return {
                joke: {}
            }
        },

        created(){
            let thisData = this;
            const config = {
                headers: {
                    Accept: 'application/json',
                }
            }

            axios.get(`https://icanhazdadjoke.com/j/${thisData.$route.params.id}`, config)
            .then(success => {
                thisData.joke = success.data;
            })
            .catch(error => {
                console.log(error);
            });
        },
        
        head(){
            return {
                title: this.joke.joke,
                meta: [
                    {
                        name: 'description',
                        content: 'best place for corny dad jokes',
                    },
                    
                ]
            }
        },
    }
</script>

<style>

</style>