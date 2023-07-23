<script>
    import Todo from './Todo.svelte';
    let newTodo = '';
    let todos = [];

    function addTodo() {
        if (newTodo !== '') {
            todos = [...todos, newTodo];
            newTodo = '';
        }
    }

    function removeTodo(index) {
        todos = todos.filter((_, i) => i !== index);
    }
</script>

<div class="todo-list">
    <input bind:value={newTodo} placeholder="New todo" />
    <button on:click={addTodo}>Add</button>

    {#each todos as todo, index (index)}
        <Todo {todo} remove={() => removeTodo(index)} />
    {/each}
</div>
