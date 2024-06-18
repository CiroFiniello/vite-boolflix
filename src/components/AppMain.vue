<!-- <script>
import MovieList from './MovieList.vue';
import axios from 'axios';
import { store } from '../store.js'
import AppSearch from './AppSearch.vue';

export default {
    components: {
        MovieList,
    },
    data() {
        return {
            Movies: [],
            store,
        }
    },
    methods: {
        getMovies() {
            axios.get('https://api.themoviedb.org/3/search/movie?api_key=f4f72d664eb55cb17ecad03ef50cc067&query=ritorno+al+futuro')
            .then((response) => {
                // handle success
                console.log(response.data.results);
                this.Movies = response.data.results;
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            })
            .finally(function () {
                // always executed
            });
        }
    },
    created(){
        this.getMovies();
    }
}
</script>

<template>


<AppSearch/>
<MovieList/>

<ul>
    <li v-for="Movies in store.Movies">
        titolo:  {{ Movies.title}}
        <p>
            titolo originale:
            {{ Movies.original_title }}  
        </p>
        <p>
            Lingua:
            {{ Movies.original_language }}
        </p> 
        <p>
            Voto:
            {{ Movies.vote_average}}
        </p>
    </li>
</ul>
<!-- <MovieList :Movies="MovieList"/> -->
<!-- 
</template>


<style lang="scss" scoped>

li{
    color: white;
}
</style> --> 



<script>
import MovieList from './MovieList.vue';
import axios from 'axios';
// import { store } from '../store.js'
import AppSearch from './AppSearch.vue';

export default {
    components: {
        MovieList,
        AppSearch,
    },
    data() {
        return {
            Movies: [],
        }
    }
}
</script>

<template>

<AppSearch/>
<MovieList/>

</template>

<style lang="scss">
li{
    color: white;
}

</style>