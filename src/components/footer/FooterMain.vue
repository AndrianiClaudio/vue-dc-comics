<template>
    <div class="col">
        <div v-for="(title,index) in col.title"
        v-bind:key='title+index'
        >
            <h2>{{title}}</h2>
            <ul>
                <li
                v-for="(item,index) in col.items[index]"
                v-bind:key='item+index'
                >
                    <a href="#">{{item}}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name:'FooterMain',
    props: {
        col: Object,
    },
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/partials/_variables.scss";
@import "../../assets/scss/partials/_mixins.scss";
.col {
    h2 {
        @include text($siz:1.25rem,$tra:uppercase,$col:white);
    }
    ul {
        @include dim($pad:0 0 1.5rem 0);
        a {
            @include text($tra:capitalize,$col:grey);
        }
    }
}
</style>