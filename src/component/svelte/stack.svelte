<script lang="ts">

    import {fade} from 'svelte/transition';

    let index = 0

    const progLanguage = [
        '../stack_prog_language/1200px-Go_Logo_Blue.svg.png',
        '../stack_prog_language/1200px-Python-logo-notext.svg.png',
        '../stack_prog_language/1200px-Ruby_logo.svg.png',
        '../stack_prog_language/1200px-WebAssembly_Logo.svg.png',
        '../stack_prog_language/1200px_C_Sharp_logo_svg_16fb904a2f.png',
        '../stack_prog_language/formation-langage-c-avance.png',
        '../stack_prog_language/Free-C-Certification-Course-1.png',
        '../stack_prog_language/node-300x300.jpg',
        '../stack_prog_language/powershell.png',
        '../stack_prog_language/Rust_programming_language_black_logo.svg.png',
        '../stack_prog_language/thumb_bigger_formation-shell-bash.jpg',
        '../stack_prog_language/Typescript_logo_2020.svg.png'
    ]
    const nextLanguage = () => {
        index = (index + 1) % progLanguage.length
    }

</script>

<style type="scss">
    @use '../scss/stack.scss';
</style>

<div class="firstContainer">
    <h2>
        Programming Language
    </h2>
    {#each [progLanguage[index]] as src (index)}
        <img class="imgLanguage" transition:fade {src} alt="" />
    {/each}
    <button class="next" on:click={nextLanguage}>Next</button>
</div>


