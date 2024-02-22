<template>
	<div class="container">
        <div class="one">
		<h2> Name: {{  name  }}</h2>
		<p> Department: {{ department }}</p>
		<p> Salary: {{ salary }}</p>
		<p> Position: {{ position }}</p>
		<button @click="$emit('deleteItem', position)">Remove Member</button>
	</div>
<div class="imgStyle">
    <img v-bind:src="imageUrl" class="profile-pic" />
</div>
</div>
</template>

<script setup>
 import { defineProps } from 'vue';
defineProps({
	name: String,
	department: String,
	salary: Number,
	position: Number,
    imageUrl:String,
})
</script>



<style scoped>
h2 {
	padding: 0;
	margin: 0;
}
.container {
    background-image:url('https://4kwallpapers.com/images/wallpapers/windows-11-dark-mode-abstract-background-black-background-3440x1440-8710.jpg');
	border: 1px solid rgb(124, 191, 202);
	width: 300px;
	margin: 1em auto 1em auto;
	padding: 1em;
	border-radius: 5px;
	font-size: 1.3em;
    color:white
    
    
}

.profile-pic {
  width: 48px;
  height: 48px;
  border-radius: 24px;
  /* border: 3px solid #000; */
}
.imgStyle {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 3px;
  background-color: #fff;
  border-radius: 50%;
  border: 2px solid rebeccapurple;
  box-shadow: 1px 10px 10px -4px #000;
}
</style>