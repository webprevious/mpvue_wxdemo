<template>
    <div class="rate">
        <span>☆☆☆☆☆</span>
        <div class="hollow" :style="style">★★★★★</div>
    </div>
</template>

<script>
export default{
    props: {
        value:{
            type:[String,Number],
            default:"0"
        }
    },
    computed: {
        style(){
            return `width:${this.value/2.4}em`
        }
    },
}
</script>

<style scoped lang="stylus">
.rate{
    position: relative;
    display: inline-block;
    .hollow{
        position: absolute;
        display:inline-block;
        top:0;
        left:0;
        width:0;
        overflow: hidden;
    }
}
</style>