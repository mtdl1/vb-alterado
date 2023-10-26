<template>
    <div class="bg-alt">
        <div class="container">
            <div class="row">
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-serum/formula-vegana.svg" alt="" class="img-fluid">
                    <p>Fórmula vegana</p>
                </div>
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-serum/Cruelty free.svg" alt="" class="img-fluid">
                    <p>Cruelty free</p>
                </div>
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-serum/Sem parabenos.svg" alt="" class="img-fluid">
                    <p>Sem parabenos</p>
                </div>
                <div class="col-4 col-md-2 baixo">
                    <img src="@/assets/img/beneficios-serum/SEM SULFATOS.svg" alt="" class="img-fluid">
                    <p>Sem sulfatos</p>
                </div>
                <div class="col-4 col-md-2 baixo">
                    <img src="@/assets/img/beneficios-serum/SEM SILICONE.svg" alt="" class="img-fluid">
                    <p>Sem silicone</p>
                </div>
                <div class="col-4 col-md-2 baixo">
                    <img src="@/assets/img/beneficios-serum/SEM PETROLATOS.svg" alt="" class="img-fluid">
                    <p>Sem petrolatos</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'BeneficiosSerum',
    }
</script>

<style scoped>
.bg-alt {
    background-color: #F9B5C3;
}
.col-md-2 {
    text-align: center;
}
p{
    text-align: center;
    font: normal normal bold 18px/22px Open Sans;
    letter-spacing: 0px;
    color: #FFFFFF;
    margin-top: 13px;
}

@media(max-width: 768px) {
    .col-4{
        margin-bottom: 40px;
        padding: 0;
    }

    .baixo{
        margin-bottom: 0;
    }

    p{
        font: normal normal bold 18px/18px Open Sans;
        letter-spacing: 0px;
    }
}
</style>