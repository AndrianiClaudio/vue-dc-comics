<template>
    <footer>
        <div id="footer-main">
            <div class="container">
                <div 
                v-for='(col,index) in cols' 
                v-bind:key='col+index'
                class="col"
                >
                    <div v-for="(title,index) in col.title"
                    v-bind:key='title+index'
                    >
                        <h2>{{title}}</h2>
                        <ul>
                            <li
                            v-for="(item,index) in col.items[index]"
                            v-bind:key='item+index'
                            >
                                <a href="#">{{item}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
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
export default {
    name: 'Footer',
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
    background-image: url('../assets/img/footer-bg.jpg');
    .container {
        @include flex ($gap:2.5rem);
        @include dim($w:$containerDefaultWidth,$pt:2.5rem,$pb:2.5rem);
        background-image: url('../assets/img/dc-logo-bg.png');
        background-repeat: no-repeat;
        background-position: right;
        .col {
            h2 {
                text-transform: uppercase;
                color:white;
            }
            ul {
                @include dim($pb:1.5rem);
                a {
                    color: grey;
                    text-transform: capitalize;
                }
            }
        }
    }
}
#footer-bar {
    @include flex();
    background-color: $footerBarBgColor;
    @include dim($h:100px);
    .container {
        @include flex($jus:space-between,$ali:center);
        button {
            @include dim($pad:1rem);
            text-transform: uppercase;
            font-size: 1rem;
            border: 2px solid $headerActiveLinkColor;
            background-color: $footerBarBgColor;
            color: white;
            &:hover {
                cursor: pointer;
            }
        }
        ul {
            @include flex($ali:center);
            gap: 1.5rem;
            a {
                text-transform: uppercase;
                font-size: 1.25rem;
                font-weight: bold;
                color: #0282f9;
            }
        }
    }
}
</style>