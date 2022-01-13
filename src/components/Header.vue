<template>
    <header>
        <img src='../assets/dc-logo.png' alt='Logo DC' class="logo">
        <nav>
            <ul>
                <li>
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
    </header>
</template>

<script>
export default ({
    name: 'Header',
    data() {
        return {
        }
    }
})
</script>

<style scoped lang = 'scss'>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        img.logo {
            height: 60px;
        }
        li {
            display: inline;
            list-style: none;
            text-transform: uppercase;
            a {
                text-decoration: none;
                color: black;
            }
        }
    }
</style>