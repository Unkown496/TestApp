<template>
    <v-main>
        <v-container fluid class="pa-0">
            <v-row no-gutters>
                <v-col v-for="i in 3" :key="{ i }">
                    <template v-if="i === 1">
                        <v-carousel hide-delimiters show-arrows-on-hover height="250">
                            <v-carousel-item v-for="(item,i) in itemsMain" :key="i" :src="item.src"></v-carousel-item>
                        </v-carousel>
                        <v-card outlined elevation="2" color="grey lighten-3">
                            <v-card-title> Sparcl Deco Star</v-card-title>
                            <v-card-text> Команда людей – нацеленная на высокое исполнение своей работы </v-card-text>
                        </v-card>
                    </template>
                    <template v-else-if="i === 2">
                        <v-card outlined elevation="0" class="pa-4 mb-15">
                            <v-card-title class="text-decoration-underline"> Услуги </v-card-title>
                            <v-row>
                                <v-col v-for="(item,i) in itemsJobs" :key="i" :src="item.src" cols="6" sm="3" lg="2"
                                    class="d-flex justify-center">
                                    <v-hover>
                                        <template v-slot:default="{ hover }">
                                            <v-card class="d-flex flex-column align-center" max-width="auto">
                                                <v-img :lazy-src="item.src" :src="item.src" height="100px">
                                                </v-img>
                                                <v-card-title class="px-0 pt-0"> {{ item.title }} </v-card-title>
                                                <v-fade-transition>
                                                    <v-overlay v-if="hover" absolute color="deep-purple">
                                                        <v-btn outlined small dark class="mx-auto">Подробнее</v-btn>
                                                    </v-overlay>
                                                </v-fade-transition>
                                            </v-card>
                                        </template>
                                    </v-hover>
                                </v-col>
                            </v-row>
                        </v-card>
                    </template>
                    <template v-else-if="i === 3">
                        <v-card light elevation="2" class="pa-5" color="grey lighten-3">
                            <v-card-title class="justify-center"> ОТЗЫВЫ НАШИХ КЛИЕНТОВ </v-card-title>
                            <v-card-text class="text-center">Наши клиенты рассказывают о нас и нашей работе.
                            </v-card-text>
                            <v-btn dark class="mx-auto d-block">
                                Больше отзывов
                                <v-icon right dark>
                                    mdi-arrow-right
                                </v-icon>
                            </v-btn>
                        </v-card>
                    </template>
                </v-col>
            </v-row>
        </v-container>
    </v-main>
</template>
<script>
    export default {
        data() {
            return {
                itemsMain: [{
                        src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
                    },
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
                    },
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
                    },
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
                    },
                ],
                itemsJobs: [{
                        title: "Хелпер",
                        src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',

                    },
                    {
                        title: "test",
                        src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
                    },
                    {
                        title: "test1",
                        src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
                    }
                ]
            }
        },
    }
</script>
<style lang="scss">
    .v-application--wrap {
        max-width: 120% !important;
    }
</style>