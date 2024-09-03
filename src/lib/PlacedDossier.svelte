<script lang="ts">
    import type { MouseEventHandler } from 'svelte/elements';
    import Dossier from './Dossier.svelte';
    import { fade } from 'svelte/transition';

    export let key: string;
    let zoomed = false;
    let open = false;
    
    const overlayClick: MouseEventHandler<HTMLButtonElement> = event => {
        if (event.target === event.currentTarget) {
            open = false;
        }
    }
</script>

{#if zoomed}
    <button class="overlay" on:click={overlayClick} transition:fade={{duration: 400 }}>
        <Dossier {key} {open} on:closeanimationend={() => !open && (zoomed = false)} on:introend={() => open = true}>
            <slot name="cover" slot="cover" />
            <slot name="left" slot="left" />
            <slot />
        </Dossier>
    </button>
{:else}
    <div class="positioned">
        <Dossier {key} on:click={() => zoomed = true}>
            <slot name="cover" slot="cover" />
            <slot name="left" slot="left" />
            <slot />
        </Dossier>
    </div>
{/if}

<style>
    .overlay {
        position: fixed;
        inset: 0;
        background-color: #0003;
        display: grid;
        place-items: stretch;
        padding: 8em;
    }
    
    .positioned {
        height: 300px;
        width: 400px;
    }
</style>
