<template>
    <div class="container pt-4">
        <iframe class="rounded" src="https://www.youtube.com/embed/Kz3pqDnSgMM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
</template>

<script>
    export default {
        name: 'DicaVideo',
    }
</script>

<style scoped>
    iframe {
        width: 100% !important;
        height: 650px !important;
    }

    @media(max-width: 768px) {
        iframe {
            height: 430px !important;
        }
    }
</style>