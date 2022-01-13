<template>
    <footer>
        <div id="footer-main">
            <div id="container">
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
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat omnis fugiat nihil, ullam iure vel accusantium, voluptatibus aliquam mollitia animi, harum facere! Magni hic veritatis porro ad numquam dolorum nam.
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    // data() {
    // }
}
    
</script>

<style scoped lang="scss">
#footer-main {
    background-image: url('../assets/footer-bg.jpg');
    #container {
        background-image: url('../assets/dc-logo-bg.png');
        background-position: right;
        background-repeat: no-repeat;
        display: flex;
        gap: 1.5rem;
        h2 {
            text-transform: uppercase;
            margin: 1rem 0;
        }
        a {
            text-transform: capitalize;
            color: grey;
        }
    }
}
#footer-bar {
    background-color: grey;
}
</style>