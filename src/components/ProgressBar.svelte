<script>
    export let progress
</script>

<div class="progress-container">
    <div class="progress-bar" style="width: {progress}%;">
        <span class="sr-only">{progress}%</span>
    </div>
</div>

<style>
    .progress-container {
        /* margin: 20px 0; */
        border: solid rgb(194, 194, 194) 1px;
        width: 100%;
    }
    .progress-bar {
        height: 30px;
        background-color: rgb(77, 199, 55);
    }
</style>
