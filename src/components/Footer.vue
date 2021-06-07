<template>
    <div class="footer">
        <div class="footer-top">
            <div class="container">
                <div class="links">

                </div>
                <div class="logo-bg">
                    <img src="../assets/img/dc-logo-bg.png" alt="logo dc">
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <div class="sign-up">
                    <button>Sign-up now&excl;</button>
                    <div class="socials">
                        <!-- <ul class="social-links">
                            <li>Follow Us</li>
                            <li v-for="(social, index) in socials" :key=index>
                                <a :href="social.url">
                                    <img :src="'../assets/img/footer-'+ social.socialName +'.png'" :alt="social.text">
                                </a>
                            </li>
                        </ul> -->
                    </div>
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
            socials: [
                {
                    socialName: "facebook",
                    url: "#",
                },
                {
                    socialName: "twitter",
                    url: "#",
                },
                {
                    socialName: "youtube",
                    url: "#",
                },
                {
                    socialName: "pinterest",
                    url: "#",
                },
                {
                    socialName: "periscope",
                    url: "#",
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .container {
        width: 70%;
        margin: auto;
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
        margin: 35px 0 50px;
        display: flex;
        flex-direction: column;
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
        display: flex;
        justify-content: space-between;
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
</style>