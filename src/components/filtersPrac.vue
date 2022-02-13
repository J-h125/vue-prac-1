<template>
    <div>过滤器：{{num | filter}}</div>
</template>
<script>
export default {
    name: 'filters',
    data(){
        return {
            num: 33
        }
    },
    filters: {
        filter:function(num){
            let filter = num + 3
            return filter
        }
    }
}
</script>
<style lang="scss" scoped>

</style>