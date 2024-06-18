<script>
import MovieList from './MovieList.vue';
import axios from 'axios';
export default {
    components:{
        MovieList
    },
    data() {
        return 
            {
                Movies: [],
        }
    },
    methods:{
        getMovies(){
            axios.get('/user?ID=12345')
            .then(function (response) {
                // handle success
                console.log(response);
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            })
            .finally(function () {
                // always executed
            });
        }
    }
}
</script>

<template>

<MovieList/>

</template>


<style scoped>

</style>