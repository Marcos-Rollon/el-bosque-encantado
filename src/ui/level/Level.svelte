<script>
    import {fade} from "svelte/transition";
    import {createEventDispatcher} from "svelte";
    const dispatch = createEventDispatcher();

    function handleBackButton(){
        dispatch("backPressed");
    }
</script>

<main transition:fade>
    <button on:click={handleBackButton}>Atrássss</button>
</main>

<style>
    main{
        background-color: red;
        width: 100vw;
        height: 100vh;
    }
</style>