<template>
	<div>
		Single Todo
		<span :class="{completed:todo.completed}" @click="toogleStatus">
			{{todo.title}}
		</span>
		<button @click="deleteTodo">Delete</button>
	</div>
</template>

<script>
	//import { mapActions } from "vuex";
	export default{
		props:['todo'],

		methods:{
			// ...mapActions({
			// 	deleteTodo:'deleteTodo',
			// 	toogleStatus:'toogleStatus'
			// })

			deleteTodo(){
				this.$store.dispatch("deleteTodo", this.todo)
			}
			,
			toogleStatus(){
				this.$store.dispatch("toogleTodoStatus", this.todo)
			}
		}

	}
</script>
<style type="text/css">
	.completed{
		color: red;
	}
</style>