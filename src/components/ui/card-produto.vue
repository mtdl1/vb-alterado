<template>
	<div class="box-produto">
		<div class="header-produto d-flex flex-column justify-content-center" :class="{bgPink: header == 'bgPink' }">
			<p class="nome" v-html="produto.nomeProduto"></p>
			<p>{{ produto.subtituloProduto }}</p>
		</div>
		<div class="body-produto d-flex">
			<div class="col-produto w-50 d-flex justify-content-center align-items-center position-relative">
				<div v-if="produto.quantidadeProduto > 1" class="pote-preco position-absolute"><strong>R$ {{((produto.precoPor/produto.quantidadeProduto).toFixed(2)).toString().replace(".", ",")}}</strong> cada pote</div>
				<div class="d-flex">
					<img v-show="!trocaImagem" class="img-fluid" :src="require(`@/${produto.img}`)"  alt="" title="" loading="lazy" />
					<img v-show="trocaImagem" class="img-fluid" :src="require(`@/${imgTroca}`)"  alt="" title="" loading="lazy"  />
				</div>
			</div>
			<div class="col-produto w-50 pl-2 d-flex flex-column justify-content-between" :class="{alinhapreco: !produto.possuiVariacao}">
				<div class="d-flex" :class="{removeFrete: produto.removeFreteGratis}">
					<div class="col-desconto text-center w-50 d-flex align-items-center justify-content-center py-2">
						<strong>{{ (Math.floor(100 - (produto.precoPor*100)/produto.precoDe)) }}% OFF</strong>
					</div>
					<!-- <div class="col-frete text-center w-50 d-flex align-items-center justify-content-center py-2"> -->
					<div :class="['col-frete text-center w-50 d-flex align-items-center justify-content-center py-2']">
						<strong>FRETE GRÁTIS</strong>
					</div>
				</div>
				<div class="mb-2 pt-1">
					<div class="precos-geral">
						<div class="d-flex justify-content-start pr-3 pt-3 ">
							<p class="preco-de">
								de:
								<s class="mr-4">
									{{ produto.precoDe.toLocaleString('pt-br', { style: 'currency', currency: 'BRL' })}}
								</s>
							</p>
						</div>
						<div class="preco-produto pr-3">
							<p class="parcelamento">até <strong>8x sem juros</strong> de</p>
							<p class="produto">{{ (produto.precoPor/8).toLocaleString('pt-br', { style: 'currency', currency: 'BRL' }) }}</p>
							<p class="avista">ou <strong>{{ produto.precoPor.toLocaleString('pt-br', { style: 'currency', currency: 'BRL' }) }}</strong> à vista <br class="desk"> </p>
						</div>
					</div>
					<div class="form-group select_sabores w-100 pr-3 my-1 mt-2" v-if="produto.possuiVariacao">
						<select name="saboresColagProd3" class="select_option browser-default custom-select" id="saboresColagProd3" @change="onChange($event)" v-model="sabores">
							<option class="option" value="0">Escolha o Sabor</option>
							<option class="option" :value="item.id" v-for="item, i in produto.variacoes" :key="i">{{item.nome}}</option>
						</select>
					</div>
					<div class="mt-2 pr-3">
						<a @click="addCartBoxCompra();" class="d-flex align-items-center justify-content-center add-to-cart mb-2 w-100 text-white"> Compre agora </a>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import Comunicacao from "@/comunicacao.js"
export default {
  name: 'CardProduto',
  props: {
    produto: {
      type: Object,
      required: true
    },
		header: {
			type: String,
			default: ''
		}
  },
  data(){
		return {
			sabores: 0,
			imgTroca: 'assets/img/produtos/produto_skincomplex_mob2.png',
			trocaImagem: false,
			boxCompraCarrinho: {
				tipo: "lista",
				itens: [
					{		
						idProduto: 0,
						idAtributoSimples: "0",
						idUnidadeVenda: "0",
						idArmazem: "0",
						quantidade: "1",
						adicional: "",
						parametros: ""
					},
				]
			},
		}
	},

  methods: {
		onChange(event) {
			this.trocaImagem = true;
			this.sabores = event.target.value;

			// 1 Pote Colágeno Verisol®
			if(this.sabores == 201){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-Colageno-Verisol-Pink-Lemonade.jpg';
			}
			if(this.sabores == 218){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-Colageno-Verisol-Yellow-Fruits.jpg';
			}
			// 1 Pote Colágeno Verisol®

			// 2 Potes Colágeno Verisol® + Serum Facial
			if(this.sabores == 202){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-2-Potes-Colageno-Verisol-Pink-Lemonade+Brinde.jpg';
			}
			if(this.sabores == 219){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-2-Potes-Colageno-Verisol-Yellow-Fruits+Brinde.jpg';
			}
			if(this.sabores == 221){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-2-Potes-Colageno-Verisol-Pink-Lemonade-Yellow-Fruits+Brinde.jpg';
			}
			// 2 Potes Colágeno Verisol® + Serum Facial

			// 4 Potes Colágeno Verisol® + Serum e Espuma de Limpeza Facial
			if(this.sabores == 203){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-4-Potes-Colageno-Verisol-Pink-Lemonade+Brinde.jpg';
			}
			if(this.sabores == 220){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-4-Potes-Colageno-Verisol-Yellow-Fruits+Brinde.jpg';
			}
			if(this.sabores == 222){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-4-Potes-Colageno-Verisol-Pink-Lemonade-Yellow-Fruits+Brinde.jpg';
			}
			// 4 Potes Colágeno Verisol® + Serum e Espuma de Limpeza Facial

			// 2 Potes Colágeno Verisol® + Tratamento Ideal
			if(this.sabores == 227){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-2-Potes-Colageno-Verisol-Pink-Lemonade+Espuma+Serum+Creme.jpg';
			}
			if(this.sabores == 228){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-2-Potes-Colageno-Verisol-Yellow-Fruits+Espuma+Serum+Creme.jpg';
			}
			if(this.sabores == 229){
				this.imgTroca = 'assets/img/produtos/colageno/Viva-Beauty-Produtos-Kits-2-Potes-Colageno-Verisol-Yellow-Pink+Espuma+Serum+Creme.jpg';
			}
			// 2 Potes Colágeno Verisol® + Tratamento Ideal
			
		},

		addCartBoxCompra() {

			if(this.produto.possuiVariacao){
				var Produto = this.sabores
				this.boxCompraCarrinho.itens[0].idProduto = Produto
			} else {
				this.boxCompraCarrinho.itens[0].idProduto = this.produto.idProduto
			}

			let {tipo, itens} = this.boxCompraCarrinho
			let itemAdc       = false
			if (tipo && itens) {
					this.$carrinho.add(tipo,itens,(success, response) => {
							response.data.itens.forEach(prod => {
									itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho.itens[0].idProduto
							})
							if(success){
									if (Produto == 0) this.$toast.error("Selecione um sabor para adicionar ao carrinho!")
									else return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data })
							}
							this.changeDadosPageAtual(response.data)
							this.$toast.error("Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.")
					})
				return
			}
		},
	},
}

</script>

<style scoped>
.bgPink {
	background-color: #DB2B4E!important;
}

.box-produto {
	border-radius: 18px;
	overflow: hidden;
	border: 1px solid #dadada;
}

.pote-preco {
	font-size: 14px;
	color: #898989;
	background: #e9e9e9;
	left: 0;
	top: 10px;
	padding: 8px;
	border-radius: 0 20px 20px 0;
}

.header-produto {
	padding: 14px;
	height: 65px;
	background-color: #333;
}

.header-produto .nome {
	color: #fff;
	font-size: 20px;
	font-family: "Open Sans", sans-serif;
	text-align: center;
	font-weight: 600 !important;
	line-height: 24px;
}

.header-produto p {
	color: #fff;
	text-align: center;
	font-size: 13px;
	font-weight: normal;
	font-family: "Open Sans", sans-serif;
	line-height: 17px;
}

.col-desconto {
	background: #fffc00;
	color: #333333;
	font-size: 13px;
}

.col-frete {
	background: #DB2B4E;
	color: #fff;
	font-size: 13px;
}

.removeFrete .col-frete {
    display: none!important;
}

.removeFrete {
    justify-content: end;
}

b, strong {
    font-weight: 600;
		letter-spacing: 1px!important;
}

.preco-produto .nome {
	font-family: "Open Sans", sans-serif;
	font-weight: normal!important;
	color: #000;
	font-size: 14px;
}

.preco-produto .produto {
	font: normal normal bold 36px/15px Helvetica;
	letter-spacing: -1.44px;
	color: #333333;
	padding: 10px 0;
}

.preco-produto .produto span{
	font: normal normal normal 14px/15px Helvetica;
	letter-spacing: -0.96px;
	color: #18A851;
}

.alinhapreco .precos-geral {
    margin-bottom: 20%;
}

.preco-de , .preco-de s{
	font-size: 14px !important;
	margin-right: 0 !important;
	color: #333333;
	font: normal normal 300 16px/13px Helvetica;
	letter-spacing: -0.64px;
}

.parcelamento {
	font: normal normal normal 12px/13px Helvetica;
	letter-spacing: -0.48px;
	color: #333333;
}

.avista{
	font: normal normal normal 16px/13px Helvetica;
	letter-spacing: -0.64px;
	color: #333;
}

.add-to-cart {
	background-color: #18A851;
	font: normal normal bold 18px/22px Helvetica;
	font-family: "Open Sans", sans-serif;
	letter-spacing: -0.02px;
	color: #FFFFFF;
	width: 73%;
	height: 60px;
	border-radius: 6px;
	border: none;
	cursor: pointer;
	transition: 0.4s ease;
	text-align: center;
	outline: none;
	margin-top: 10px;
}

.add-to-cart:hover {
    opacity: 0.8;
}

.pote-preco {
    font-size: 14px;
    color: #898989;
    background: #e9e9e9;
    left: 0;
    top: 10px;
    padding: 8px;
    border-radius: 0 20px 20px 0;
}

.d-flex.justify-content-start.pr-3.pt-3 {
    align-items: center!important;
}

img{
	padding: 15px;
}

.body-produto {
    background-color: #FFF;
}

.custom-select{
	font-size: 14px;
}

.custom-select option{
	font-size: 14px;
}

@media (max-width: 768px) {
	.mb-2.mt-5.pt-1 {
    margin-top: 0!important;	
	}

	.box-produto {
		width: 100%;
		border-radius: 8px;
		overflow: hidden;
	}

	.pr-3 {
		padding-right: 10px !important;
	}

	.header-produto .nome {
		font-size: 17px;
	}

	.header-produto {
		height: 65px;
	}

	.header-produto p {
		font-size: 13px;
		line-height: 18px;
	}

	.col-desconto,
	.col-frete {
		font-size: 10px;
	}

	.precos-geral p{
		margin: 4px 0!important;
	}

	.preco-de,
	.preco-por {
		font-size: 14px !important;
	}

	.preco-por {
		padding-left: 8px;
	}

	.preco-de s {
		font-size: 14px !important;
		margin-right: 0 !important;
	}

	.preco-produto .produto {
		font-size: 30px !important;
		padding: 5px 0;
	}
	

	.preco-produto .produto span {
		font-size: 14px !important;
	}

	.preco-produto p{
		font-size: 11px !important;
		line-height: 16px;
	}

	.add-to-cart {
		font-size: 14px !important;
		height: 45px;
	}

	.col-produto.w-50.p-4 {
		padding: 0 !important;
	}

	.custom-select{
		font-size: 12px;
	}
}
@media (max-width: 380px) {
	.preco-de, .preco-de s {
		font-size: 14px !important;
	}

	select{
		font-size: 10px !important;
	}
}
</style>