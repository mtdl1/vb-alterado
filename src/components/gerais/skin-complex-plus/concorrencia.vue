<template>
    <section>
        <div class="container-fluid text-center pt-4 px-0"> 
            <div class="container">
                <h2 class="pb-4">Viva Beauty x Concorrência</h2>
                <div class="row">
                    <div class="col-6 col-md-3 text-right pr-0 order-2 order-md-1 viva">
                            <p>Colágeno Verisol <img src="@/assets/img/skin-complex-plus/check.png"></p>
                            <p>Ácido Hialurônico <img src="@/assets/img/skin-complex-plus/check.png"></p>
                            <p>Silício Orgânico <img src="@/assets/img/skin-complex-plus/check.png"></p>
                            <p>Vitaminas <img src="@/assets/img/skin-complex-plus/check.png"> </p>
                            <p>Minerais <img src="@/assets/img/skin-complex-plus/check.png"> </p>
                            <p>Rico em Biotina <img src="@/assets/img/skin-complex-plus/check.png"></p>
                            <p>Ácido Pantotênico <img src="@/assets/img/skin-complex-plus/check.png"></p>
                            <p>Fonte de fibras <img src="@/assets/img/skin-complex-plus/check.png"></p>
                    </div>
                    <div class="col-12 col-md-6 px-0 order-1 order-md-2 ">
                        <img class=" comparacao" src="@/assets/img/skin-complex-plus/comparacao.png" alt="imagem que mostra a comparação do colágeno Viva Beauty com a concorrência" title="Colágeno Viva Beauty x Concorrência">
                    </div>
                    <div class="col-6 col-md-3 pl-0 text-left order-3 order-md-3 concorrente ">
                            <p> <img src="@/assets/img/skin-complex-plus/check.png"> Colágeno Hidrolisado</p>
                            <p> <img src="@/assets/img/skin-complex-plus/check.png"> Sem Ácido Hialurônico</p>
                            <p> <img src="@/assets/img/skin-complex-plus/check.png"> Sem Vitaminas</p>
                            <p> <img src="@/assets/img/skin-complex-plus/check.png"> Poucos minerais </p>
                    </div>
                </div>
            </div>
            <div class="row">
                <a href="#KitProduto" class="btn btn-chamada">Eu quero</a>
            </div>
        </div>
        <div class="container-fluid text-center bg-light py-4 ">
            <div class="container">
                <h2 class="pb-4 mx-auto">O melhor e mais completo</h2>
                <p class="w-75 mx-auto">Com ingredientes de alta tecnologia, o Viva Beauty possui <strong>fórmula completa e exclusiva, acelerando muito os resultados!</strong> Além disso, é totalmente natural, sem corantes artificiais, sem açúcares, e sem gorduras!</p>
                <div class="d-flex justify-content-center align-items-center composicao">
                    <div class="items-formula">
                        <p>Silício <br> Orgânico <strong>1</strong></p>
                        <p class="mt-5">Ácido <br> Hialurônico <strong>2</strong></p>
                        <p class="mt-5 txt-maior">Peptídeos <br> Bioativos de <br> Colágeno <br class="mob"> Verisol <strong>3</strong></p>
                    </div>
                    <div class="img-composicao">
                        <img src="@/assets/img/skin-complex-plus/skin complex plus.png" class="img-fluid mx-auto desk poteDesk" alt="  Pote de Skin Complex Plus sabor Pink Lemonade com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso">
                        <img src="@/assets/img/skin-complex-plus/skin complex plus.png" class=" mx-auto mob poteMob" alt=" Pote de Skin Complex Plus sabor Pink Lemonade com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso">
                    </div>
                    <div class="items-formula direita">
                        <p><strong>7</strong> Rico em Biotina</p>
                        <p class="mt-5"><strong>6</strong> Ácido Pantotênico</p>
                        <p class="mt-5"><strong>5</strong>Fontes de <br> Fibras</p>
                    </div>
                </div>
                <div class="items-formula meio  ">
                        <p><strong>4</strong></p>
                        <p class="mt-2">Vitaminas e <br class="desk"> minerais </p>
                    </div>
            </div>
        </div>
        <div class="container-fluid text-center py-4">
            <div class="container">
                <h2 class="pb-4">Principais Diferenciais</h2>
                <h3 class="pb-2"><strong>Peptídeos Bioativos de Colágeno Verisol®</strong></h3>
                <p class="w-75 mx-auto">Único colágeno oral específico para a pele com comprovação científica de resultados. Proporciona redução significativa da profundidade das rugas após 4 semanas de uso, e principalmente retarda os sinais do envelhecimento da pele agindo de dentro para fora.</p>
                <h2 class="pt-4 pb-2">Ácido Hialurônico</h2>
                <p class="w-75 mx-auto">É responsável por preencher os espaços entre as células. Consegue reter alta quantidade de água, mantendo a sua pele hidratada, firme e lisinha.</p>
                <h2 class="pt-4 pb-2">Silício Orgânico</h2>
                <p class="w-75 mx-auto">Recomendado por dermatologistas, ele é o  “segredinho” da nossa fórmula. É o responsável por fazer com que seu organismo absorva o colágeno mais rápido e em maior quantidade. Aumenta a hidratação, brilho e a tonicidade da pele, unhas e cabelos.</p>
            </div>
        </div>
    </section>
</template>
<script>
    export default {
        name: 'ConcorrenciaSkinComplex',
    }
</script>

<style scoped>
    h2 {
        font-size: 21px;
        font-family: Poppins, sans-serif;
        color: #000;
    }

    h3 {
        font-size: 19px;
        font-family: Poppins, sans-serif;
        color: #000;
    }


    .btn-chamada {
        width: 180px;
        cursor: pointer;
        padding: 10px 20px;
        margin: 30px auto;
        text-align: center;
        color: #ffffff;
        background: #12AC53;
    }

    .bg-light {
        background-color: #FBF3F1!important;
        background-size: 100% 100%;
    }

    .bg-light h2, .bg-light p {
        color: rgb(0, 0, 0);
    }

    p {
        font-size: 15px;
        font-family: Poppins, sans-serif;
        color: #000;
    }

    .viva p  {
        padding-top: 17px
    }

    .concorrente p {
        padding-top: 20px;
    }


    .items-formula p{
        color: #951837;
        display: flex;
        align-items: center;
        justify-content: flex-end;
        text-align: right;
        font-weight: bold;
        min-height: 55px;
    }

    .items-formula.direita p{
        justify-content: flex-start;
        text-align: left;
    }

    .items-formula p strong{
        color: #fff;
        background-color: #951837;
        width: 25px;
        height: 25px;
        padding: 5px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0 15px;
        text-align: center;
        font-weight: normal;
    }

    .items-formula.meio p {
        justify-content: center!important;
        text-align: center;
        margin-right:15px ;
    }

    .composicao{
            margin-top: 30px;
        }

        .items-formula.meio p {
            min-height: unset;
        }

    .poteDesk{
        position: relative;
    }

    .comparacao{
        width: 190%;
        position: relative;
        right: 45%;
    }




    @media(max-width: 768px) {
        .bg-light {
            background: #FBF3F1 !important;
            background-size: 100%;
        }
        .comparacao img {
            width: 100%;
          
        }

        .items-formula p{
            font-size: 10px !important;
        }

        .items-formula p strong{
            width: 20px;
            height: 20px;
            font-size: 10px;
            padding: 5px;
            margin: 0 5px;
        }

        h2 {
            font-size: 17px !important;
        }

        h3 {
            font-size: 16px !important;
        }


        .items-formula p {min-height: 50px;}

        img.img-fluid.mx-auto {
            margin-top: 20px;
        }

        .items-formula.meio p {
        
        margin-right:0 ;
    }

        .poteMob{
            width: 100%;
            position: relative;
           
        }

        .viva p{
            padding-right: 20px;
            font-size: 13px;
        }

        .concorrente p{
            padding-left: 1px;
            font-size: 12px;
        
        }

        .items-formula {
            width: 40%;
        }

        .img-composicao {
            width: 60%;
        }

        .items-formula.meio {
            margin: 0 auto;
        }
    }
</style>