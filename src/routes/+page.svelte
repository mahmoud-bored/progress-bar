<script lang="ts">
    let min = $state(0)
    let max = $state(100)
    let current = $state(0)
</script>

<div class="input-progress">
    <input type="number" bind:value={current}>
    <div class="input-container">
        <input class="min-input" type="number" bind:value={min} >
        <input type="range" min="{min}" max="{max}" bind:value={current}>
        <input class="max-input" type="number" bind:value={max}>
    </div>
</div>

<style>
    .input-progress {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 20px;
        width: 100%;
        height: 100%;
    }
    .input-container {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 30px;
    }
    input[type="range"] {
        width: 90%
    }
    input {
        border-radius: 5px;
    }
</style>