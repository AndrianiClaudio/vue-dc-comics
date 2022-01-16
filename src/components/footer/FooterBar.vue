<template>
<div class="container">
    <button>{{button.text}}</button>
    <nav>
        <ul>
            <li
            v-for="(linkTxt,index) in footerLinks.text"
            v-bind:key='linkTxt+index'
            >
                <a href="#">{{linkTxt}}</a>
            </li>
            <li
            v-for="(linkImg,index) in footerLinks.img"
            v-bind:key='linkImg+index'
            >
                <img
                :src="linkImg.src"
                :alt="linkImg.alt">
            </li>
        </ul>
    </nav>
</div>
</template>

<script>
export default {
    name:'FooterBar',
    data() {
        return {
            button: {
                text: 'SIGN-UP NOW'
            },
            footerLinks: {
                text: ['follow us'],
                img: [
                    {
                        src: require('../../assets/img/footer-facebook.png'),
                        alt: 'facebook',
                    },
                    {
                        src: require('../../assets/img/footer-twitter.png'),
                        alt: 'twitter',
                    },
                    {
                        src: require('../../assets/img/footer-youtube.png'),
                        alt: 'youtube',
                    },
                    {
                        src: require('../../assets/img/footer-pinterest.png'),
                        alt: 'pinterest',
                    },
                    {
                        src: require('../../assets/img/footer-periscope.png'),
                        alt: 'periscope',
                    },
                ]
            }
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/partials/_variables.scss";
@import "../../assets/scss/partials/_mixins.scss";

.container {
    @include flex($jus:space-between,$ali:center);
    button {
        @include dim($pad:1rem);
        @include text($tra:uppercase,$siz:1rem,$col:white);
        @include bgSet($col: $footerBarBgColor);
        border: 2px solid $headerActiveLinkColor;
        &:hover {
            cursor: pointer;
        }
    }
    ul {
        @include flex($ali:center,$gap:1.5rem);
        a {
            @include text($tra:uppercase,$siz: 1.25rem,$wei:bold,$col:$footerBarTextColor);
        }
    }
}
</style>