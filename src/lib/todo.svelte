<script>
    export let todo;
    export let remove;
</script>

<div class="todo-item">
    <p>{todo}</p>
    <button on:click={remove}>Remove</button>
</div>

<style>
    .todo-item {
        display: flex;
        justify-content: space-between;
        margin-bottom: 1em;
    }
</style>
