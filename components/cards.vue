<template>
    <div class="flex mt-8 ml-2 mr-2 justify-between">
        <card v-for="card in cards" :card-title="card.title" :key="card.id"/>
    </div>
</template>

<script>
import card from '~/components/card.vue'

    export default {
        name: "cards",
        components: {
            card
        },
        data: () => ({
            cards: [{
                id: 1,
                title: "Ik"
            },
            {
                id: 2,
                title: "Jij"
            },
            {
                id: 3,
                title: "Nee"
            },
            {
                id: 4,
                title: "Ja"
            },
            {
                id: 5,
                title: "Een"
            }
            ]
        }),
        methods: {

        }
    };
</script>

<style>
</style>