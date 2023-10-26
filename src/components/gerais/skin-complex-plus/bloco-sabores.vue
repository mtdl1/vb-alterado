<template>
    <div class="container px-0">
        <div class="row px-0 flex-wrap-reverse">
            <div class="col-md-8 pt-4">
                <tabela-nutricional-plus />
            </div>
            <div class="col-md-4 complex ">
            <saboresColageno :selecao="selectSabor" class="ml-3" />
            <div class="d-flex flex-wrap-mob buttons">
                <div class=" btns order-1 order-md-2 mx-auto ">
                     <p class="text-center py-4">SABORES DELICIOSOS</p>
                    <div :class="['btn-change-sabor mx-auto mb-3 bor-pink', {pinkLemonade: selectSabor == 1}]" @click="selectSabor = 1">PINK LEMONADE</div>
                    <div :class="['btn-change-sabor mx-auto mb-3 bor-yellow', {yellowFruits: selectSabor == 2}]" @click="selectSabor = 2">YELLOW FRUITS</div>
                </div>
            </div>

            </div>
        </div>
        <div class="row">
            <div class="col-md-5 tabela1 ">
                <span class="lemonade">
                   <p>PINK LEMONADE</p> 
                </span>
                <p><strong>Ingredientes:</strong> Polidextrose, Peptídeos Bioativos de Colágeno Hidrolisado com peso molecular médio de 2kDa (Verisol©), Hialuronato de Sódio obtido pela fermentação de Streptococcus zoopidemicus (Ácido Hialurônico), Ácido Ascórbico (Vitamina C), D-Pantotenato de Cálcio (Ácido Pantotênico), Bisglicinato de Zinco (Zinco), Cloridrato de piridoxina (Vitamina B6), Sulfato de Manganês (Manganês), Acetato de Retinol (Vitamina A), Sulfato Cúprico (Cobre), D-Biotina (Biotina), Cianocobalamina (Vitamina B12), Ácido Ortosilícico estabilizado em cloreto de coline (Silício), Beterraba em pó, Acidulante, Ácido Cítrico, Aromas naturais de limão e framboesa, Edulcorante, glicosídeos de esteviol e Antiumectante Dióxido de Silício.</p><br>
                <p><strong>NÃO CONTÉM GLÚTEN.</strong></p>
                <strong>ALÉRGICOS:</strong>  PODE CONTER LEITE, PEIXE E SOJA. <br>
                "Por conter ingredientes naturais, este produto pode sofrer pequenas variações sensoriais de cor, sabor e odor conforme safra".

            </div>
            <div class="col-md-5 tabela2">
                <span class="fruits">
                   <p> YELLOW FRUITS</p>
                </span>
                <p><strong>Ingredientes:</strong>  Polidextrose, Peptídeos bioativos de colágeno hidrolisado com peso molecular médio de 2kDa (Verisol®), Hialuronato de sódio obtido pela fermentação de streptococcus zoopidemicus (Ácido hialurônico), Ácido ascórbico (Vitamina C), D-Pantotenato de cálcio (Ácido pantotênico), Bisglicinato de zinco (Zinco), Cloridrato de piridoxina (Vitamina B6), Sulfato de manganês (Manganês), Acetato de retinol (Vitamina A), Sulfato cúprico (Cobre), D-Biotina (biotina), Cianocobalamina (Vitamina B12), Ácido ortosilícico estabilizado em cloreto de colina (Silício), Acidulante ácido cítrico, Aroma natural de Baunilha, Aroma idêntico ao natural de Pêssego, Aroma idêntico ao natural de Manga, Edulcorante glicosídeos de esteviol, e Antiumectante dióxido de silício </p><br>
                <p><strong>NÃO CONTÉM GLÚTEN.</strong> </p>
                <strong>ALÉRGICOS:</strong>  PODE CONTER LEITE, PEIXE E SOJA. <br>
                "Por conter ingredientes naturais, este produto pode sofrer pequenas variações sensoriais de cor, sabor e odor conforme safra".
            
            </div>

        </div>
    </div>
</template>

<script> 

import saboresColageno from './sabores-colageno.vue'
import TabelaNutricionalPlus from './tabela-nutricional-plus.vue'
 
 export default {
  components: { saboresColageno,  TabelaNutricionalPlus },
    name: 'BlocoSabores',

      data() {
            return {
                selected: 1,
                selectSabor: 1
            }
        },

   
 }

</script>

<style scoped>

    .tabela1 {
        border: 1px solid;
        padding: 12px ;
        border-color: #951837;
        border-radius: 5px;
        padding-right: 5px;
        width: 700px;
        margin-right: 12px;
        margin-left: 60px;
        
    }

     .tabela2 {
        border: 1px solid;
        padding: 12px;
        border-color: #F2C560;
        border-radius: 5px;
        padding-right: 5px;
        width: 700px;
        margin-right: 50px;
        margin-left: 12px;
        
        
    }

    .tabela1 p, .tabela2 p {
         font: normal normal 16px/20px Open Sans;
         color: #333333;
    }

    .btns {
        padding-left: 22%;
    }

    .lemonade {
        display: flex;
        width: 145px;
        height: 30px;
        background-color: #AF1134;
        border-radius: 5px;
        justify-content: center;
        align-items: center;
        margin-bottom: 20px;

    }

      .fruits {
        display: flex;
        width: 145px;
        height: 30px;
        background-color: #F2C560;
        border-radius: 5px;
        justify-content: center;
        align-items: center;
        margin-bottom: 20px;

    }

    .lemonade p {
        color: #ffffff;
        font: normal normal bold 16px/20px Open Sans;
        text-align: center;
    }

    .fruits p{
        color:#951837;
        font: normal normal bold 16px/20px Open Sans;
        text-align: center;
    }

    .buttons{
        padding-top: 80px;

    }

     .btn-change {
        width: 280px;
        height: 57px;
        border-radius: 5px;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        font: normal normal bold 20px/24px Open Sans;
        letter-spacing: -0.4px;
        color: #951837;
        cursor: pointer;
    }

    .btn-change-sabor {
        width: 282px;
        height: 55px;
        border: 1px solid #951837;
        border-radius: 4px;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        font: normal normal bold 24px/19px Open Sans;
        letter-spacing: -0.48px;
        color: #951837;
        cursor: pointer;
    }

    .yellowFruits:hover {
         background: #F2C560 0% 0% no-repeat padding-box; 
    }

   

    .yellowFruits {
         background: #F2C560 0% 0% no-repeat padding-box; 
    }

    .pinkLemonade {
         background: #AF1134 0% 0% no-repeat padding-box;
         color: #ffffff;
    }

    p{
     font: normal normal bold 24px/19px Open Sans;
     color: #951837;
        
    }

    .complex{
        margin-left: -8%;
    }

     @media(max-width: 768px) {

        .btns{
            padding: 0;
        }

        .complex{
            margin: 0;
        }

        .col-md-7 {
            padding: 0px 0px 0px 0px!important;
        }

        .buttons{
            padding-top: 60px
        }
   
        .btn-change-sabor {
        width: 240px;
        height: 50px;
    }

    .tabela1, .tabela2{
        margin: 12px 12px;
        width: 85% !important;
    }

    .tabela1, .tabela2{
        margin-left: 7%;
    }

     }

</style>