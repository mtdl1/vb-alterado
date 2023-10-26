<template>
        <header class="mob">
            <!-- <div class="row bg-light justify-content-center align-items-center py-3">Frete Especial Brasil e até 12x sem juros</div> -->
            <div class="w-100 d-flex justify-content-center align-items-center py-4 px-3 position-relative">
                <a href="/">
                    <img class="logoMob" src="@/assets/img/logo/VIVA LOGO.svg" alt="">
                </a>
                <div class="d-flex align-items-center position-absolute icons-menu-left fa-solid">
                    <img src="@/assets/img/icones/menu-mobile.svg" alt="" width="30">
                </div>
                <div class="d-flex align-items-center position-absolute icons-menu-right">
                    <a href="/checkout/carrinho/" class="position-relative mx-2" @click.prevent="openCarrinho()">
                        <img src="@/assets/img/icones/CARRINHO.svg" alt="" width="30">
                        <div class="headerContainerTop-carrinho-num position-absolute" v-if="dadosCarrinho.quantidadeItens"> {{ dadosCarrinho.quantidadeItens }} </div>
                    </a>
                </div>
            </div>

            <div class="overlayMenu"></div>
            <ul class="itensMenu pt-2">
                <div class="position-absolute text-right close-menu">
                    <i class="fa-solid fa-xmark"></i>
                </div>
                <div class="col-12 pb-4 text-right">
                    <a href="/checkout/acesso" class="pr-3">
                        <i class="fa fa-user-o" style="font-size: 25px" aria-hidden="true"></i>
                    </a>
                </div>
                <li><a href="/">INÍCIO</a></li>
                <li><a href="/products/colageno">Colágeno Skin Complex Plus</a></li>
                <li><a href="/products/serum-facial-anti-idade">Sérum Facial Anti-Idade</a></li>
                <li><a href="/products/creme">Creme Hidratante Primer</a></li>
                <li><a href="/products/espuma-limpeza">Espuma de Limpeza Facial</a></li>
                <li><a href="/todos-produtos">Todos Produtos Viva Beauty</a></li>
                <li><a class="esgotado" href="">DETOX 360° VIVA SLIM</a></li>
                <li><a href="https://blog.vivabeauty.com.br/">BLOG VIVA BEAUTY</a></li>
                <li><a href="/pages/contact">CONTATO</a></li>
            </ul>
        </header>
</template>

<script>
    import comunicacao from "@/comunicacao.js";
    import { mapState, mapMutations } from 'vuex';

    export default {
        data() {
            return {
                showSearch: false,
                wrapperMob: false,
                config: false,
                dadosCarrinho: false,
                linkTarja: '/products/tratamento-anti-idade-7-em-1-skin-complex-plus-com-colageno-verisol-acido-hialuronico-silicio-organico',
            };
        },

        components: {
        },

        computed: {
            ...mapState(['screenWidth', 'menuLoaded', 'dadosUser'])
        },

        methods: {
            ...mapMutations(['changeStatusMenu']),
            openMenu() {
                comunicacao.$emit("openMenu");
            },

            openCarrinho() {
                comunicacao.$emit("toggleCarrinho", {
                    show: true
                });
            },
        },

        mounted() {
            var icon = document.querySelectorAll('.fa-solid');
            var overlay = document.querySelector('.overlayMenu');
            var menu = document.querySelector('.itensMenu');
            icon.forEach(element => {
                element.addEventListener('click', () => {
                    overlay.classList.toggle('activeOverlay');
                    menu.classList.toggle('activeMenu');
                });
            });

            overlay.addEventListener('click', () => {
                overlay.classList.toggle('activeOverlay');
                menu.classList.toggle('activeMenu');
            });

            comunicacao.$on("updateSubTotal", (response) => {
                this.subTotalCarrinho = response.valor;
            });

            this.$requestSend("get", "/v2/front/checkout/cart", {}, (success, response) => {
                this.dadosCarrinho = response.data;
                if (response.data && response.data.subtotal && response.data.subtotal.valor) {
                    this.dadosSubTotal = response.data.subtotal.valor;
                }
                comunicacao.$emit("carrinhoCarregado", response.data);
            });

            comunicacao.$on("configCarregada", (response) => {
                this.config = response.configuracoes;
            });

            this.$requestSend("get", "/v2/front/checkout/cart", {}, (success, response) => {
                this.dadosCarrinho = response.data;
                comunicacao.$emit("carrinhoCarregado", response.data);
            });
        },

        created() {
            comunicacao.$on("updateNumCarrinho", (qtd) => (this.dadosCarrinho.quantidadeItens = qtd));
            if (window.location.href.indexOf("/products/tratamento-anti-idade-7-em-1-skin-complex-plus-com-colageno-verisol-acido-hialuronico-silicio-organico") > -1) {
                this.linkTarja = "#KitProduto";
            }
        },
};
</script>

<style lang="scss" scoped>
video{
    max-width: 100%;
}
    .bg-light {
        background-color: #e4c9bf !important;
        font-family: 'Poppins', sans-serif;
    }

    .icons-menu-right {
        right: 25px;
        top: 35%;
    }
    
    .icons-menu-left {
        left: 25px;
        top: 35%;
    }

    .close-menu {
        right: -40px;
        top: 10px;
    }

    .close-menu i {
        color: #fff;
        font-size: 30px;
    }

    .esgotado {
        color: #777;
    }

    .itensMenu {
        transition: 0.5s ease;
        position: fixed;
        width: 0;
        height: 0;
        left: -200%;
        background-color: #fff;

        li {
            list-style-type: none;
            border-top: 1px solid #eee;
        }

        a {
            text-decoration: none;
            font-size: 14px;
            display: block;
            height: 100%;
            padding: 15px 0px 15px 20px;
        }
    }

    .itensMenu {
        left: -200%;
        top: 0;
    }

    .itensMenu.activeMenu {
        width: 70vw;
        height: 100vh;
        left: 0;
        top: 0;
        z-index: 99999;

    }

    .overlayMenu {
        transition: 0.5s ease;
        width: 100vw;
        height: 100%;
        position: fixed;
        top: 0;
        left: -200%;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 99999;
    }

    .overlayMenu.activeOverlay {
        left: 0;
        top: 0;
        z-index: 999;
    }

    .logoMob {
        position: relative;
        width: 88px;
    }

    .headerContainerTop-carrinho-num {
        top: -18px;
        right: -11px;
        font-size: 15px;
        color: #fff;
        background-color: #db2b4e;
        border-radius: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0;
        min-height: 20px;
        min-width: 20px;
    }

    @media screen and (max-width: 800px) {
        .mobf {
            display: flex;
            height: 75px !important;
        }

        .sectionMob {
            display: block;
        }

        .sectionMob h2 {
            font-size: 7px;
        }

        .close-search {
            font-size: 30px;
            z-index: 99;
            top: 18px;
            right: 10px;
            color: #333;
        }

        .search-button {
            filter: invert(1);
            width: 20px;
            height: 20px;
        }

        .search-mobile {
            top: -200px;
            transition: 0.5s ease;
        }

        .wrapperMob {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 9;
        }
    }
.faixa-destaque-black-friday {
    padding: 5px 0;
    background-color: #edbf2c;
}

.faixa-destaque-black-friday p {
    font-size: 14px;
    font-weight: bold;
    text-transform: uppercase;
}

.faixa-destaque-black-friday img {
    width: 15px;
    margin: 0 5px;
}
</style>