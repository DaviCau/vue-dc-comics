<template>
    <div class="footer">
        <div class="footer-top">
            <div class="container footer-container">
                <div class="links">
                    <ul v-for="(section, index) in footerLinks" :key="index">
                        <li class="list-title">{{section.sectionTitle}}</li>
                        <li v-for="(link, indexLink) in footerLinks[index].sectionLinks" :key="indexLink">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="logo-bg">
                    <img src="../assets/img/dc-logo-bg.png" alt="logo dc">
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container footer-container">
                <div class="sign-up">
                    <button>Sign-up now&excl;</button>
                </div>
                <div class="socials">
                    <ul class="social-links">
                        <li class="list-title">Follow Us</li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-facebook.png" alt="facebook">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-twitter.png" alt="twitter">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-youtube.png" alt="youtube">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-pinterest.png" alt="pinterest">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-periscope.png" alt="periscope">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer",
    data: function() {
        return {
            footerLinks: [
                {
                    sectionTitle: "DC COMICS",
                    sectionLinks: [
                        {
                            text: "Characters",
                            url: "#"
                        },
                        {
                            text: "Comics",
                            url: "#"
                        },
                        {
                            text: "Movies",
                            url: "#"
                        },
                        {
                            text: "TV",
                            url: "#"
                        },
                        {
                            text: "Games",
                            url: "#"
                        },
                        {
                            text: "Videos",
                            url: "#"
                        },
                        {
                            text: "News",
                            url: "#"
                        }
                    ]
                },
                {
                    sectionTitle: "SHOP",
                    sectionLinks: [
                        {
                            text: "Shop DC",
                            url: "#"
                        },
                        {
                            text: "CoShop DC Collectibles",
                            url: "#"
                        }
                    ]
                },
                {
                    sectionTitle: "DC",
                    sectionLinks: [
                        {
                            text: "Terms Of Use",
                            url: "#"
                        },
                        {
                            text: "Privacy policy (New)",
                            url: "#"
                        },
                        {
                            text: "Ad Choices",
                            url: "#"
                        },
                        {
                            text: "Advertising",
                            url: "#"
                        },
                        {
                            text: "Jobs",
                            url: "#"
                        },
                        {
                            text: "Subscriptions",
                            url: "#"
                        },
                        {
                            text: "Talent Workshops",
                            url: "#"
                        },
                        {
                            text: "CPSC Certificates",
                            url: "#"
                        },
                        {
                            text: "Ratings",
                            url: "#"
                        },
                        {
                            text: "Shop Help",
                            url: "#"
                        },
                        {
                            text: "Contact Us",
                            url: "#"
                        }
                    ]
                },
                {
                    sectionTitle: "SITES",
                    sectionLinks: [
                        {
                            text: "DC",
                            url: "#"
                        },
                        {
                            text: "MAD Magazine",
                            url: "#"
                        },
                        {
                            text: "DC Kids",
                            url: "#"
                        },
                        {
                            text: "DC Universe",
                            url: "#"
                        },
                        {
                            text: "DC Power Visa",
                            url: "#"
                        },
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .footer-container {
        display: flex;
        justify-content: space-between;
    }

    .footer-top {
        background-image: url("../assets/img/footer-bg.jpg");
        background-size: cover;
        height: 370px;
        overflow: hidden;
    }

    .links {
        height: 370px;
        margin: 35px 0 50px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;

        ul {
            list-style: none;
            margin-right: 50px;
            .list-title {
                color: white;
                font-weight: bold;
                font-size: 20px;
                padding: 20px 0 15px;
            }
            a {
                color: lightgray;
                text-decoration: none;
                font-size: 12px;

                &:hover {
                    text-decoration: underline;
                }
            }
        }
    }

    .logo-bg {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 370px;
    }

    .footer-bottom {
        background-color: #303030;
        padding: 30px;
    }

    .sign-up button {
        background-color: transparent;
        padding: 15px;
        border: solid 3px #0282f3;
        color: white;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 16px;
    }

    .socials {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        width: 30%;

        .social-links {
            width: 100%;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;

            .list-title {
                color: #0282f3;
                font-size: 20px;
                font-weight: bold;
                text-transform: uppercase;
            }
        }
    }
</style>