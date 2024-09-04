<script lang="ts">
</script>

<div class="page">
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
</style>
