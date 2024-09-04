<script lang="ts">
    export let entries: [title: string, value: string, url?: boolean | string][]
</script>

{#each entries as [title, value, url]}
    {#if url}
        <a class="line" href={typeof url === 'string' ? url : value} target="_blank">
            <div>{title}</div>
            <div class="middle" />
            <div>{value.match(/^https:\/\/(?:www.)?(.*?)\/?$/)?.[1] ?? value}</div>
        </a>
    {:else}
        <div class="line">
            <div>{title}</div>
            <div class="middle" />
            <div>{value}</div>
        </div>
    {/if}
{/each}

<style>
    .line {
        display: flex;
        flex-direction: row;
        gap: 0.2em;
    }

    .middle {
        flex-grow: 1;
        border-bottom: 1.5px dashed currentColor;
        margin-bottom: 0.23em;
    }
</style>
