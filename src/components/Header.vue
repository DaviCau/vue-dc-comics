<template>
  <div class="header">
      <img src="../assets/img/dc-logo.png" alt="logo dc">

      <div class="nav">
          <ul>
              <li v-for="(link, index) in links" :key=index>
                  <a href="link.url" :class="link.current ? 'active' : ''">{{link.text}}</a>
              </li>
          </ul>
      </div>
  </div>
</template>

<script>
export default {
    name: "Header",
    data: function() {
        return {
            links: [
                {
                    text: "Characters",
                    url: "#",
                    current: false
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false
                },
                {
                    text: "Tv",
                    url: "#",
                    current: false
                },
                {
                    text: "Games",
                    url: "#",
                    current: false
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false
                },
                {
                    text: "News",
                    url: "#",
                    current: false
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 130px;
    }

    img {
        height: 80px;
    }

    ul {
        list-style: none;
        display: flex;
        justify-content: flex-end;

        li {
            margin: 0 15px;

            a {
                height: 130px;
                text-decoration: none;
                text-transform: uppercase;
                font-weight: bold;
                color: #1c1c1c;
                border-top: solid 5px transparent;
                border-bottom: solid 5px transparent;
                display: flex;
                justify-content: center;
                align-items: center;

                &:hover {
                    color: #0282f9;
                    border-bottom: solid 5px #0282f9;
                }
            }
        }
    }

    .active {
        color: #0282f9;
        border-bottom: solid 5px #0282f9;
    }
</style>