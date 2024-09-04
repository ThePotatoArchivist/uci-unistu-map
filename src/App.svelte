<script lang="ts">
    import PlacedDossier from './lib/PlacedDossier.svelte';
</script>

<main>
    <PlacedDossier key="d1">
        <svelte:fragment slot="cover">
            <p>Classified</p>
        </svelte:fragment>
        <svelte:fragment slot="left">
            <p>Hi</p>
        </svelte:fragment>
        <p>Hi</p>
    </PlacedDossier>
    <PlacedDossier key="d2">
        <svelte:fragment slot="cover">
            <p>Classified</p>
        </svelte:fragment>
        <svelte:fragment slot="left">
            <p>Hi</p>
        </svelte:fragment>
        <p>Hi</p>
    </PlacedDossier>
</main>

<style>
</style>
