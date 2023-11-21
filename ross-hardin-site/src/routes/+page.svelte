<script>
    import { goto } from '$app/navigation';
    let title = 'Welcome!';

    const updateTitle = () => {
        title = 'something new';
    }

    const handleClick = () => {
        goto('/about');
    }
</script>

<div class="index">
    <h2>{title}</h2>
    <button on:click={updateTitle}>change title</button>
    <input type="text" bind:value={title}>
    <button on:click={handleClick}>About</button>
    <a href="/about">About</a>
</div>

<style>
    .index {
        text-align: center;
        display: block;
        margin: 20px auto;
    }
</style>
