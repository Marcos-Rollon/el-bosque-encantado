<script>
    import {createEventDispatcher} from "svelte";

    export let text = ""

    const dispatch = createEventDispatcher();

    function handleClick(){
        dispatch("click")
    }
</script>

<div class="container" on:click={handleClick}>
    <h2>{text}</h2>
</div>
<style>
    .container{
        display: flex;
        align-items: center;
        justify-content: center;

        width: 500px;
        height: 100px;
        margin: 10px;

        background-color: rgb(0, 173, 72);
        border-radius: 10px;
        color: white;
        transition: ease-in-out 0.2s;
    }

    .container:hover{
        transform: scale(1.1);
        filter: drop-shadow(2px 2px 5px rgb(0 0 0 / 0.5));
    }
    .container:active{
        filter: brightness(0.85);
    }
</style>