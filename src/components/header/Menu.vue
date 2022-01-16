<template>
    <li>
        <a href="#" :class="{active:active}">
            {{item}}
        </a>
    </li>
</template>

<script>
export default {
    name:'Items',
    props: {
        item:String,
        active:Boolean,
    },
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/partials/_variables.scss";
@import "../../assets/scss/partials/_mixins.scss";
li {
    a {
        @include flex($ali:center);
        @include dim($h:$headerHeight);
        @include text($tra: uppercase,$col:black);
        &.active {
            background: linear-gradient(to bottom, $headerBgColor calc(100% - $headerActiveLinkBorderDim), $headerActiveLinkColor $headerActiveLinkBorderDim);
        }
    }
}
</style>