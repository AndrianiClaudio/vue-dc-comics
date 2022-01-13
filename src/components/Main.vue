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
                        <a href="#"><img src="../assets/buy-comics-digital-comics.png" alt="#"></a>
                        <span>Digital comics</span>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/buy-comics-merchandise.png" alt="#"></a>
                        <span>DC merchandise</span>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/buy-comics-subscriptions.png" alt="#"></a>
                        <span>subscription</span>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/buy-comics-shop-locator.png" alt="#"></a>
                        <span>comic shop locator</span>
                    </li>
                    <li>
                        <a href="#"><img src="../assets/buy-dc-power-visa.svg" alt="#"></a>
                        <span>dc power visa</span>
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
#jumbo {
    background-color: black;
    display: flex;
    align-items: center;
    height: 130px;
    #container {
        color: white;
    }
}
#menu {
    background-color: blue;
    display: flex;
    align-items: center;
    min-height: 160px;
    ul {
        display: flex;
        justify-content: space-around;
        li {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-size: 0.85rem;
            color: white;
            text-transform: uppercase;
            img {
                // height: 50px;
                width: 50px;    
            }
        }
    }
}
</style>