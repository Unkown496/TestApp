<template>
    <v-system-bar app absolute color="white" height="30" class="d-none d-md-flex" id="start">
        <div v-for="(item) in items" :key="item.icon" :text="item.text" :placeholder="item.placeholder" class="px-3">
            <p class="ma-0">
                <v-icon v-text="item.icon"></v-icon>
                <span> {{ item.placeholder }} </span>
                <span> {{ item.text }} </span>
            </p>
        </div>
        <v-spacer></v-spacer>
        <div class="d-flex">
            <p class="px-3 ma-0">
                <v-icon>mdi-account</v-icon>
                Регистрация
            </p>
            <p class="px-3 ma-0">
                <v-icon>mdi-lock</v-icon>
                Войти
            </p>
        </div>
    </v-system-bar>
</template>
<script>
    export let items = [{
            icon: "mdi-email",
            placeholder: "Email",
            text: "placeYourEmail"
        },
        {
            icon: "mdi-cellphone-sound",
            placeholder: "Telephone",
            text: "placeYourTel"
        },
        {
            icon: "mdi-whatsapp",
            placeholder: "WhatsApp",
            text: "placeYourWA"
        },
    ];
    export default {
        data() {
            return {
                items: items,
            }
        }
    }
</script>