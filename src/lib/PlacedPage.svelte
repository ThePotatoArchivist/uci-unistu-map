<script lang="ts">
    import Page from './Page.svelte';
    import { fade } from 'svelte/transition';
    import { receive, send } from './transition';

    export let key: string;
    let zoomed = false;
</script>

<button class="positioned" on:click|preventDefault={() => zoomed = true}>
    {#if !zoomed}
        <div class="transition" in:receive={{key}} out:send={{key}}>
            <Page>
                <slot />
            </Page>
        </div>
    {/if}
</button>

{#if zoomed}
    <div class="overlay-container">
        <button class="overlay" on:click={() => zoomed = false} transition:fade={{duration: 400}} />
        
        <div class="transition" in:receive={{key}} out:send={{key}}>
            <Page>
                <slot />
            </Page>
        </div>
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
        width: 35em;
        cursor: pointer;
    }

</style>
