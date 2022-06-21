<script>
    import {createEventDispatcher} from 'svelte';
    const dispatch = createEventDispatcher()

    export let items;
    export let activeItem;
</script>

<ul class="flex justify-center">
    {#each items as item}
        <li on:click={() => dispatch('tabChange', item)} class="cursor-pointer px-3 md:text-lg text-sm text-center">
            <div class:active={item === activeItem}>
                {item}
            </div>
        </li>
    {/each}
</ul>

<style>
    .active {
        color: #03A84E;
        border-bottom: 1px solid #03A84E;
        padding-bottom: 4px;
    }
</style>