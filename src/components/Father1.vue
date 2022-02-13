<template>
    <div>
        <first-com></first-com>
        <second-com ref="child2"></second-com>
    </div>
</template>
<script>
import firstCom from "./firstCom.vue"
import secondCom from "./secondCom.vue"
export default {
    name:"father1",
    components:{
        firstCom,
        secondCom
    },
    provide(){
        return{
            number:this.num
        }
    },
    mounted(){
        console.log(this.$refs.child2.name)
        this.$refs.child2.sayHi()
    },
    props:{},
    data(){
        return{
            num:999
        }
    },
    methods: {}
}
</script>
<style lang="scss" scoped>

</style>
