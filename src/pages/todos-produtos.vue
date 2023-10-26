<template>
    <div>
        <BannerProdutos />
        <VitrineTodosProdutos />
    </div>
</template>

<script>
import { mapMutations } from "vuex";
import VitrineTodosProdutos from '../components/common/vitrines/vitrine-todos-produtos.vue';
import BannerProdutos from '../components/gerais/banners/banner-produtos.vue';

export default {
    name: "TodosProdutos",

    components: {
        VitrineTodosProdutos,
        BannerProdutos
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
            response.data.estrutura.seo.canonical =
            "https://www.vivabeauty.com.br/todos-produtos";
            response.data.estrutura.seo.title =
            "Todos os Produtos | Viva Beauty";
            response.data.estrutura.seo.description = "Todos os Produtos da Viva Beauty";
            this.loading.geral = false;
            this.$aplicaSEO(response.data.estrutura);
            this.changeDadosPageAtual(response.data);
        }
        });
    },
    };
</script>