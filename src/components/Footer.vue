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
            <FooterBar />
        </div>
    </footer>
</template>

<script>
import FooterMain from './footer/FooterMain.vue';
import FooterBar from './footer/FooterBar.vue';
export default {
    name: 'Footer',
    components: {
        FooterMain,
        FooterBar
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
}
</style>