<template>
    <v-main>
        <sub-app-breadcrumbs :title="'Реквизиты'" :items="items"></sub-app-breadcrumbs>
        <v-container class="mb-10">
            <v-row>
                <v-col v-for="n in 3" :key="{ n }" cols="12">
                    <template v-if="n === 1">
                        <h3 class="text-decoration-underline">
                            Sparcl Deco Star
                        </h3>
                    </template>
                    <template v-else-if="n === 2">
                        Здесь вы найдете реквизиты нашей компании. Если будет необходима дополнительная информация,
                        пожалуйста, обратитесь к нам по телефону: +7 (499) 394-04-45 или отправьте электронное письмо:
                        hello@eventpeople.pro. Мы свяжемся с вами в ближайшее время!
                    </template>
                    <template v-else-if="n === 3">
                        <v-data-table :headers="headers" :items="itemsTable" hide-default-header hide-default-footer
                            class="elevation-1"></v-data-table>
                    </template>
                </v-col>
            </v-row>
        </v-container>
    </v-main>
</template>
<script>
    import appBr from "../app-breadcrumps";
    export default {
        components: {
            "sub-app-breadcrumbs": appBr
        },
        data() {
            return {
                headers: [{
                        text: 'Dessert (100g serving)',
                        align: 'start',
                        value: 'name',
                    },
                    {
                        text: 'name',
                        value: 'text'
                    },
                ],
                itemsTable: [{
                    name: 'Наименование юрлица: ',
                    text: "Индивидуальный предприниматель Романов Александр Александрович",

                }, ],
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
                    {
                        text: "Реквизиты",
                        href: "/payment",
                        disabled: false,
                    },

                ]
            }
        }
    }
</script>