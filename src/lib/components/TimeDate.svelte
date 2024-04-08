<script>
    import { onDestroy, onMount } from "svelte";

    let time = new Date();

    const updateTime = () => {
        time = new Date();
    };

    const interval = setInterval(updateTime, 1000); // Update time every second

    onMount(() => {
        updateTime(); // Initialize time on mount

        // Cleanup function to clear interval when component is destroyed
        onDestroy(() => {
            clearInterval(interval);
        });
    });
</script>

<div class="flex flex-col mr-8">
    <span class="text-2xl text-end">{time.toLocaleTimeString()}</span>
    <span class="text-lg  text-end"> {time.toLocaleDateString()}</span>
</div>
