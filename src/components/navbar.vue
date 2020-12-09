<template>
    <div class="nav">
        <ul>
            <li>1</li>
            <li>2</li>
            <li>3</li>
            <li>4</li>
            <li>5</li>
        </ul>
        <hr>

        <h4>Online Friends</h4>
        <ol>
            <li v-for="(friend,index) in friends" :key="index" ><span v-if="friend.status" @click="unfrnd(friend.name)">{{friend.name}}</span></li>
        </ol>
    </div>
</template>

<script>
    export default {
        name : "navbar",
        props: ['friends'],
        methods:{
            unfrnd(name){
                this.$emit('dlt',{name})
            }
        }
    }   
</script>

<style scoped>
    .nav ul{display: flex;align-items: center;justify-content: center;}
    .nav ul li{ list-style: none; padding: 0px 20px;}

</style>