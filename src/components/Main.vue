<template>
    <main>
        <div id="jumbo">
            <div id="container">
                <h1> --> Content goes here </h1>
            </div>
        </div>
        <div id="menu">
            <div id="container">
                <ul>
                    <li>
                        <a href="#"><img src="../assets/img/buy-comics-digital-comics.png" alt="#"><span>Digital comics</span></a>

                    </li>
                    <li>
                        <a href="#"><img src="../assets/img/buy-comics-merchandise.png" alt="#"><span>DC merchandise</span></a>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/img/buy-comics-subscriptions.png" alt="#"><span>subscription</span></a>

                    </li>
                    <li>
                        <a href="#"><img src="../assets/img/buy-comics-shop-locator.png" alt="#"><span>comic shop locator</span></a>

                    </li>
                    <li>
                        <a href="#"><img src="../assets/img/buy-dc-power-visa.svg" alt="#"><span>dc power visa</span></a>

                    </li>
                </ul>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'Main',
    // data() {
    // }
}
    
</script>

<style scoped lang='scss'>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_mixins.scss";
main {
     min-width: 950px;
}
#jumbo {
    background-color: $jumboBgColor;
    height: 110px;
    @include flex($align:center);
    #container {
        color: white;
    }
}
#menu {
    background-color: $headerActiveLinkColor;
    @include flex($align:center);
    // display: flex;
    // align-items: center;
    min-height: 160px;
    ul {
        @include flex($justify:space-around);
        // display: flex;
        // justify-content: space-around;
        li {
            @include flex($align:center);
            // display: flex;
            // align-items: center;
            gap: 0.5rem;
            font-size: 0.85rem;
            color: white;
            text-transform: uppercase;
            img {
                // height: 50px;
                width: 50px;    
            }
            a {
                @include flex($align:center);
                gap: 0.5rem;
                color: white;
                &:visited {
                    color: inherit;
                }
            }
        }
    }
}
</style>