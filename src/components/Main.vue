<template>
    <div class="main">
        <div class="jumbotron"></div>
        <div class="main-content">
            <div class="container">
                <div class="comics-container">
                    <h2>CURRENT SERIES</h2>
                    <Card 
                        v-for="(element, index) in elements"
                        :key="index"
                        :single-comic="element"
                    />
                </div>
                <div class="load-more">
                    <button>LOAD MORE</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Card from "./Card.vue"
import comics from "../data/comics"

export default {
    name: "Main",
    components: {
        Card
    },
    data: function() {
        return {
            elements: comics
        }
    }
}
</script>

<style lang="scss" scoped>
    .jumbotron {
        height: 400px;
        background-image: url("../assets/img/jumbotron.jpg");
    }

    .main-content {
        background-color: #1c1c1c;
        color: white;

        .load-more {
            display: flex;
            justify-content: center;
            padding-bottom: 25px;

            button {
                padding: 10px 50px;
                color: white;
                font-weight: bold;
                font-size: 14px;
                background-color: #0282f9;
                border: transparent;
            }
        }

        .comics-container {
            position: relative;
            padding-top: 50px;
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        
            h2 {
                position: absolute;
                top: 0;
                left: 0;
                transform: translateY(-50%);
                padding: 10px 25px;
                font-size: 30px;
                background-color: #0282f9;
            }
        }
    }
</style>