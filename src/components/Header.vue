<template>
    <header>
        <div id="container">
            <img src='../assets/img/dc-logo.png' :alt='logo.alt' class="logo">
            <nav>
                <ul>
                    <li>
                        <a href="#">
                            characters
                        </a>
                    </li>
                    <li>
                        <a href="#" class="active">
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
                // src: '../assets/img/dc-logo.png',
                alt: 'logo DC'
            }
        }
    }
}
</script>
<style scoped lang = 'scss'>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_mixins.scss";
header {
    @include flex('',center);
    height: 100px;
    min-width: 850px;
    #container {
        @include flex(space-between,center);
        /* display: flex;
        align-items: center;
        justify-content: space-between; */
        img.logo {
            height: 70px;
        }
        ul {
            /* display: flex; */
            @include flex();
            li {
                @include flex($align:center);
                /* display: flex;
                align-items: center; */
                text-transform: uppercase;
                height: 100px;
                padding: 0.5rem;
                a {
                    @include flex($align:center);
                    /* display: flex;
                    align-items: center; */
                    height: 100px;
                    color: black;
                    border-bottom: 5px solid white;
                    font-weight: bold;
                    &.active {
                        color: $headerActiveLinkColor;
                        border-bottom: 5px solid $headerActiveLinkColor;
                        /* border-bottom: 5px solid aqua; */
                    }
                }
            }
        }
    }
}

</style>