<script lang="ts">
    import type { MouseEventHandler } from 'svelte/elements';
    import Dossier from './Dossier.svelte';
    import { fade } from 'svelte/transition';

    export let key: string;
    let zoomed = false;
    let open = false;
</script>

<div class="positioned">
    {#if !zoomed}
        <Dossier {key} on:click={() => zoomed = true}>
            <slot name="cover" slot="cover" />
            <slot name="left" slot="left" />
            <slot />
        </Dossier>
    {/if}
</div>

{#if zoomed}
    <button class="overlay" on:click|self={() => open = false} transition:fade={{duration: 400 }}>
        <Dossier {key} {open} zoomed on:closeanimationend={() => !open && (zoomed = false)} on:introend={() => open = true}>
            <slot name="cover" slot="cover" />
            <slot name="left" slot="left" />
            <slot />
        </Dossier>
    </button>
{/if}

<style>
    .overlay {
        position: fixed;
        inset: 0;
        background-color: #0005;
        display: grid;
        place-items: center;
        z-index: 10;
    }
    
    .positioned {
        height: 300px;
        width: 400px;
        box-sizing: border-box;
        translate: var(--translate);
        rotate: var(--rotate);
    }
</style>
