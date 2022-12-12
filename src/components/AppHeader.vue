<script>
export default {
    name: "AppHeader",
    data() {
        return {
            logo: "img/dc-logo.png",
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false
                },
            ]
        }
    }
}

</script>

<template>

    <header>
        <div class="container">

            <a href="#">
                <img :src="logo" alt="logo">
            </a>

            <nav>
                <ul>
                    <li v-for="link in links"><a href="#">{{ link.text }}</a></li>
                </ul>
            </nav>
        </div>

    </header>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

header {
    height: 95px;
    padding: 10px 0;
    // debug
    border: 1px solid black;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    img {
        height: 65px;
    }

    ul {
        list-style: none;
        height: 100%;
        display: flex;

        li a {
            text-decoration: none;
            padding: 0 10px;
            font-size: 13px;
            color: $text-nav;

            &.active {
                border-bottom: 1px solid #0282f9;
            }
        }
    }
}
</style>
