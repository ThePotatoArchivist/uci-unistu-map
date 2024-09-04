<script lang="ts">
    import { createEventDispatcher } from 'svelte';
    import { receive, send } from './transition';

    export let key: string;
    export let alignRight = false;
    export let title = '';
    export let open = false;
    export let zoomed = false;
    
    const dispatch = createEventDispatcher<{closeanimationend: null}>()
</script>

<div class="container" class:closed={!open} class:zoomed class:alignRight in:receive={{key}} out:send={{key}} on:introend>
    <div class="cover right back">
        <div class="tab bottom" />
        <slot name="cover" />
    </div>
    <div class="cover left" on:transitionend={() => dispatch('closeanimationend')}>
        <div class="tab bottom" />
        <slot name="left" />
    </div>
    <div class="cover right">
        <div class="tab top">
            <div class="title">{title}</div>
        </div>
        <slot />
    </div>
</div>

<style>
    .container {
        aspect-ratio: 5 / 3;
        width: 80em;
        box-sizing: border-box;
        position: relative;
        perspective: 2000px;
    }

    .container.closed {
        pointer-events: none;
    }

    .alignRight {
        translate: -50% 0;
    }

    .cover {
        position: absolute;
        top: 0;
        bottom: 0;
        width: 50%;
        background-color: #f0d197;
        display: grid;
        box-sizing: border-box;
    }
    
    .left {
        left: 2.6%;
        transform-origin: right center;
        border-top-left-radius: 15px;
    }
    
    .right {
        left: 50%;
        border-bottom-right-radius: 15px;
    }

    .left, .back {
        width: 47.5%;
        transition: rotate 0.6s;
        backface-visibility: hidden;
    }
    
    .back {
        transform-origin: left center;
        border-radius: 0;
        z-index: 10;
        border-top-right-radius: 15px;
        border-bottom-right-radius: 0;
        filter: drop-shadow(3px 0 3px #0003);
    }
    
    .closed .left, .back {
        rotate: y 180deg;
    }
    
    .closed .back {
        rotate: y 360deg;
    }
    
    .tab {
        position: absolute;
        width: 5%;
        background-color: #f0d197;;
    }
    
    .left .tab {
        right: 99.5%;
        border-radius: 999px 0 0 999px;
    }
    
    .left .tab, .back .tab {
        width: 5.55%;
    }
    
    .right .tab {
        left: 99.5%;
        border-radius: 0 999px 999px 0;
       
    }
    
    .tab.top {
        top: 0;
        height: 33.3%;
    }
    
    .tab.bottom {
        bottom: 0;
        height: 66.7%;
    }

    .title {
        position: absolute;
        width: 200%;
        height: 100%;
        top: 0;
        right: 0;
        writing-mode: vertical-lr;
        text-orientation: sideways;
        text-align: center;
        font-size: 1.4em;
        display: grid;
        place-items: center
    }
</style>
