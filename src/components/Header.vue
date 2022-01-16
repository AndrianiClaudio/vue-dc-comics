<template>
    <header>
        <div class="container">
            <img :src='logo.src' :alt='logo.alt' class="logo">
            <ul>
                <Item 
                v-for="(item,index) in menu.items"
                v-bind:key="item+index"
                :item="item"
                :active='index == menu.activeIndex'
                @click.native="activeItem(index)"
                />
            </ul>
        </div>
    </header>
</template>

<script>
import Item from './header/Item.vue';
export default {
    name: 'Header',
    components: {
        Item,
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
@import "../assets/scss/partials/_variables.scss";
header {
    @include flex($ali:center);
    @include dim($h:$headerHeight);
    .container {
        @include flex($ali:center,$jus:space-between);
        img.logo {
            @include dim($h:$headerLogoDim);
        }
        ul {
            @include flex();
        }
    }
}
</style>