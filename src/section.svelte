<script lang="ts">
    import Corpus from "./component/svelte/corpus.svelte";
    import Tools from "./component/svelte/tools.svelte";
    import Stack from "./component/svelte/stack.svelte";
    import Carrousel from "./component/svelte/carrousel.svelte";
    import Framework from "./component/svelte/framework.svelte";
</script>

<section>
    <Corpus />
</section>

<br>

<section class="secondSection">
    <h2>My Stack</h2>
    <Carrousel />
</section>


<section class="thirdSection">
    <h2 class="stackTitle">Stack Technique à apprendre</h2>
    <Stack/>
</section>

<section>
    <Framework />
</section>

<section>
    <Tools />
</section>

<style type="scss">
    @use '../sass/section.scss';
</style>