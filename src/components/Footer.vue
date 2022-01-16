<template>
    <footer>
        <div id="footer-main">
            <div class="container">
                <FooterMain 
                v-for="(col,index) in cols"
                v-bind:key="col+index"
                :col='col'
                />
            </div>
        </div>
        <div id='footer-bar'>
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
        </div>
    </footer>
</template>

<script>
import FooterMain from './footer/FooterMain.vue';
export default {
    name: 'Footer',
    components: {
        FooterMain,
        // FooterBar
    },
    data() {
        return {
            cols: [
                {
                    title: ['dc comics','shop'],
                    items: [['characters','comics','movies','TV','games','videos','news'],['shop DC','shop dc collctibles']],
                },
                {
                    title: ['dc'],
                    items: [['terms of use','Privacy policy (news)','ad Choices','advertising','jobs','talent Workspace','CPSC Certificates','Ratings','shop Help','contact Us']],
                },
                {
                    title: ['sites'],
                    items: [['DC','MAD magazine','DC kids','DC Universe','DC Power Visa']],
                },
            ],
            button: {
                text: 'SIGN-UP NOW'
            },
            footerLinks: {
                text: ['follow us'],
                img: [
                    {
                        src: require('../assets/img/footer-facebook.png'),
                        alt: 'facebook',
                    },
                    {
                        src: require('../assets/img/footer-twitter.png'),
                        alt: 'twitter',
                    },
                    {
                        src: require('../assets/img/footer-youtube.png'),
                        alt: 'youtube',
                    },
                    {
                        src: require('../assets/img/footer-pinterest.png'),
                        alt: 'pinterest',
                    },
                    {
                        src: require('../assets/img/footer-periscope.png'),
                        alt: 'periscope',
                    },
                ]
            }
        }
    }
}

</script>

<style scoped lang="scss">
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_mixins.scss";
#footer-main {
    @include flex ($jus:center);
    @include bgSet($url: '../assets/img/footer-bg.jpg');
    .container {
        @include flex ($gap:2.5rem);
        @include dim($w:$containerDefaultWidth,$pad:2.5rem 0);
        @include bgSet($url: '../assets/img/dc-logo-bg.png',$siz:null,$rep: no-repeat,$pos:right);
    }
}
#footer-bar {
    @include flex();
    @include bgSet($col: $footerBarBgColor);
    @include dim($h:$footerBarHeight);
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
}
</style>