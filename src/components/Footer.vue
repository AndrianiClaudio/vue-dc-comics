<template>
    <footer>
        <div id="footer-main">
            <div class="container">
                <div 
                v-for='(col,index) in cols' 
                v-bind:key='index'
                class="col"
                >
                    <div v-for="(title,index) in col.title"
                    v-bind:key='index'
                    >
                        <h2>{{title}}</h2>
                        <ul>
                            <li
                            v-for="(item,index) in col.items[index]"
                            v-bind:key='index'
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
                <button>SIGN-UP NOW</button>
                <nav>
                    <ul>
                        <li>
                            <a href="#">FOLLOW US</a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-facebook.png" alt=""></a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-twitter.png" alt=""></a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-youtube.png" alt=""></a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-pinterest.png" alt=""></a>
                        </li>
                        <li>
                            <a href="#"><img src="../assets/img/footer-periscope.png" alt=""></a>
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
                font-size: 1.25rem;
                font-weight: bold;
                color: #0282f9;
            }
        }
    }
}
</style>