<template>
    <div id="skill-spotlight">
        <div id="skill-spotlight-title">{{ skill.name }}</div>
        <div id="skill-bullet-container">
            <div v-for="(bullet, index) in skill.bullets" :key="index" class="skill-bullet">
                {{ bullet }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'skill-spotlight',
    props: {
        skill: {
            name: String,
            bullets: Array,
        }
    },
    watch: {
        skill: function() {
            console.log('frrrrt')
            document.getElementById('skill-spotlight').scrollIntoView({behavior: "smooth", block: "center", inline: "nearest"});
        }
    }
}
</script>

<style>
    #skill-spotlight {
        border: 1px solid  rgb(44, 62, 80);
        margin: 20px;
        padding: 0 0 20px 0;
        -webkit-box-shadow: 1px 2px 1px 0px rgba(44, 62, 80, 0.6);
        -moz-box-shadow:    1px 2px 1px 0px rgba(44, 62, 80, 0.6);
        box-shadow:         1px 2px 1px 0px rgba(44, 62, 80, 0.6);
        align-content: center; 
    }

    #skill-spotlight-title {
        display: flex;
        justify-content: center;
        align-content: center;
        border-bottom: 1px solid gray;
        padding: 10px;
        margin: auto;
        width: 60%;
        font-size: 1.2em;
    }

    #skill-bullet-container {
        text-align: left;
        padding: 0 20px;
    }

    .skill-bullet {
        padding: 5px 0px;
    }

    .skill-bullet::before {
        content: '-';
    }

    .skill-bullet:first-of-type {
        padding-top: 15px;
    }
</style>
