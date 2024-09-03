<script lang="ts">
    import { createEventDispatcher } from 'svelte';
    import { receive, send } from './transition';

    export let key: string;
    export let open = false;
    
    const dispatch = createEventDispatcher<{closeanimationend: null}>()
</script>

<button class="container" class:closed={!open} on:click in:receive={{key}} out:send={{key}} on:introend>
    <div class="cover right back">
        <slot name="cover" />
    </div>
    <div class="cover left" on:transitionend={() => dispatch('closeanimationend')}>
        <slot name="left" />
    </div>
    <div class="cover right">
        <slot />
    </div>
</button>

<style>
    .container {
        /* aspect-ratio: 4 / 3; */
        height: 100%;
        width: 100%;
        box-sizing: border-box;
        position: relative;
        perspective: 2000px;
    }

    .cover {
        position: absolute;
        top: 0;
        bottom: 0;
        background-color: orange;
    }
    
    .cover {
        width: 50%;
    }
    
    .left {
        left: 0;
        transform-origin: right center;
    }
    
    .left, .back {
        transition: rotate 0.6s;
        backface-visibility: hidden;
    }
    
    .back {
        transform-origin: left center;
        z-index: 10;
    }
    
    .right {
        left: 50%;
    }
    
    .closed .left, .back {
        rotate: y 180deg;
    }
    
    .closed .back {
        rotate: y 360deg;
    }
</style>
