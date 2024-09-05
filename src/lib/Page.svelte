<script lang="ts">
    export let handwritten = false;
    export let typewriter = false;
</script>

<div class="page" class:handwritten class:typewriter>
    <slot />
</div>

<style>
    :global(:root) {
        --page-color: white;
        --page-margin: 3em;
    }

    .page {
        background-color:var(--page-color);
        width: 35em;
        place-self: center;
        aspect-ratio: 8.5 / 11;
        padding: var(--page-margin);
        box-sizing: border-box;
        text-align: left;
    }

    .handwritten {
        font-family: 'Indie Flower', cursive;
    }

    .typewriter {
        font-family: "Special Elite", 'Courier New', Courier, monospace;
    }
</style>
