<script>
export default {
    name: "Card",
    props: {
        thumb: Object
    }
}

</script>

<template>

    <!-- card -->
    <div class="card">
        <div>
            <img :src="thumb.thumb" :alt="thumb.series">
        </div>
        <h4>{{ thumb.series }}</h4>
    </div>

</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 30px);
    margin: 20px 15px;

    h4 {
        margin-top: 10px;
    }
}
</style>
