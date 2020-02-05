<template>
  <div>
        <div class="row">
            <div class="col-12">
                <Joke v-for="joke in jokes" :key="joke.id" :joke="joke.joke" :id="joke.id"></Joke>
            </div>
        </div>
  </div>
</template>

<script>
import axios from 'axios';
import Joke from '~/components/Joke.vue';
export default {
    components: {
        Joke
    },
    head(){
        return {
            title: 'Dad Jokes',
            meta: [
                {
                    name: 'description',
                    content: 'best place for corny dad jokes',
                },
                
            ]
        }
    },

    data(){
        return {
            jokes: [],
        }
    },

    async created(){
        const config = {
            headers: {
                Accept: 'application/json',
            }
        }

        try {
            const res = await axios.get('https://icanhazdadjoke.com/search', config);
            
            this.jokes = res.data.results;
            
        } catch(error){
            console.log(error);
        }
    }
}
</script>

<style>

</style>