<template>
    <v-container class="elevation-2">
        <h4><b>Ofertas pra você</b></h4>
        <v-row class="mt-1">
            <v-col v-for="(oferta, i) in ofertas" :key="i" cols="6">
                <v-card class="offer-card" elevation="2" @click="handleCardClick(oferta)" height="160">
                    <v-img :src="oferta.imagem" :alt="oferta.titulo" cover />
                    
                    <v-card-actions class="d-flex flex-column">
                        <v-chip color="pink" label>
                            <v-icon icon="mdi-label" start></v-icon>
                            {{oferta.desconto}}
                        </v-chip>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
        <br>

        <a href="" style="text-decoration: none;">Ver todas as ofertas</a>
    </v-container>
</template>

<script setup>
function handleCardClick(oferta) {
    console.log('Oferta selecionada:', oferta.titulo)
}

const ofertas = [
    { titulo: 'Oferta 1', imagem: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', desconto: '20% off' },
    { titulo: 'Oferta 2', imagem: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', desconto: '35% off' },
    { titulo: 'Oferta 3', imagem: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', desconto: '15% off' },
    { titulo: 'Oferta 4', imagem: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', desconto: '50% off' },
]
</script>

<style scoped>
.offer-card {
    width: 100%;
    height: 150px;
    border-radius: 8px;
    overflow: hidden;
    cursor: pointer;
}
</style>