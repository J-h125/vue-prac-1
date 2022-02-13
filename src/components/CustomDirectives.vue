<template>
    <div class="directive">
        <input type="text" placeholder="我是局部自定义指令" v-focus1>
    </div>
</template>
<script>
export default {
    name:'',
    components:{},
    props:{
    },
    directives: {
        focus1:{
            inserted:function(el){
                el.focus()
            }
        }
    },
    data(){
        return{}
    }
}
</script>
<style lang="scss" scoped>
.directive {
    border: 1px solid red;
}
</style>