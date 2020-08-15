<template>
	<div>To do list
		<todo v-for="(todo,index) in todos" :key="index" :todo="todo" />


	</div>
</template>

<script>
	import { mapState } from "vuex";
	import Todo from "./Todo";

	export default{
		components:{
			Todo
		}, 
		computed:{
			// todos(){
			// 	return this.$store.state.todos;
			// }
			...mapState({
				todos:"todos"//this todos is in state
			})
		}

	}
</script>