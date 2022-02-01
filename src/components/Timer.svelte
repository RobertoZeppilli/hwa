<script>
    import ProgressBar from "./ProgressBar.svelte";

    // export let progress;

    let totalSeconds = 20;
    let secondsLeft = totalSeconds;
    let isRunning = false;

    $: progress = ((totalSeconds - secondsLeft) / totalSeconds) * 100;

    const handleStart = () => {
        isRunning = true;
        const timer = setInterval(() => {
            secondsLeft--;

            if(secondsLeft < 0) {
                clearInterval(timer)
                isRunning = false
                secondsLeft = totalSeconds
            }
        }, 1000);
    };

</script>

<div class="timer">
    <h2>Seconds Left: {secondsLeft}</h2>
    <ProgressBar {progress} />
    <button disabled={isRunning} class="start" on:click={handleStart}>Start</button>
</div>

<style>
    .timer {
        padding: 2.45rem;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;
        /* background-color: #333; */
    }

    .timer h2 {
        margin: 20px 0;
    }

    .start {
        background-color: rgb(154, 73, 73);
        width: 100%;
        margin: 10px 0;
    }

    .start[disabled] {
        background-color: rgb(154, 73, 73, 0.7);
        cursor: not-allowed;
    }
</style>
