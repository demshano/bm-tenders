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

<div class="fixed top-32 right-0 p-4">
    <h1 class="text-2xl">The current time is {time.toLocaleTimeString()}</h1>
    <h2 class="text-lg">Today's date is {time.toLocaleDateString()}</h2>
</div>
