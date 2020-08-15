<template>
	<div>
		Todo form
		<input type="text" v-model="newTodoItem">
		<button @click="addTodoItem">Submit</button>
	</div>
</template>

<script>
	export default{
		data(){
			return{
				newTodoItem:""

			}

		},
		methods:{
			addTodoItem(){
				this.$store.dispatch("addNewTodo", this.newTodoItem)
				this.newTodoItem=""

			}
		}

	}
</script>