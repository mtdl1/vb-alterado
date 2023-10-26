<template>
    <div>
      <section class="container-fluid px-0  position-relative">
          <div class="container position-relative pl-0">
              <div class="row align-items-center py-3">
                <nav class="navbar navbar-expand-lg pl-0">
                      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#conteudoNavbarSuportado" aria-controls="conteudoNavbarSuportado"
                          aria-expanded="false" aria-label="Alterna navegação">
                          <i class="fa fa-bars" aria-hidden="true"></i>
                      </button>
                      <div class="collapse navbar-collapse" id="conteudoNavbarSuportado">
                          <ul class="nav">
                              <li class="nav-item dropdown">
                                  <a class="nav-link dropdown-toggle pl-0" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Produtos</a>
                                  <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                                      <a href="/products/colageno" class="dropdown-item nav-link">Colágeno Skin Complex Plus</a>
                                      <a href="/products/serum-facial-anti-idade" class="dropdown-item nav-link">Sérum Facial Anti-Idade</a>
                                      <a href="/products/espuma-limpeza" class="dropdown-item nav-link">Espuma de Limpeza Facial</a>
                                      <a href="/products/creme" class="dropdown-item nav-link">Creme Hidratante Primer</a>
                                      <a href="/todos-produtos" class="dropdown-item nav-link">Todos Produtos Viva Beauty</a>
                                  </div>
                              </li>
                          </ul>
                      </div>
                </nav>
                  <a href="/" class="navbar-brand mx-auto">
                      <img src="@/assets/img/logo/VIVA LOGO.svg" alt="" width="120">
                  </a>
                  <a href="/checkout/acesso" class="conta pr-3">
                    <p>Minha Conta</p>
                  </a>
                  <a :href="`${$siteUrl}/checkout/carrinho/`" @click.prevent="openCarrinho()" class="carrinho-icone mr-0 pr-0">
                    <img src="@/assets/img/icones/CARRINHO.svg" alt="" width="20">
                    <div class="headerContainerTop-carrinho-num" v-if="dadosCarrinho.quantidadeItens">
                      {{ dadosCarrinho.quantidadeItens }}
                    </div>
                  </a>
              </div>
          </div>
      </section>
    </div>
</template>

<script>
    import comunicacao from "@/comunicacao.js";
    import { mapState, mapMutations } from 'vuex';

    export default {
        components: {
        }, 

    data() {
      return {
        config: false,
        dadosCarrinho: false,
        linkTarja: '/products/tratamento-anti-idade-7-em-1-skin-complex-plus-com-colageno-verisol-acido-hialuronico-silicio-organico',
      };
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
        comunicacao.$emit("toggleCarrinho", { show: true });
      },
    },

    mounted() {
      comunicacao.$on("updateSubTotal", (response) => {
        this.subTotalCarrinho = response.valor;
      });

      this.$requestSend("get", "/v2/front/checkout/cart", {}, (success, response) => {
        this.dadosCarrinho = response.data;
        if ( response.data && response.data.subtotal && response.data.subtotal.valor) {
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
        }
      );
    },

    created() {
      comunicacao.$on(
        "updateNumCarrinho",
        (qtd) => (this.dadosCarrinho.quantidadeItens = qtd)
      );
      if (window.location.href.indexOf("/products/tratamento-anti-idade-7-em-1-skin-complex-plus-com-colageno-verisol-acido-hialuronico-silicio-organico") > -1) {
          this.linkTarja = "#KitProduto";
      }
    },
  };
</script>

<style scoped>
video{
    max-width: 100%;
}
.bg-light {
  background-color: #e4c9bf !important;
  font-family: 'Poppins', sans-serif;
}

.cart-count {
  right: 15%;
  top: 40px;
}

.navbar .nav-item .dropdown-menu{ 
  display: none; 
}

.navbar .nav-item:nth-child(3) .nav-link:hover {
  text-decoration: none;
}

.navbar .nav-item:hover .dropdown-menu { 
  display: block;
  width: max-content !important;
  margin-left: -10px !important;
  border: 1px solid #dbdbdb;
}

.navbar .nav-item .dropdown-menu{ 
  margin-top:0; 
}

.dropdown-menu a {
  font-weight: 500 !important;
  padding-left: 16px !important;
  text-transform: capitalize;
  font-size: 16px;
}

dropdown-toggle:hover {
  display: none;
}

.dropdown-toggle::after {
  float: right;
  margin-left: unset !important;
  border: unset !important;
  font-family: "Font Awesome 5 Free";
  font: normal normal normal 14px/1 FontAwesome;
  font-weight: 600 !important;
  content: "\f107";
  color: rgb(0, 0, 0);
  font-size: 16px;
  padding-left: 5px;
  position: relative;
  top: 0;
}

.nav-item.dropdown:hover .dropdown-toggle::after {
  content: "\f106";
}

a.nav-link {
  color: rgb(0, 0, 0);
  font-size: 16px;
  font-family: 'Open Sans', sans-serif;
  font-weight: 600;
  transition: 0.5s;
}

.dropdown-item:focus, .dropdown-item:hover {
  color: #ff4289;
  text-decoration: none;
  background-color: #FFF;
  transition: 0.5s;
}

.dropdown-item.active, .dropdown-item:active {
  color: #fff;
  text-decoration: none;
  background-color: #ff4289;
}

.headerContainerTop-carrinho-num {
  position: absolute;
  top: 25%;
  right: 0.5%;
  font-size: 10px;
  color: #fff;
  background-color: #d72a4c;
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2px 6px;
}

svg.icon-inline.icon-2x {
  filter: invert(1);
}

.conta p{
  color: #000;
  font-size: 16px;
  font-family: 'Open Sans', sans-serif;
  font-weight: 600;
  text-transform: capitalize;
  transition: 0.5s;
}

.conta p:hover{
  color: #ff4289;
  text-decoration: none;
  transition: 0.5s;
}

.carrinho-icone{
  transition: 0.5s;
}

.carrinho-icone:hover{
  transform: scale(1.1);
  transition: 0.5s;
}

@media(max-width: 768px) {
    button.navbar-toggler {
      position: absolute;
      left: 43vw;
      top: -9vh;
  }

  .navbar-collapse {
      background: rgb(153, 153, 153);
  }
}

.faixa-destaque-black-friday {
  padding: 5px 0;
  background-color: #edbf2c;
  color: #000;
  font-weight: bold;
  width: 400%;
  margin-left: -60px;
}

.faixa-destaque-black-friday p {
  width: fit-content;
  display: inline-block;
  padding: 0 10px;
  font-size: 14px;
  text-transform: uppercase;
}

.faixa-destaque-black-friday img {
  width: 15px;
  margin-left: 5px;
}
</style>