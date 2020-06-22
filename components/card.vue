<template>
    <div class="w-1/5 h-56 ml-2 mr-2" @click="flipped = !flipped">
        <div class="flip-card border border-white rounded duration-500 relative h-full cursor-pointer" :class="{ 'flipped': flipped }">
            <div class="flip-card__front p-4 absolute inline-block">
                <h3 class="text-5xl text-white font-body text-center z-2">{{ cardTitle }}</h3>
            </div>
            <div class="flip-card__back text-white font-body text-center p-4 absolute top-0 left-0 h-full w-full inline-block">
                <h3 class="text-2xl mb-2 font-bold">{{ translation }}</h3>
                <p class="text-xl"> {{ example }}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "card",
        props: ["cardTitle"],
        components: {
            
        },
        data: () => ({
            flipped: false,
            translation: "Translation",
            example: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
        }),
        methods: {
        }
    };
</script>

<style>
    
.flipped {
  -webkit-transform: rotateY(180deg);
}

.flip-card {
	-webkit-transform-style: preserve-3d;
}

.flip-card__front, .flip-card__back {
	backface-visibility: hidden;
}

.flip-card__back {
  -webkit-transform: rotateY(180deg);
}
</style>