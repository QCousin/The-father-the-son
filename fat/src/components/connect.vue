<template>
    <p @click="sendfn">{{like}}</p>
</template>

<script>
export default {
//    name:"connect",
    props:["like"],
    methods:{
        sendfn() {
            this.$semit(tabFn)
        }
    }
}   
</script>

<style>
p{
    float:left;
    text-align: center;
}
</style>

