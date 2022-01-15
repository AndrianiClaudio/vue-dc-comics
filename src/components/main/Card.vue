<template>
<li class="card">
    <img :src="thumb" alt="#">
    <strong class="series">{{series}}</strong>
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
.card {
    @include flex($dir:column,$gap:1rem);
    flex-basis: calc((100% / 6) - 1rem);
    .series {
        text-transform: uppercase;
        color: white;
        font-size: .85rem;
    }
}
</style>