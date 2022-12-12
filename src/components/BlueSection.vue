<script>
export default {
    name: "BlueSection",
    data() {
        return {
            items: [
                {
                    img: "/img/buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS",
                    url: "#"
                },
                {
                    img: "/img/buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url: "#"
                },
                {
                    img: "/img/buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url: "#"
                },
                {
                    img: "/img/buy-comics-shop-locator.png",
                    text: "COMIC CHOP LOCATOR",
                    url: "#"
                },
                {
                    img: "/img/buy-dc-power-visa.svg",
                    text: "DC POWER VISA",
                    url: "#"
                }
            ]
        }
    }
}

</script>

<template>
    <section class="merchandise">
        <ul class="container">
            <li v-for="item in items">
                <img :src="item.img" alt="">
                <a :href="item.url">{{ item.text }}</a>
            </li>
        </ul>
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.merchandise {
    background-color: $primary;
    height: 125px;

    .container {
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px 40px;

        li {
            display: flex;
            align-items: center;
            padding-inline: 10px;
        }

        a {
            padding-left: 5px;
            font-size: $font-medium;
            color: $text-white;
        }

        img {
            height: 50px;
        }
    }
}
</style>