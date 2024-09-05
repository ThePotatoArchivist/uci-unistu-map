<script lang="ts">
    export let href: string;
</script>

<a {href} target="_blank" {...$$restProps}>{href.match(/^https:\/\/(?:www.)?(.*?)\/?$/)?.[1] ?? href}</a>

<style>
    a {
        overflow-wrap: anywhere;
    }
</style>
