<script lang="ts">
    import {fade} from 'svelte/transition';

    let index = 0

    const devops = [
        '../stack_tools/0.png',
        '../stack_tools/1200px-Jenkins_logo.svg.png',
        '../stack_tools/800px-Amazon_Web_Services_Logo.svg.png',
        '../stack_tools/Ansible_logo.svg.png',
        '../stack_tools/Azure DevsOps.png',
        '../stack_tools/ci-cd.png',
        '../stack_tools/Circleci-icon-logo.svg.png',
        '../stack_tools/h2jfrvzrbyh1yff2n3wfu2hkqqps6x_uvqo.png',
        '../stack_tools/homepage-docker-logo.png',
        '../stack_tools/kubernetes.png',
        '../stack_tools/Logo-vagrant.png',
        '../stack_tools/bf69b502-cycloyd.png',
        '../stack_tools/Selenium_logo.svg.png',
        '../stack_tools/TERRAFORM.png',
        '../stack_tools/unnamed.png'
    ]

    const nextTools = () => {
        index = (index + 1) % devops.length
    }
</script>

<style type="scss">
    @use '../scss/tools.scss';
</style>

<div class="thirdContainer">
    <h2>
        Tools for DevOps and Others way to develop
    </h2>

    {#each [devops[index]] as src (index) }
        <img class="imgDev" transition:fade { src } alt="" />
    {/each}
    <button class="next" on:click={nextTools}>Next</button>
</div>
