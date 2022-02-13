<template>
    <div>
        v-model：
        <input type="text" :value="content" @input="showContent">
    </div>
</template>
<script>
export default {
    name:'model',
    model:{
        prop:'content',
        event:'input'
    },
    props:{
        content:String
    },
    data(){
        return{
        }
    },
    methods: {
        showContent(e){
            this.$emit('input',e.target.value)
        }
    }
}
</script>
<style lang="scss" scoped>

</style>
