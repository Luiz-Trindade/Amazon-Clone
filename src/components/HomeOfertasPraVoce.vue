<template>
    <v-container class="elevation-2">
        <h4><b>Ofertas pra você</b></h4>
        <v-row class="mt-1" dense>
            <v-col
                v-for="(oferta, i) in ofertas"
                :key="i"
                cols="6"
                sm="6"
                md="4"
                lg="3"
                class="d-flex"
            >
                <v-card
                    class="offer-card"
                    elevation="2"
                    @click="handleCardClick(oferta)"
                >
                    <v-img
                        :src="oferta.imagem"
                        :alt="oferta.titulo"
                        cover
                        height="120"
                    />
                    <v-card-actions class="d-flex flex-column align-start px-2 py-1">
                        <v-chip color="pink" label size="small">
                            <v-icon icon="mdi-label" start></v-icon>
                            {{ oferta.desconto }}
                        </v-chip>
                        <span class="oferta-titulo mt-1">{{ oferta.titulo }}</span>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
        <div class="text-left mt-2">
            <a href="#" style="text-decoration: none;">Ver todas as ofertas</a>
        </div>
    </v-container>
</template>

<script setup>
import { ref } from 'vue'

const ofertas = ref([
    { titulo: 'Oferta 1', imagem: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', desconto: '20% off' },
    { titulo: 'Oferta 2', imagem: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', desconto: '35% off' },
    { titulo: 'Oferta 3', imagem: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', desconto: '15% off' },
    { titulo: 'Oferta 4', imagem: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', desconto: '50% off' },
    // Adicione mais ofertas dinamicamente se desejar
])

function handleCardClick(oferta) {
    console.log('Oferta selecionada:', oferta.titulo)
}
</script>

<style scoped>
.offer-card {
    width: 100%;
    min-height: 180px;
    border-radius: 8px;
    overflow: hidden;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: box-shadow 0.2s;
}
.offer-card:hover {
    box-shadow: 0 4px 20px rgba(0,0,0,0.12);
}
.oferta-titulo {
    font-size: 1rem;
    font-weight: 500;
    color: #333;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    max-width: 120px;
}
@media (max-width: 600px) {
    .oferta-titulo {
        max-width: 90px;
        font-size: 0.95rem;
    }
}
</style>