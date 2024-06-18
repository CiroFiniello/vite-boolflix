<script>
import { store } from '../store.js';
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <!-- <h2>
        Movies number : {{ Movies.length }}
    </h2> -->
<div class="container">
    <div class="row">
        <div class="form-floating mb-3 d-flex">
    <input type="text" class="form-control" id="floatingInput" placeholder="scrivi un titolo di un film">
    <label id="ktm" for="floatingInput">Scrivi un titolo</label>
    <button class="btn btn-primary">Cerca</button>
    </div>
    </div>
</div>
</template>

<style lang="scss" scoped>

#ktm{
    border: 1px solid white;
}

</style>