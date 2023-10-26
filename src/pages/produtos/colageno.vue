<template>
  <div>
    <BannerSerum />
    <BeneficiosColageno class="py-5" />
    <AntesDepoisColageno class="py-5" />
    <ResultadosColageno class="py-5" />
    <VitrineColageno class="py-5" />
    <ConcorrenciaColageno class="py-5" />
    <FormulaColageno class="py-5" />
    <ConsumirColageno class="py-5" />
    <FamosasAprovam class="py-5" />
    <VideoColageno class="py-5" />
    <BannerDesafio />
    <PerguntasFrequentesColageno class="py-5" />
    <BotaoCompreAgora class="mob" />
  </div>
</template>

<script>
import { mapMutations } from "vuex";

import VitrineColageno from "../../components/common/vitrines/vitrine-colageno.vue";
import BannerDesafio from "../../components/gerais/banners/banner-desafio.vue";
import AntesDepoisColageno from "../../components/gerais/colageno/antes-depois-colageno.vue";
import BeneficiosColageno from "../../components/gerais/colageno/beneficios-colageno.vue";
import ConcorrenciaColageno from "../../components/gerais/colageno/concorrencia-colageno.vue";
import ConsumirColageno from "../../components/gerais/colageno/consumir-colageno.vue";
import FormulaColageno from "../../components/gerais/colageno/formula-colageno.vue";
import ResultadosColageno from "../../components/gerais/colageno/resultados-colageno.vue";
import VideoColageno from "../../components/gerais/colageno/video-colageno.vue";
import PerguntasFrequentesColageno from "../../components/gerais/perguntas-frequentes/perguntas-frequentes-colageno.vue";
import BannerSerum from "../../components/gerais/serum/banner-serum.vue";
import FamosasAprovam from "../../components/gerais/serum/famosas-aprovam.vue";
import BotaoCompreAgora from "../../components/ui/buttons/botao-compre-agora.vue";

export default {
  name: "PageColageno",

  components: {
    BeneficiosColageno,
    BannerSerum,
    AntesDepoisColageno,
    ResultadosColageno,
    ConcorrenciaColageno,
    FormulaColageno,
    ConsumirColageno,
    FamosasAprovam,
    VideoColageno,
    BannerDesafio,
    PerguntasFrequentesColageno,
    VitrineColageno,
    BotaoCompreAgora,
  },

  data() {
    return {
      loading: {
        geral: true,
        banner: true,
      },
    };
  },

  methods: {
    ...mapMutations(["changeDadosPageAtual"]),
  },

  created() {
    this.$requestSend("get", "/v2/front/url/home", {}, (success, response) => {
      if (success) {
        //definindo manualmente os atributos de SEO
        response.data.estrutura.seo.canonical = "https://www.vivabeauty.com.br/products/colageno";
        response.data.estrutura.seo.title = "Colágeno Skin Complex Plus | Viva Beauty";
        response.data.estrutura.seo.description = "Colágeno Skin Complex Plus";
        this.loading.geral = false;
        this.$aplicaSEO(response.data.estrutura);
        this.changeDadosPageAtual(response.data);
      }
    });
  },
};
</script>