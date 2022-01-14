<template>
<div class="card">
  <h1>{{txt}}</h1>
</div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        txt:String,
    }
}
</script>

<style scoped lang='scss'>
h1 {
    color: red;
}
</style>