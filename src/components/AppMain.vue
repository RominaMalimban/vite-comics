<script>
export default {
    name: "AppMain",
}

</script>

<template>
    <main>
        <div class="container">
            Content goes here
        </div>

    </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

main {
    background-color: #1c1c1c;

    .container {
        color: $text-white;
        padding: 40px 0;
    }
}
</style>
