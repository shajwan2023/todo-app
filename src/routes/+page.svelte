<script>
	import TodoForm from '../components/TodoForm.svelte';
	import { todos } from '../stores/todoStore.js';
	import Todo from '../components/Todo.svelte';
</script>

<div class="text-slate-800 max-w-lg mx-auto placeholder-cyan-100">
	<h1 class="text-center">My Todos</h1>

	<TodoForm />

	{#each $todos as todo}
		<Todo {todo} index={todo.id} />
	{/each}
</div>
