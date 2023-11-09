<template>
<main>
    <div class="container">
        <h2>=>Content goes here</h2>
    </div>
</main>
</template>

<script>
    export default {
        name: 'AppContent',
        
    }
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;

main{
    background-color: $black;
    height: 100px;

    h2{
        color: $white;
        padding-top: 35px;
    }
}

</style>