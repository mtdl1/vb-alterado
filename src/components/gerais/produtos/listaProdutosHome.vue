<template>
    <div class="container mt-2">
        <h1 class="text-center">Viva Beauty: <br class="mob">o melhor colágeno para sua pele</h1>
        <div class="row d-flex">
            <!-- <div class="col-6 col-md-3 text-center py-3 esgotado">
                <a href="/products/tratamento-anti-idade-6-em-1-skin-complex-com-colageno-verisol-acido-hialuronico">
                    <div class="img-prod mb-3">
                        <img class="img-fluid" src="@/assets/img/produtos/Produto_SkinComplex-0_295x.webp" alt="">
                    </div>
                    <h2 class="w-75 mx-auto">Skin Complex: Tratamento Anti-Idade 6 em 1 com Verisol + Ácido Hialurônico</h2>
                    <p><strong>ESGOTADO</strong></p>
                </a>
            </div> -->
            <div class="text-right descricao desk">
                <p class="desk"> Skin Complex Plus com<br> Colágeno Verisol <br><strong class="lemonade">PINK LEMONADE</strong></p>
            </div>
            <div class=" text-center d-flex" >
                <a href="/products/colageno">
                    <div class="img-prod mb-3">
                        <img class="img-fluid desk" src="@/assets/img/produtos/Produto_SkinComplexPlus-1.png" alt="Imagem para desktop do pote do colágeno Verisol® com Ácido Hialurônico Skin Complex Plus sabor Pink Lemonade" title="Skin Complex Plus com Colágeno Verisol sabor Pink Lemonade">
                        <img class="img-fluid mob" src="@/assets/img/produtos/produto_skincomplex_mob1.png" alt="Imagem para mobile do pote do colágeno Verisol® com Ácido Hialurônico Skin Complex Plus sabor Pink Lemonade" title="Skin Complex Plus com Colágeno Verisol sabor Pink Lemonade" >
                    </div>
                    <p class="mob"> Skin Complex Plus <br>com Colágeno Verisol <br><strong class="lemonade">PINK LEMONADE</strong></p>
                </a>
                <a href="/products/colageno">
                    <div class="img-prod mb-3">
                        <img class="img-fluid desk" src="@/assets/img/produtos/Produto_SkinComplexPlus-2.png" alt="Imagem para Desktop do pote do colágeno Verisol® com Ácido Hialurônico Skin Complex Plus sabor Yellow Fruits" title="Skin Complex Plus com Colágeno Verisol sabor Yellow Fruits">
                        <img class="img-fluid mob" src="@/assets/img/produtos/produto_skincomplex_mob2.png"  alt="Imagem para Mobile do pote do colágeno Verisol® com Ácido Hialurônico Skin Complex Plus sabor Yellow Fruits" title="Skin Complex Plus com Colágeno Verisol sabor Yellow Fruits" >
                    </div>
                    <p class="mob"> Skin Complex Plus <br>com Colágeno Verisol <br><strong class="fruits">YELLOW FRUITS</strong></p>
                </a>
            </div>
            <div class="text-left descricao mob">
                <p class="desk"> Skin Complex Plus com<br> Colágeno Verisol <br><strong class="fruits">YELLOW FRUITS</strong></p>
            </div>
            <!-- <div class="col-6 col-md-3 text-center py-3 esgotado">
                <a href="/products/detox-360-natural-8-em-1-viva-slim-com-fruto-do-cacto-hibisco-cha-verde">
                    <div class="img-prod mb-3">
                        <img class="img-fluid" src="@/assets/img/produtos/Produto_VivaSlim-1_590x_9a57bfc2-330a-4ce3-a3e4-d3a275c8f5a3_295x.webp" alt="">
                    </div>
                    <h2 class="w-75 mx-auto">Detox 360º Natural 8 em 1 Viva Slim: 8 em 1 Viva Slim: 8 Funções em um só produto</h2>
                    <p><strong>ESGOTADO</strong></p>
                </a>
            </div> -->
            <!-- <div class="col-6 col-md-3 text-center py-3">
                <a href="/products/serum-anti-idade-multibeneficios-viva-beauty">
                    <div class="img-prod mb-3 esgotado" >
                        <img class="img-fluid" src="@/assets/img/produtos/Serum_VB_295x.webp" alt="">
                    </div>
                    <h2 class="w-75 mx-auto serum">Sérum Anti-Idade Multibenefícios Viva Beauty </h2>
                    <p><strong >ESGOTADO</strong></p>
                </a>
            </div> -->
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ListaProdutosHome',
    }
</script>

<style scoped>
    
     h1 {
        font-size: 24px;
        font-family: Poppins, sans-serif;
        color: #000;
        padding: 16px 0 14px;
     }

    h2 {
        font-size: 16px;
        font-family: Poppins, sans-serif;
        font-weight: normal;
        color: #000;
        padding-bottom: 8px;
    }

    /* .serum{
        padding-bottom: 22px;
    } */

    .img-prod {
        height: 280px;
        width: 284px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 20px;
    }

    .descricao{
        display: flex;
        justify-content: center;
        align-items: center;
        margin: auto 0;

    }

    .descricao p {
        font-size: 25px;
    }


    .lemonade{
        color: #AF1134;
    }

    .fruits{
        color: #F2C560;
    }




    @media(max-width: 768px) {
        .row.px-5 {
            padding: 0 !important;
        }

         h1 {
        font-size: 20px;
        font-family: Poppins, sans-serif;
        color: #000;
        padding: 16px 0 14px;
     }


        .img-prod {
            width: 100%;
            margin: auto;
            height: 190px;
        }
    }
</style>