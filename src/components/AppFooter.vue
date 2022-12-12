<script>
export default {
    name: "AppFooter",
    data() {
        return {
            // backGroundLogo: "img/dc-logo-bg.png",
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
            ],
            comics: [
                "Characters",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News"
            ],
            shops: [
                "Shop DC",
                "Shop DC Collectibles"
            ],
            DC: [
                "Terme of Use",
                "Privacy Policy (New)",
                "Ad Choices",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshop",
                "CPCS Certificates",
                "Ratings",
                "Shop Help",
                "Contact us"
            ],
            sites: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ],
            socials: [
                "img/footer-facebook.png",
                "img/footer-twitter.png",
                "img/footer-youtube.png",
                "img/footer-pinterest.png",
                "img/footer-periscope.png"
            ]
        }
    }

}
</script>

<template>
    <footer>
        <!-- section 1 -->
        <section class="merchandise">
            <ul class="container">
                <li v-for="item in items">
                    <img :src="item.img" alt="">
                    <a :href="item.url">{{ item.text }}</a>
                </li>
            </ul>
        </section>

        <!-- section 2 -->
        <section class="links">
            <div class="container">
                <div class="col">
                    <h3>DC COMICS</h3>
                    <ul>
                        <li v-for="comic in comics">
                            <a href="#">{{ comic }}</a>
                        </li>
                    </ul>

                    <h3>SHOP</h3>
                    <ul>
                        <li v-for="shop in shops">
                            <a href="#">{{ shop }}</a>
                        </li>
                    </ul>
                </div>

                <div class="col center">
                    <h3>DC</h3>
                    <ul>
                        <li v-for="link in DC">
                            <a href="#">{{ link }}</a>
                        </li>
                    </ul>
                </div>

                <div class="col">
                    <h3>SITES</h3>
                    <ul>
                        <li v-for="site in sites">
                            <a href="#"> {{ site }}</a>
                        </li>
                    </ul>
                </div>

                <div class="bg-logo">
                </div>

            </div>

        </section>

        <!-- section 3 -->
        <section class="sub-footer">

            <div class="container">

                <!-- button -->
                <a class="sign-up">SIGN-UP NOW!</a>

                <!-- social -->
                <div class="social">
                    <span>FOLLOW US</span>
                    <ul>
                        <li v-for="social in socials">
                            <img :src="social" alt="">
                        </li>
                    </ul>
                </div>
            </div>

        </section>
    </footer>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

footer {

    // SECTION 1 
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

    // SECTION 2 
    .links {
        background-image: url(../../public/img/footer-bg.jpg);
        background-size: cover;
        color: $text-white;

        .container {
            display: flex;
            position: relative;

            .col {
                padding: 40px 0;

                &.center {
                    padding: 40px 25px;
                }

                h3 {
                    margin: 15px 0;
                }

                ul li a {
                    color: #797979;
                    font-size: $font-small;
                }
            }

            .bg-logo {
                width: 100%;
                height: 100%;
                position: absolute;
                background-image: url(../../public/img/dc-logo-bg.png);
                background-repeat: no-repeat;
                right: -250px;
                background-position: 50%;
            }
        }


    }

    // SECTION 3
    .sub-footer {
        height: 90px;
        background-color: #303030;

        .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 100%;

            .sign-up {
                color: #fff;
                padding: 10px;
                border: 2px solid $primary;
            }

            .social {
                display: flex;
                align-items: center;

                ul {
                    display: flex;
                    align-items: center;

                    li {
                        padding: 0 10px;
                    }
                }

                span {
                    color: $primary;
                }
            }
        }
    }
}
</style>
