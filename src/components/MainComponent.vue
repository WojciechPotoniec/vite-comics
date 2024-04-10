<template>
    <main>
        <div class="container">
            <h2 class="text-light">Content goes here</h2>
        </div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent',
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