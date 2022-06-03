<template>
    <v-footer dark class="flex-column pt-5 px-0">
        <v-row color="grey darken-3" class="mb-9 px-5">
            <v-col v-for="(item, i) in itemsMain" :key="item.title" cols="12" sm="4"
                class="d-flex flex-column justify-md-center">
                <template v-if="i === 0">
                    <h2> {{item.title}} </h2>
                    <p> {{item.text}} </p>
                </template>
                <template v-else-if="i === 1">
                    <h2> {{ item.title }} </h2>
                    <v-divider></v-divider>
                    <v-list dense>
                        <v-list-item-group v-model="selectedItem" color="deep-purple">
                            <v-list-item v-for="(item) in itemsSubMenu" :key="item.title">
                                <v-list-item-icon>
                                    <v-icon v-text="item.icon"></v-icon>
                                </v-list-item-icon>
                                <v-list-item-content>
                                    <v-list-item-title v-text="item.text"></v-list-item-title>
                                </v-list-item-content>
                            </v-list-item>
                        </v-list-item-group>
                    </v-list>
                </template>
                <template v-else-if="i === 2">
                    <h2> {{ item.title }} </h2>
                    <h4> Sparcl Deco Star</h4>
                    <p width="50%"> {{ item.text }} </p>
                </template>
            </v-col>
            <v-divider></v-divider>
        </v-row>
        <v-col rows="12" class="px-0 grey darken-4 text-center">
            <p class="ma-0 text--white">
                Sparcl Deco Star ® Все права защищены.
            </p>
            <p class="text-center ma-0 text--white"> {{ new Date().getFullYear() }} </p>
        </v-col>
    </v-footer>
</template>
<script>
    export default {
        data() {
            return {
                selectedItem: '',
                itemsSubMenu: [{
                        icon: "mdi-information",
                        text: "О КОМПАНИИ"
                    },
                    {
                        icon: "mdi-briefcase",
                        text: "УСЛУГИ"
                    },
                    {
                        icon: "mdi-currency-usd",
                        text: "ЦЕНЫ"
                    },
                    {
                        icon: "mdi-contacts",
                        text: "КОНТАКТЫ"
                    }
                ],
                itemsMain: [{
                        title: "Sparcl Deco Star",
                        text: "-– динамично развивающаяся компания, с амбициозными целями. Наш актив – это профессионалы, работающие в нашей команде. У нас вы можете заказать комплекс услуг из персонала, для организации мероприятий различного формата."
                    },
                    {
                        tilte: "",
                        text: ""
                    },
                    {
                        title: "Наши контакты",
                        text: "г. Москва, Павелецкая набережная 2 офис 34 \n Telephone: +7 (499) 394-04-45 \n WhatsApp: +7 (929) 665-47-40 \n E-mail: hello@eventpeople.pro"
                    }
                ],
            }
        }
    }
</script>