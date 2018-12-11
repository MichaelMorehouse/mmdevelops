<template>
    <div id="about-me">
        <h2 class="text-uppercase">About Me</h2>
        <div class="about-grid">
            <div class="col-one">
                <span class="leadin-text">Lorem ipsum dolor amet</span> copper mug portland roof party, pariatur meggings knausgaard in selfies letterpress fingerstache poutine plaid pickled tumeric yr. La croix meggings franzen commodo beard. Nostrud adaptogen jianbing, hexagon chambray cloud bread celiac dreamcatcher skateboard salvia kitsch fashion axe laborum shoreditch. Gluten-free before they sold out incididunt schlitz est laboris cliche shoreditch chicharrones kickstarter green juice excepteur butcher.
            </div>
            <div class="col-two">
                Marfa put a bird on it migas craft beer, keffiyeh blue bottle typewriter deep v enamel pin est 8-bit ramps pug occaecat excepteur. Et mollit portland cornhole, cardigan organic four dollar toast tbh celiac laboris. Qui slow-carb magna lorem pug hammock poke incididunt yuccie pariatur put a bird on it typewriter. Eiusmod four loko activated charcoal occaecat synth succulents vegan iPhone. Ut +1 organic listicle. Cold-pressed intelligentsia health goth enim.
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    #about-me {
        color: rgb(44, 62, 80);
        text-align: center;
        padding: 20px 10px;
    }

    .leadin-text {
        font-size: 1.2em;
    }

    .col-one { 
        grid-area: colone; 
        border-right: 1px rgb(128, 128, 128, .5) solid;
    }
    .col-two { grid-area: coltwo; }

    .about-grid {
        display: grid;
        grid-auto-columns: auto auto;
        grid-template-areas: 
            'colone coltwo'
        ;
    }

    .about-grid > div {
        padding: 0 10px;
    }

</style>
