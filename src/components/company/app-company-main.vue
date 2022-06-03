<template>
    <v-main>
        <v-card class="d-none d-sm-flex">
            <v-row no-gutters>
                <v-col v-for="i in 2" :key="{i}">
                    <template v-if="i === 1">
                        <v-card-title> {{ title }} </v-card-title>
                        <v-spacer></v-spacer>
                    </template>
                    <template v-else-if="i === 2">
                        <v-breadcrumbs :items="items" class="d-flex justify-end">
                        </v-breadcrumbs>
                    </template>
                </v-col>
            </v-row>
        </v-card>
        <v-container>
            <v-row>
                <v-col>
                    <v-img src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg"
                        gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"></v-img>
                    <h3>CCA Construction</h3>
                    <p>
                        Одна из наиболее опытных и уважаемых строительных компаний Восточной Европы. Уже более 100 лет
                        мы
                        воплощаем мечты заказчиков о качественном и доступном жилье.
                        <span class="font-italic">
                            Наши главные приоритеты: безопасность, функциональность и эстетика во всем.
                        </span>
                        Начиная с 1906 года и по настоящее время, мы выросли из небольшой строительной фирмы в надежного
                        поставщика строительных услуг международного масштаба.
                        <span class="font-italic">
                            Главный офис компании находится в Москве, филиалы – в Варшаве, Киеве, Бухаресте, Праге и
                            Братиславе.
                        </span>
                        Общее количество сотрудников насчитывает более 4500 человек. В наш портфель входят проекты
                        разного
                        уровня сложности – 1
                        <span class="font-italic">
                            небольших жилых комплексов до крупных промышленных предприятий.
                        </span>
                        Этому успеху мы обязаны своим сотрудникам. Благодаря их исключительному профессионализму и
                        приверженности общему делу,
                        <span class="font-italic">
                            мы можем реализовывать самые сложные и нестандартные проекты.
                        </span>
                    </p>
                </v-col>
            </v-row>
        </v-container>
    </v-main>
</template>
<script>
    export default {
        data: () => {
            return {
                title: document.title,
                items: [{
                        text: "Главная",
                        href: "/",
                        disabled: false,
                    },
                    {
                        text: "Компания",
                        href: "/company",
                        disabled: false,
                    },
                ]
            }
        }
    }
</script>
<style lang="scss">
    .v-breadcrumbs {
        &__item {
            color: black !important;

            &:hover {
                color: #6A1B9A !important;
                border-radius: .25rem;
                border-width: 1px;
                border-style: groove;
                border-color: #6A1B9A;
                -webkit-box-shadow: 12px 18px 35px 27px rgba(152, 29, 227, 0.23);
                -moz-box-shadow: 12px 18px 35px 27px rgba(152, 29, 227, 0.23);
                box-shadow: 12px 18px 35px 27px rgba(152, 29, 227, 0.23);
            }
        }
    }
</style>