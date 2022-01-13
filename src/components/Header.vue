<template>
    <header>
        <div id="container">
            <img src='../assets/dc-logo.png' :alt='logo.alt' class="logo">
            <nav>
                <ul>
                    <li class="active">
                        <a href="#">
                            characters
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            comics
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            movies
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            tv
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            games
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            collectibles
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            videos
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            fans
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            news
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            shop
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            logo: {
                // src: '../assets/dc-logo.png',
                alt: 'logo DC'
            }
        }
    }
}
</script>
<style scoped lang = 'scss'>
header {
    display: flex;
    align-items: center;
    height: 100px;
    #container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        img.logo {
            height: 70px;
        }
        li {
            display: inline;
            text-transform: uppercase;
            padding: 0.5rem;
            a {
                text-decoration: none;
                color: black;
            }
        }
    & .active {
        border-bottom: 5px solid aqua;
    }
    }
}

</style>