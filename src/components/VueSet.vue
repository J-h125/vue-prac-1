<template>
    <div class="set">
        <ul>
            <li v-for="value in obj" :key="value">{{value}}</li>
        </ul>
        <button @click="add()">+obj.b</button>
    </div>
</template>
<script>
export default {
    name: "VueSet",
    props:{},
    data(){
        return{
            obj:{
                a:'this.$set'
            }
        }
    },
    methods:{
        add () {
            this.$set(this.obj,'b','bbb')  
            // this.obj.b = 'bbb'  
            console.log(this.obj)
        }
    }
}
</script>
<style lang="scss" scoped>
.set {
    border:1px solid red;
}
</style>