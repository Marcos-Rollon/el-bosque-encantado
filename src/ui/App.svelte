<script>
    import MainMenu from "./main_menu/MainMenu.svelte";
    import Level from "./level/Level.svelte";

    let currentPage = "menu";

    function handleMenuOption(option){
        switch (option.detail) {
            case 0:
                currentPage = "level";
                break;
            case 1:
                currentPage = "menu";
                break;
            case 2:
                currentPage = "menu";
                break;
            default:
                break;
        }
    }
</script>

{#if currentPage == "menu"}
    <MainMenu on:menuClick={handleMenuOption}/>
{:else if currentPage == "level"}
    <Level on:backPressed={()=> currentPage= "menu"}/>
{/if}

<style>

</style>