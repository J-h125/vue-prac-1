<template>
    <div>
        求和：{{count}}
    </div>
</template>
<script>
import {EventBus} from '../util/event-bus'
export default {
    name:"secondCom",
    props:{},
    data(){
        return{
            count: 0
        }
    },
    mounted(){
        EventBus.$on('addition',(param)=>{
            this.count = this.count + param.num
        })
    },
    methods: {
        sayHi(){
            console.log('hihihihihiiihi')
        }
    }
}
</script>
<style lang="scss" scoped>

</style>
