<template>
    <main>
        <div id="jumbo"></div>
        <div class="cards">
            <ul class="container">
                <Card
                    v-for="(card,index) in cards"
                    v-bind:key="card+index"
                    :thumb='card.thumb'
                    :series='card.series'
                />
            </ul>
        </div>
        <div id="menu">
            <ul class="container">
                <Menu 
                v-for="(item,index) in menu.items"
                v-bind:key='item+index'
                :src=item.src
                :text=item.text
                />
            </ul>
        </div>
    </main>
</template>

<script>
import Card from './main/Card.vue';
import Menu from './main/Menu.vue';

export default {
    name: 'Main',
    components: {
        Card,
        Menu,
    },
    data() {
        return {
            cards:[
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                "price": "$19.99",
                "series": "Action Comics",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                "price": "$3.99",
                "series": "American Vampire 1976",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                "price": "$16.99",
                "series": "Aquaman",
                "type": "graphic novel"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                "price": "$2.99",
                "series": "Batgirl",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                "price": "$3.99",
                "series": "Batman",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                "price": "$2.99",
                "series": "Batman Beyond",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                "price": "$3.99",
                "series": "Batman/Superman",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                "price": "$4.99",
                "series": "Batman/Superman Annual",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                "price": "$5.99",
                "series": "Batman: The Joker War Zone",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                "price": "$6.99",
                "series": "Batman: Three Jokers",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                "price": "$4.99",
                "series": "Batman: White Knight Presents: Harley Quinn",
                "type": "comic book"
            },
            {
                "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                "price": "$16.99",
                "series": "Catwoman",
                "type": "graphic novel"
            }
            ],
            menu: {
                items: [
                    {
                        src:require('../assets/img/buy-comics-digital-comics.png'),
                        text:'Digital comics'
                    },
                    {
                        src:require('../assets/img/buy-comics-merchandise.png'),
                        text:'DC merchandise'
                    },
                    {
                        src:require('../assets/img/buy-comics-subscriptions.png'),
                        text:'subscription'
                    },
                    {
                        src:require('../assets/img/buy-comics-shop-locator.png'),
                        text:'comic shop locator'
                    },
                    {
                        src:require('../assets/img/buy-dc-power-visa.svg'),
                        text:'dc power visa'
                    },
                ]
            }
        }
    },
}    
</script>

<style scoped lang='scss'>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_mixins.scss";
#jumbo {
    @include dim($h:350px);
    background-image: url('../assets/img/jumbotron.jpg');
    background-position: top;
    background-size: cover;
}
.cards {
    @include dim($w:100%,$pt:4rem,$pb:4rem);
    background-color: #25383f;
    .container {
        @include flex($wra:wrap,$gap:1rem);
    }
}
#menu {
    background-color: $headerActiveLinkColor;
    @include dim($pt:3rem,$pb:3rem);
    .container {
        @include flex($jus:center,$ali:center,$gap:1.5rem);
        // a {
        //     @include flex($ali:center);
        //     text-transform: uppercase;
        //     color: white;
        //     img {
        //         @include dim($h:60px);
        //     }
        // }
    }
}
</style>