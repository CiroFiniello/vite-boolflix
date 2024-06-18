<script>

export default {
    props: {
        Movies: {
        type: Array,
        required: true
        }
    }
}
</script>

<template>
<h1>Movie comp</h1>
<ul>
        <li v-for="movie in Movies" :key="movie.id">
        <p>titolo: {{ movie.title }}</p>
        <p>titolo originale: {{ movie.original_title }}</p>
        <p>Lingua: {{ movie.original_language }}</p>
        <p>Voto: {{ movie.vote_average }}</p>
        </li>
    </ul>
</template>

<style scoped>
li {
    color: white;
    list-style-type: none;
    border: 1px solid orange;
    padding: 1rem;
}
ul{
    display: flex;
    padding: 2rem;

}
</style>