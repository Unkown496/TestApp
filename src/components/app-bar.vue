<template>
    <v-card outlined elevation="0">
        <v-app-bar app dense outlined color="white" elevation="1" :collapse-on-scroll="collapseOnScroll" ref="appBar">
            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title>Sparcl Deco Star</v-toolbar-title>
            <v-btn style="visibility:hidden;">test</v-btn>
            <v-spacer></v-spacer>
            <!-- <v-icon v-for="item in iconsNav" :key="item.icon" v-text="item.icon" :href="item.link" small tag="a"></v-icon> -->
            <div class="text-center d-none d-md-flex" v-for="(item, i) in navMenu" :key="i">
                <v-menu open-on-hover bottom offset-y :disabled="item.isDisabled" origin="center center"
                    transition="scale-transition">

                    <template v-slot:activator="{ on, attrs }">
                        <v-btn text v-bind="attrs" v-on="on">
                            {{ item.title }}
                        </v-btn>
                    </template>
                    <v-list>
                        <v-list-item-group active-class="deep-purple--text text--accent-4">
                            <v-list-item v-for="(item, i) in navMenu[i].list" :key="i">
                                <v-list-item-title tag="a" :href="item.href"
                                    class="text-uppercase text-decoration-none black--text">{{ item.text }}
                                </v-list-item-title>
                            </v-list-item>
                        </v-list-item-group>
                    </v-list>
                </v-menu>
            </div>
        </v-app-bar>

        <v-navigation-drawer v-model="this.drawer" fixed temporary>
            <v-list nav dense>
                <v-list-item-group active-class="deep-purple--text text--accent-4" v-for="(item, i) in navMenu" :key="i">
                    <v-list-item>
                        <v-menu open-on-hover bottom offset-y :disabled="item.isDisabled" origin="center center"
                            transition="scale-transition">

                            <template v-slot:activator="{ on, attrs }">
                                <v-btn text v-bind="attrs" v-on="on">
                                    {{ item.title }}
                                </v-btn>
                            </template>
                            <v-list>
                                <v-list-item-group active-class="deep-purple--text text--accent-4">
                                    <v-list-item v-for="(item, i) in navMenu[i].list" :key="i" @click="drawer = !drawer">
                                        <v-list-item-title tag="a" :href="item.href"
                                            class="text-uppercase text-decoration-none black--text">{{ item.text }}
                                        </v-list-item-title>
                                    </v-list-item>
                                </v-list-item-group>
                            </v-list>
                        </v-menu>
                    </v-list-item>
                </v-list-item-group>
                <v-spacer></v-spacer>
                <v-list-item-group active-class="deep-purple--text text--accent-4" v-for="item in items"
                    :key="item.icon">
                    <v-list-item @click="drawer = !drawer">
                        <v-list-item-icon>
                            <v-icon v-text="item.icon"></v-icon>
                        </v-list-item-icon>
                        <v-list-item-title v-text="item.text"></v-list-item-title>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>

    </v-card>
</template>
<script>
    import {
        items
    } from "./app-system-bar";
    export default {
        data() {
            return {
                items: items,
                drawer: false,
                group: null,
                collapseOnScroll: true,
                navMenu: [{
                        icon: "mdi-user",
                        title: "О КОМПАНИИ",
                        list: [{
                                text: "О нас",
                                href: "/about"
                            },
                            {
                                text: "Реквизиты",
                                href: "/payment"
                            },
                            {
                                text: "Клиенты",
                                href: "/clients"
                            },
                            {
                                text: "Отзывы",
                                href: "/rewiver"
                            }
                        ]
                    },
                    {
                        icon: "mdi-briefcase",
                        title: "Услуги",
                        list: [{
                                text: "tesft",
                            },
                            {
                                text: "test1",
                            },
                            {
                                text: "test2",
                            },
                            {
                                text: "test3",
                            }
                        ]
                    },
                    {
                        icon: "mdi-currency-usd",
                        title: "Цены",
                        isDisabled: true,
                    },
                    {
                        icon: "mdi-currency-usd",
                        title: "Контакты",
                        isDisabled: true,
                    }
                ],
            }
        },
        methods: {
            click() {
                return console.log(this.$refs.appBar, '\n', this.$refs.appBar.$el.classList.length === 10, this.$refs
                    .appBar.currentScroll);
            }
        },
    }
</script>
<style lang="scss">
    .v-toolbar {
        &__title {
            overflow: visible !important;
        }
    }
</style>