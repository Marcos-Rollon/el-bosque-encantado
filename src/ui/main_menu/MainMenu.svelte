<script>
    import MainMenuItem from "./MainMenuItem.svelte";
    import {fade} from "svelte/transition";
    import {createEventDispatcher} from "svelte";

    const dispatch = createEventDispatcher();

    function handleMenuClick(option){
        dispatch("menuClick", option)
    }

</script>

<main transition:fade>
    <div style="height: 100px;"></div>
    <MainMenuItem text="Continuar" on:click={()=> handleMenuClick(0)}/>
    <MainMenuItem text="Nueva Partida" on:click={()=> handleMenuClick(1)}/>
    <MainMenuItem text="Acerca de..." on:click={()=> handleMenuClick(2)} />
</main>

<style>
    main{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    
</style>