<script>
export default {
    name: "AppJumbo",
    data() {
        return {
            jumbo: "/img/jumbotron.jpg"
        }
    }
}

</script>

<template>
    <section>
        <img :src="jumbo" alt="">
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

section img {
    object-fit: cover;
    object-position: 20% 0;
    height: 400px;
    width: 100%;
}
</style>