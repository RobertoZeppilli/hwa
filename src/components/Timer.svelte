<script>
    import ProgressBar from "./ProgressBar.svelte";
</script>

<div class="timer">
    <h2>Seconds Left: </h2>
    <ProgressBar />
    <button class="start">Start</button>
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
</style>
