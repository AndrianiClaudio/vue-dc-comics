<template>
    <footer>
        <div id="footer-main">
            <div class="container">
                <div class="col">
                    <h2>dc comics</h2>
                    <ul>
                        <li>
                            <a href="#">characters</a>
                        </li>
                        <li>
                            <a href="#">comics</a>
                        </li>
                        <li>
                            <a href="#">movies</a>
                        </li>
                        <li>
                            <a href="#">TV</a>
                        </li>
                        <li>
                            <a href="#">games</a>
                        </li>
                        <li>
                            <a href="#">videos</a>
                        </li>
                        <li>
                            <a href="#">news</a>
                        </li>
                    </ul>
                    <h2>shop</h2>
                    <ul>
                        <li>
                            <a href="#">Shop DC</a>
                        </li>
                        <li>
                            <a href="#">Shop DC Collectibles</a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h2>dc</h2>
                    <ul>
                        <li>
                            <a href="#">terms Of Use</a>
                        </li>
                        <li>
                            <a href="#">Privacy policy (news)</a>
                        </li>
                        <li>
                            <a href="#">ad Choices</a>
                        </li>
                        <li>
                            <a href="#">advertising</a>
                        </li>
                        <li>
                            <a href="#">jobs</a>
                        </li>
                        <li>
                            <a href="#">talent Workspace</a>
                        </li>
                        <li>
                            <a href="#">CPSC Certificates</a>
                        </li>
                        <li>
                            <a href="#">Ratings</a>
                        </li>
                        <li>
                            <a href="#">shop Help</a>
                        </li>
                        <li>
                            <a href="#">contact Us</a>
                        </li>
                    </ul>
                </div>
                <div class="col">

                    <h2>sites</h2>
                    <ul>
                        <li>
                            <a href="#">DC</a>
                        </li>
                        <li>
                            <a href="#">MAD Magazine</a>
                        </li>
                        <li>
                            <a href="#">DC Kids</a>
                        </li>
                        <li>
                            <a href="#">DC Universe</a>
                        </li>
                        <li>
                            <a href="#">DC Power Visa</a>
                        </li>
                    </ul>
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
}
    
</script>

<style scoped lang="scss">
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_mixins.scss";
#footer-main {
    @include flex ($jus:center);
    background-image: url('../assets/img/footer-bg.jpg');
    // @include dim($pt:3rem,$pb:3rem);
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