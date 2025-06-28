<template>
    <v-container
        style="background-image: linear-gradient(to top, rgba(255,255,255,1) 30%, rgba(0,0,0,0) 50%), url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=800&q=80'); background-size: cover; background-position: center; height: 400px;">
        <v-sheet class="mx-auto mb-4" style="border-radius: 10px; background-color: transparent;">
            <v-slide-group :show-arrows="false" style="margin-top: 200px; padding: 5px;">
                <v-slide-group-item v-for="(category, i) in categories" :key="i" v-slot="{ isSelected, toggle }">
                    <v-btn :color="isSelected ? 'primary' : undefined" class="ma-1" rounded="10" elevation="1"
                        @click="toggle" style="width: 100px; height: 160px;">
                        <v-row>
                            <v-col
                                style="display: flex; align-items: center; justify-content: center; flex-direction: column;">
                                <span class="text-caption" style="white-space: pre-line; text-align: left; font-size: 12px !important;">
                                    Continue
                                    comprando...
                                </span>
                                <v-img :lazy-src="category.img" :src="category.img" height="100" width="80" class="mb-2"
                                    cover rounded />
                            </v-col>
                        </v-row>
                    </v-btn>
                </v-slide-group-item>
            </v-slide-group>
        </v-sheet>
    </v-container>
</template>


<script setup>
const categories = [
    { img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', label: 'Sunshine' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', label: 'Road' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', label: 'House' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', label: 'Sunshine' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', label: 'Road' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', label: 'House' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', label: 'Sunshine' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', label: 'Road' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', label: 'House' },
    // Adicione mais categorias conforme necessário
]
</script>