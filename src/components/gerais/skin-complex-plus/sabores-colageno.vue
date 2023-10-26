<template>
    <div class="container">
        <div class="row align-items-center justify-content-between py-3">
            <div class="text-center imgs">
                <img src="@/assets/img/sabores-skin-complex-plus/skinplus_lemonade.png" class="img-fluid mb-n " alt="Pote de Skin Complex Plus sabor Pink Lemonade com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" v-show="selecao == 1">
                <img src="@/assets/img/sabores-skin-complex-plus/skinplus_lemonade.png" class="img-fluid mb-n " alt="  Pote de Skin Complex Plus sabor Pink Lemonade com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" v-show="selecao == 3">
                <img src="@/assets/img/sabores-skin-complex-plus/skinplus_yellow.png" class="img-fluid mb-n " alt="Pote de Skin Complex Plus sabor Yellow Fruits com rótulo na cor amarela" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" v-show="selecao == 2">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'SaboresColageno',
        props: {
            selecao: Number
        }
    }
</script>

<style scoped>

    .imgs{
        width: 350px;
    }

    h2 {
        font: normal normal bold 32px/40px Open Sans;
        letter-spacing: -1.28px;
        color: #FFFFFF;
        padding-bottom: 24px;
    }

    p {
        text-align: center;
        font: normal normal normal 16px/22px Open Sans;
        letter-spacing: 0px;
        color: #FFFFFF;
        padding-top: 24px;
    }



    .mb-n {
        margin-bottom: -100px;
    }

    @media(max-width: 768px) {
      
        p {
            font: normal normal normal 14px/19px Open Sans;
            padding-top: 10px;
            padding-bottom: 30px;
        }

       .imgs{
        width: 280px
       }
    }

    @media(max-width: 360px) {
        h2 {
            font: normal normal bold 20px/32px Open Sans;
        }
    }
</style>