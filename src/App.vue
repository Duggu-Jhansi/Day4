<template>
	<main>
		<ListItems v-for="(item, index) in database" :name="item.name" :department="item.deparment" :salary="item.salary" :position="index"  :imageUrl="item.imageUrl" :key="index"  v-on:deleteItem="deleteItem"
		/>
		<PropsEmits v-for="(card, index) in cards" :id="card.id" :title="card.title" :description="card.description" :position="index"  :imgUrl="card.imgUrl" :key="index" 
		/>
	</main>
</template>

<script setup>
import { ref } from "vue";
import ListItems from "./components/ListItems.vue";
import PropsEmits from "./components/PropsEmits.vue";

let database = ref([
	{
		name: "Sarah",
		deparment: "Marketing",
		salary: 30000,
		imageUrl: 'https://assets.ccbp.in/frontend/react-js/floyd-miles-img.png',

	},
	{
		name: "Esther",
		deparment: "Engineering",
		salary: 72000,
		imageUrl: 'https://assets.ccbp.in/frontend/react-js/esther-howard-img.png',
	},
	{
		name: "Terrance",
		deparment: "Executive",
		salary: 125000,
		imageUrl: 'https://assets.ccbp.in/frontend/react-js/devon-lane-img.png',
	}
]);

function deleteItem(position) {
	database.value.splice(position, 1);
}
let cards=ref([
  {
    id: 1,
    title: 'Data Scientist',
    description:
      'Data scientists gather and analyze large sets of structured and unstructured data',
    imgUrl: 'https://assets.ccbp.in/frontend/react-js/data-scientist-img.png',
    className: 'card-1',
  },
  {
    id: 2,
    title: 'IOT Developer',
    description:
      'IoT Developers are professionals who can develop, manage, and monitor IoT devices.',
    imgUrl: 'https://assets.ccbp.in/frontend/react-js/iot-developer-img.png',
    className: 'card-2',
  },
  {
    id: 3,
    title: 'VR Developer',
    description:
      'A VR developer creates completely new digital environments that people can see.',
    imgUrl: 'https://assets.ccbp.in/frontend/react-js/vr-developer-img.png',
    className: 'card-3',
  },
  {
    id: 4,
    title: 'ML Engineer',
    description:
      'Machine learning engineers feed data into models defined by data scientists.',
    imgUrl: 'https://assets.ccbp.in/frontend/react-js/ml-engineer-img.png',
    className: 'card-4',
  },
]);
</script>


<style scoped>

</style>