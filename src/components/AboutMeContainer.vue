<template>
    <div id="about-me">
        <h2 class="text-uppercase">About Me</h2>
        <div class="about-grid">
            <div class="col-one">
                <p>
                    <span class="leadin-text">Scientist. Technologist. Lifelong learner.</span>
                    These titles give a sense of my passions. I live to develop novel solutions, learn from my colleagues and share my expertise.
    
                </p>
                <p>
                    Working as an analytical chemist taught me the importance of creative problem solving, iterative process improvement, and the vital importance documentation.
                </p>
            </div>
            <div class="col-two">
                <p>
                    I am always learning and looking to contribute towards the effort at hand. Whether that involves rolling up my sleeves and getting to work, or helping coordinate between colleagues, I find it satisfying to help where I'm most needed.
                </p>
                <p>I also like to cook :3</p>
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
        padding: 20px 10%;
    }

    .leadin-text {
        font-size: 1.2em;
    }

    .col-one { 
        grid-area: colone; 
        border-right: 1px rgb(44, 62, 80, .5) solid;
    }
    .col-two { grid-area: coltwo; }

    .about-grid {
        display: grid;
        grid-auto-columns: auto auto;
        grid-template-areas: 
            'colone coltwo'
        ;
    }

    .about-grid>div {
        padding: 0px 20px;
    }

</style>
