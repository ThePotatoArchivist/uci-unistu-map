<script lang="ts">
    import Dossier from './Dossier.svelte';
    import { fade } from 'svelte/transition';

    export let key: string;
    export let title = '';
    let zoomed = false;
    let open = false;
</script>

<button class="positioned" on:click|preventDefault={() => zoomed = true}>
    {#if !zoomed}
        <Dossier {key} {title} alignRight>
            <slot name="cover" slot="cover" {open} />
            <slot name="left" slot="left" {open} />
            <slot {open} />
        </Dossier>
    {/if}
</button>

{#if zoomed}
    <div class="overlay-container">
        <button class="overlay" on:click={() => open = false} transition:fade={{duration: 400}} />
        <Dossier {key} {title} {open} zoomed on:closeanimationend={() => !open && (zoomed = false)} on:introend={() => open = true}>
            <slot name="cover" slot="cover" {open} />
            <slot name="left" slot="left" {open} />
            <slot {open} />
        </Dossier>
    </div>
{/if}

<style>
    .overlay-container {
        position: fixed;
        inset: 0;
        display: grid;
        place-items: center;
        z-index: 10;
    }

    .overlay {
        z-index: -10;
        background-color: #0005;
        position: absolute;
        inset: 0;
    }
    
    .positioned {
        box-sizing: border-box;
        translate: var(--dossier-translate);
        font-size: 0.6em;
        width: 40em;
        cursor: pointer;
    }
</style>
