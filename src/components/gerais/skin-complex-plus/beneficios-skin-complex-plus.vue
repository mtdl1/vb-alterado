<template>
    <div class="container-fluid bg-light py-5 text-center mt-5">
        <div class="container">
            <h2>7 Benefícios em um único produto:</h2>
            <div class="row px-5 pt-4">
                <div class="col-4 col-md">
                    <img src="@/assets/img/beneficios-skin-complex/pele.webp" alt="Imagem demonstrando que o colágeno Viva Beauty traz benefícios para a pele" title="Benefícios para a pele" class="img-fluid">
                </div>
                <div class="col-4 col-md">
                    <img src="@/assets/img/beneficios-skin-complex/unhas.webp" alt="Imagem demonstrando que o colágeno Viva Beauty traz benefícios para as unhas" title="Benefícios para as unhas" class="img-fluid">
                </div>
                <div class="col-4 col-md">
                    <img src="@/assets/img/beneficios-skin-complex/rugas.webp" alt="Imagem demonstrando que o colágeno Viva Beauty previne as rugas" title="Previne as rugas" class="img-fluid">
                </div>
                <div class="col-4 col-md">
                    <img src="@/assets/img/beneficios-skin-complex/flacidez.webp" alt="Imagem demonstrando que o colágeno Viva Beauty previne a flacidez" title="Previne a flacidez" class="img-fluid">
                </div>
                <div class="col-4 col-md">
                    <img src="@/assets/img/beneficios-skin-complex/celulites.webp" alt="Imagem demonstrando que o colágeno Viva Beauty previne as celulites" title="Previne as celulites" class="img-fluid">
                </div>
                <div class="col-4 col-md">
                    <img src="@/assets/img/beneficios-skin-complex-plus/ossos.webp" alt="Imagem demonstrando que o colágeno Viva Beauty auxilia no fortalecimento dos ossos" title="Auxílio no fortalecimento dos ossos" class="img-fluid">
                </div>
                <div class="col-4 col-md">
                    <img src="@/assets/img/beneficios-skin-complex/cabelos.webp" alt="Imagem demonstrando que o colágeno Viva Beauty ajuda no fortalecimento e crescimento dos cabelos" class="img-fluid">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MaisQueColagenoSkinComplex',
    }
</script>

<style scoped>
    .bg-light {
        background: #fbf3f1 !important;
    }

    h2 {
        font-size: 20px;
        font-family: Poppins, sans-serif;
        color: #000;
    }

    @media(max-width: 768px) {
        .col-4 {
            padding: 0 !important;
        }
    }
</style>