<template>
    <nuxt-link :to="'jokes/'+id">
        <div class="card mb-3 mt-3">
            <div class="card-body">
                {{ joke }}
            </div>
        </div>
    </nuxt-link>
</template>

<script>
export default {
    name: 'Joke',
    props: ['joke', 'id'],
}
</script>

<style>

</style>