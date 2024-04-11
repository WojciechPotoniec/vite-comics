<template>
    <main>
        <div class="container">
            <h2 class="text-light">Content goes here</h2>
        </div>
    </main>
</template>

<script>
import {comics} from '../data/data.js'
    export default {
        name: 'MainComponent',
        data(){
            return{
                comics: comics
            }
        }
    }
</script>

<style lang="scss" scoped>
@use "./src/assets/styles/partials/variables" as *;
main{
  background-color: $bg-color-main;
  padding: 40px 0;
}
h2{
    margin: 0;
}
</style>