<template>
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
</template>
<script>
    export default {
        data() {
            return {
                title: document.title
            }
        },
        props: {
            items: Array
        }
    }
</script>
<style lang="scss">
    .v-breadcrumbs {
        &__item {
            color: black !important;
            &:hover {
                border-radius: 0.25rem;
                border-width: 1px;
                background-color: #eeeeee !important;
                padding: .3rem;
                font: {
                    weight: 500;
                };
            }
        }
    }
</style>