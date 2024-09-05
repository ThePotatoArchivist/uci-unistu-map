<div class="post-it">
    <slot />
</div>

<style>
    .post-it {
        position: absolute;
        font-family: "Indie Flower", cursive;
        height: 15em;
        width: 15em;
        background-color: var(--postit-color);
        top: var(--postit-top);
        left: var(--postit-left);
        rotate: var(--postit-rotate);
        box-sizing: border-box;
        padding: 1em;
        box-sizing: border-box;
    }
</style>
