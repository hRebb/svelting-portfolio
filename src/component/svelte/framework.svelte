<script lang="ts">
    import {fade} from 'svelte/transition'
    let index = 0
    const frameworks = [
        '../stack_framework/Angular_full_color_logo.svg.png',
        '../stack_framework/cypress-io-logo-social-share-8fb8a1db3cdc0b289fad927694ecb415.png',
        '../stack_framework/logo-D3.png',
        '../stack_framework/React-icon.svg.png',
        '../stack_framework/symfony.png'
    ]

    const nextFramework = () => {
        index = (index + 1) % frameworks.length
    }
</script>

<div class="secondContainer">
    <h2>
        Frameworks
    </h2>
    {#each [frameworks[index]] as src (index) }
        <img class="imgFramework" transition:fade {src} alt="" />
    {/each}
    <button class="next" on:click={nextFramework}>Next</button>
</div>

<style type="scss">
    @use '../scss/framework.scss';
</style>