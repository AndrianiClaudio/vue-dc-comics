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
@import "../../assets/scss/partials/_variables.scss";
li{
    &:hover {
        span {
            @include text($dec:underline 1px solid white);
        }
    }
    a {
        @include flex($ali:center);
        @include text($tra:uppercase,$col:white);
        img {
            @include dim($h:$mainMenuImgHeight);
        }
    }
}
</style>