<div class="post-it">
    <slot />
</div>

<style>
    .post-it {
        height: 15em;
        width: 15em;
        background-color: var(--postit-color);
        translate: var(--postit-translate);
        rotate: var(--postit-rotate);
        box-sizing: border-box;
        padding: 1em;
        box-sizing: border-box;
    }
</style>
