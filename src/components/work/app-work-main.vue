<template>
    <v-main>
        <sub-app-breadcrumbs :items="itemsBr"></sub-app-breadcrumbs>
        <v-container>
            <v-row>
                <v-col>
                    <h2 class="text-decoration-underline"> {{ title }} </h2>
                    <v-img src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg"
                        gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"></v-img>
                    <p>Для организации мероприятия нужно немало времени и сил, так как это дело весьма хлопотное.
                        Организатору мероприятий невсегда по силам уследить за всеми немаловажными мелочами. Ситуацию
                        может спасти Хелпер (от английского "Helper" - помощник). Он выступит Вашим личным помощником на
                        площадке и выполнит задания различного рода.</p>
                    <div class="text-caption d-flex flex-collumn">
                        <p class="flex-grow-1">Заинтересовала услуга? Оставьте заявку сейчас, и мы свяжемся с вами в ближайшее время.</p>
                        <v-btn dark>
                            Оставить заявку
                        </v-btn>
                    </div>

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
                title: document.title,
                itemsBr: [{
                        text: "Главная",
                        href: "/att",
                        disabled: false,
                    },
                    {
                        text: "Услуги",
                        href: "/att",
                        disabled: false,
                    },
                    {
                        text: document.title,
                        href: "/",
                        disabled: false,
                    }
                ],
            }
        }
    }
</script>