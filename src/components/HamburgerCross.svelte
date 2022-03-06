<script>
    import HamburgerIcon from "../icons/HamburgerIcon.svelte";
    import CrossIcon from "../icons/CrossIcon.svelte";
    export let showMobilFeatures = false;
</script>

<div class="icon {$$props.class}" on:click>
    {#if showMobilFeatures}
        <CrossIcon/>
    {:else}
        <HamburgerIcon />
    {/if}
</div>
