<template>
    <v-main>
        <sub-app-breadcrumbs :items="items"></sub-app-breadcrumbs>
        <v-container>
            <v-row>
                <v-col>
                    <v-data-table :headers="headersTable" :items="itemsTable" dense
                    class="elevation-1"></v-data-table>
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
                items: [{
                        text: "Главная",
                        href: "/",
                        disabled: false,
                    },
                    {
                        text: "Услуги",
                        href: "/att",
                        disabled: false,
                    },
                ],
                headersTable: [{
                    text: 'Найменование',
                    align: 'start',
                    sortable: false,
                    value: 'title',
                }, 
                { text: 'Минимальное время работы', value: 'minTime' },
                { text: "Стоимость работы (руб/час)", value: "payday" },
                // { text: "Оставить заявку", value: thi }
            ],
                itemsTable: [{
                    title: "Хелп",
                    minTime: '100',
                    payday: '120'
                }]
            }
        }
    }
</script>