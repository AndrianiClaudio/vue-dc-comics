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
    @include flex($dir:column,$gap:1rem,$bas:$cardWidth);
    img{
        height: 150px;
        width: 150px;
        max-height: 400px;
        max-width: 400px;
    }
    .series {
        @include text($siz: .85rem,$tra:uppercase,$col:white);
    }
}
</style>