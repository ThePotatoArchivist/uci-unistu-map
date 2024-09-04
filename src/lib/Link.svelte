<script lang="ts">
    export let href: string;
</script>

<a {href} {...$$restProps}>{href.match(/^https:\/\/(?:www.)?(.*?)\/?$/)?.[1] ?? href}</a>
