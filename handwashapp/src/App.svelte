<script>
    import Timer from "./Timer.svelte";
    import HowTo from "./HowTo.svelte";
    let audio;
    function timerEnds(e) {
        audio.play();
    }
</script>

<h1>Handwashing App</h1>
<Timer on:end={timerEnds} />
<HowTo />
<h3>
    <a href="http://picture">Picture Source</a>
    <a href="http://picture">Sound Source</a>
</h3>

<audio bind:this={audio}>
    <source src="sound.wav" />
</audio>
<style>
    h1, h3{
        text-align: center;
    }
</style>