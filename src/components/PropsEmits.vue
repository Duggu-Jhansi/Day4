<template>
	<div class="container" >
        <div class="d-flex flex-row">
       <h1>id: {{ id }}</h1>
		<h2> title: {{ title }}</h2>
		<p> description: {{ description}}</p>
    <img v-bind:src="imgUrl" class="profile-pic" />
</div>
</div>
</template>

<script setup>
 import { defineProps } from 'vue';
defineProps({
    id:Number,
	title: String,
	description: String,
    imgUrl:String,
})
</script>



<style scoped>
h2 {
	padding: 0;
	margin: 0;
}
.container {
   
	background-image:url('https://img.freepik.com/free-photo/3d-background-with-white-cubes_23-2150472987.jpg');
	border: 1px solid rgb(124, 191, 202);
	width: 300px;
	margin: 1em auto 1em auto;
	padding: 1em;
	border-radius: 5px;
	font-size: 1.3em;
    color:black
   
    
}


</style>