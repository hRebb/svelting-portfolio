<script lang="ts">
    import {fade} from 'svelte/transition';

    const carouselPhotos = [
        '../img/bootstrap_plain_logo_icon_146619.png',
        '../img/css3_socialnetwork_17714.png',
        '../img/data-servers_icon-icons.com_52838.png',
        '../img/figma_logo_icon_147289.png',
        '../img/file_type_git_icon_130581.png',
        '../img/file_type_php_icon_130266.png',
        '../img/file_type_sql_icon_130152.png',
        '../img/github_git_icon_145985.png',
        '../img/gitlab_original_logo_icon_146503.png',
        '../img/html_5_icon-icons.com_55763.png',
        '../img/javascript_icon_130900.png',
        '../img/jquery_plain_wordmark_logo_icon_146445.png',
        '../img/microsoft_visual_studio_code_alt_macos_bigsur_icon_189952.png',
        '../img/mysql_original_wordmark_logo_icon_146417.png',
        '../img/phpmyadmin_logo_icon_168906.png',
        '../img/sass_lang_logo_icon_168850.png',
        '../img/Trello_icon-icons.com_66775.png',
        '../img/wordpress_94199.png'
    ]

    let index = 0 

    const next = () => {
        index = (index + 1) % carouselPhotos.length
    }
</script>

<style type="scss">
    @use '../scss/carrousel.scss';
</style>

{#each [carouselPhotos[index]] as src (index)}
	<img class="imgCarrousel" transition:fade {src} alt="" />	
{/each}

<div class="divButton">
    <button class="nextButton" on:click={next}>Next</button>
</div>