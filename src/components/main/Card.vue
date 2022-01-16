<template>
    <li class="card">
        <img :src="thumb" alt="#">
        <strong class="series">
            {{series}}
        </strong>
    </li>
</template>

<script>
export default {
    name: 'Card',
    props: {
        thumb:String,
        series:String,
    },
}
</script>

<style scoped lang='scss'>
@import "../../assets/scss/partials/_mixins.scss";
@import "../../assets/scss/partials/_variables.scss";
.card {
    @include flex($dir:column,$gap:1rem,$bas:$cardWidth,$ali:center);
    &:hover {
        cursor: pointer;
        .series {
            @include text($dec:underline 1px solid white,$siz:null);
        }
    }
    img{
        @include dim($h: $cardDim,$w:$cardDim);
    }
    .series {
        @include text($siz: .85rem,$tra:uppercase,$col:white,$ali:center);
    }
}
</style>