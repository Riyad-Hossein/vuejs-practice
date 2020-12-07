<template>
    <div class="nav">
        <ul>
            <li>1</li>
            <li>2</li>
            <li>3</li>
            <li>4</li>
            <li>5</li>
        </ul>
    </div>
</template>

<script>
    export default {
        name : "navbar"
    }   
</script>

<style scoped>
    .nav ul{display: flex;align-items: center;justify-content: center;}
    .nav ul li{ list-style: none; padding: 0px 20px;}

</style>