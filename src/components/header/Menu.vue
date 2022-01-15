<template>
<li>
    <a href="#" :class="(active) ? 'active' : ''">
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
    methods: {
        
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/partials/_variables.scss";
@import "../../assets/scss/partials/_mixins.scss";
li {
    a {
        @include flex($ali:center);
        @include dim($h:100px);
        text-transform: uppercase;
        color: black;
        &.active {
            background: linear-gradient(to bottom, white 95%, $headerActiveLinkColor 5%);
        }
    }
}
</style>