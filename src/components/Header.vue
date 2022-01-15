<template>
    <header>
        <div class="container">
            <img :src='logo.src' :alt='logo.alt' class="logo">
            <ul>
                <Menu 
                v-for="(item,index) in menu.items" v-bind:key="index"
                :item="item"
                :active='index == menu.activeIndex'
                @click.native="activeItem(index)"
                />
            </ul>
        </div>
    </header>
</template>

<script>
import Menu from './header/Menu.vue';
export default {
    name: 'Header',
    components: {
        Menu,
    },
    data() {
        return {
            logo: {
                src: require('../assets/img/dc-logo.png'),
                alt: 'logo DC comics.'
            },
            menu: {
                activeIndex: 1,
                items: [
                    'characters',
                    'comics',
                    'movies',
                    'TV',
                    'games',
                    'collectibles',
                    'videos',
                    'fans',
                    'news',
                    'shop',
                ],
            },
        }
    },
    methods: {
        activeItem(index) {
            this.menu.activeIndex = index;
        },
    }
}
</script>
<style scoped lang = 'scss'>
@import "../assets/scss/partials/_mixins.scss";
header {
    @include flex($ali:center);
    @include dim($h:100px);
    .container {
        @include flex($ali:center,$jus:space-between);
        img.logo {
            @include dim($h:70px);
        }
        ul {
            @include flex();
        }
    }
}
</style>