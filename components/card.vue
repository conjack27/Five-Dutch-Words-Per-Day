<template>
    <div class="card flip-card w-1/5 h-56 ml-2 mr-2">
        <div class="flipper border border-white rounded   p-4 ">
            <div class="front">
                <h3 class="text-5xl text-white font-body text-center">{{ cardTitle }}</h3>
            </div>
            <div class="back">
                <h1>John Doe</h1>
                <p>Architect & Engineer</p>
                <p>We love that guy</p>
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
            
        }),
        methods: {

        }
    };
</script>

<style>
    
    /* entire container, keeps perspective */
.flip-card {
}

/* flip the pane when clicked */
.flip-card:hover .flipper, .flip-card.hover .flipper {
  -webkit-transform: rotateY(180deg);
}

/* flip speed goes here */
.flipper {
	-webkit-transition: 0.6s;
	-webkit-transform-style: preserve-3d;
	position: relative;
    width: 100%;
    height: 100%;
}

/* hide back of pane during swap */
.front, .back {
	-webkit-backface-visibility: hidden;
	position: absolute;
	top: 0;
	left: 0;
    width: 100%;
    height: 100%;
}

/* front pane, placed above back */
.front {
  z-index: 2;
}

/* back, initially hidden pane */
.back {
  -webkit-transform: rotateY(180deg);
}
</style>