<template>
    <div class="main">
        <div class="jumbotron"></div>
        <div class="main-content">
            <div class="container">
                <h2>CURRENT SERIES</h2>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Main"
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

        .container {
            position: relative;
            padding: 50px 0;
        
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