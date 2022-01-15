<template>
    <li>
        <a href="#">
            <img :src="src" alt="#">
            <span>
                {{text}}
            </span>
        </a>
    </li>
</template>

<script>
export default {
    name: 'Menu',
    props: {
        src:String,
        text:String,
    },
}
</script>

<style scoped lang='scss'>
@import "../../assets/scss/partials/_mixins.scss";
a {
    @include flex($ali:center);
    text-transform: uppercase;
    color: white;
    img {
        @include dim($h:60px);
    }
}
</style>