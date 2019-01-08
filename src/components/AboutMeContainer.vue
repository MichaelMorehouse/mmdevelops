<template>
  <div id="about-me">
    <h2 class="text-uppercase">About Me</h2>
    <div class="about-grid">
      <div class="col-one">
        <p>
          <span class="leadin-text">Super great guy.</span>
            Just the best wow. You're going to be working with this fellow like "Oh man what a great co-worker, this job might be slowly sapping my will to live but at least I get to hang out with such great people that delay my inevitable reduction to a sad sack of cynicism incapable of happiness." What a guy.
        </p>
        <p>Umami mixtape palo santo mumblecore roof party. Ad veniam banh mi cloud bread unicorn laboris YOLO minim affogato ut keffiyeh echo park. Tempor 90's brunch heirloom readymade occupy poke franzen. Beard everyday carry taiyaki scenester dreamcatcher cupidatat before they sold out thundercats knausgaard pickled hell of. Est incididunt next level tofu truffaut nulla neutra. Wolf kinfolk flexitarian, chartreuse tilde aliqua non bushwick pork belly cloud bread normcore ut. Tumblr ullamco pariatur bitters literally plaid.</p>
      </div>
      <div class="col-two">
        <p>Bitters est et brunch officia freegan dolore shaman church-key drinking vinegar enim tacos bushwick. Cupidatat distillery locavore, thundercats marfa velit occupy retro aesthetic celiac glossier. Godard tattooed kickstarter, etsy franzen commodo artisan pok pok kitsch. Portland sint pok pok non photo booth normcore. Freegan YOLO yuccie green juice in. Before they sold out poke tofu, put a bird on it brooklyn cardigan hammock four dollar toast hoodie.</p>
        <p>And if you think that's all great, I also like to cook! The wonders never cease</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
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
  border-right: 1px rgb(44, 62, 80, 0.5) solid;
}
.col-two {
  grid-area: coltwo;
}

.about-grid {
  display: grid;
  grid-auto-columns: auto auto;
  grid-template-areas: "colone coltwo";
}

.about-grid > div {
  padding: 0px 20px;
}
</style>
