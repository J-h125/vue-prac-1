<template>
    <div>111
        <button @click="add">加法</button>
        <div>inject:{{number}}</div>
    </div>
</template>
<script>
import {EventBus} from '../util/event-bus'
export default {
    name:"firstCom",
    inject:['number'],
    props:{},
    data(){
        return{
            num: 0
        }
    },
    methods: {
        add(){
            EventBus.$emit('addition',{
                num : this.num++
            })
        }
    }
}
</script>
<style lang="scss" scoped>

</style>
