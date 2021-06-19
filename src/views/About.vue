<template>
  <div class="container">
    <div class="row product" id="product" style="margin-top: 1em">
      <div class="six columns prodtext mobile">
        <h2 class="semi">Product</h2>
        <p>
          Founded in 2021, Sahay started life as an idea to not only change the
          way the healthcare system works, but also consolidate all the
          hospitals in the nearby areas and their equipment to make management
          and governing the system easier. Mainly a mobile app, Sahay allows
          hospitals to work together and share resources during this pandemic.
        </p>
        <a href="//github.com/arhaanb/sahay-mobile" target="_blank">
          <button class="cool">App Source</button>
        </a>
      </div>
      <div class="six columns">
        <br /><br />
        <img draggable="false" src="../assets/mockup.png" alt />
      </div>
    </div>

    <div class="u-cf"></div>

    <div class="row product" id="product2">
      <div class="six columns anti">
        <br /><br /><br />
        <p class="center">
          <img
            class="illus"
            src="@/assets/illustration2.svg"
            draggable="false"
            alt="Illustration of man getting vaccinated."
          />
        </p>
      </div>
      <div class="six columns prodtext">
        <h2 class="semi">Dashboard</h2>
        <p>
          Our web app modernises the way our health industry operates, and aims
          to provide a more fast-tracked and elegant solution to the chaos of
          hospitals. Integrated with a real time feedback and update, we ensure
          that no hospital has to suffer due to not having enough resources. A
          quick and easy scan through your personal dashboard gives our users
          all the necessary information, and also grants the ability to make
          requests when in need.
        </p>
        <a href="//app.sahay.us" target="_blank">
          <button class="cool">Dashboard</button>
        </a>
      </div>
      <div class="six columns antianti">
        <p class="center">
          <img
            class="illus mob"
            src="@/assets/illustration2.svg"
            draggable="false"
            alt="Illustration of man getting vaccinated."
          />
        </p>
      </div>
    </div>

    <div class="u-cf"></div>

    <div class="row product">
      <div class="six columns worktext">
        <h2 class="semi">How we work</h2>
        <p>
          Hospitals can register at our website after creating their account the
          can upload the list of all their equpment that they have on the
          dashboard, they can further contact other hospitals for the equipments
          required by them.
        </p>
        <a style="margin-right: 1em" href="/branding" target="_blank">
          <button class="cool">Company Branding</button>
        </a>

        <a href="/figma" target="_blank">
          <button class="cool">Figma</button>
        </a>
      </div>
      <div class="six columns">
        <p class="hrtalign">
          <img class="hrt" src="/sur.png" draggable="false" alt />
        </p>
      </div>
    </div>
    <div class="u-cf"></div>

    <div class="vidpen">
      <div>
        <iframe
          width="100%"
          src="https://www.youtube.com/embed/VfyERhwbi4c"
          frameborder="0"
          allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
          class="video"
        ></iframe>
      </div>
    </div>

    <br />
    <br />
    <br />
  </div>
</template>

<style scoped>
#product {
  margin-bottom: 2em;
}

#product2 {
  margin-bottom: 2em;
  margin-top: 2em;
}

.product h2 {
  margin: 0;
  font-size: 2.2em;
  margin-bottom: 0.1em;
}

.product img {
  margin-top: -2em;
}

.vidpen {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 56.25%;
  margin-top: 7.5em;
}

.video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 0.5em;
}

.prodtext {
  margin-top: 4em;
}

.worktext {
  margin-top: 7em;
}

.hrt {
  width: 17.5em;
  float: right;
}

.hrtalign {
  margin-top: 7.5em;
}

.antianti {
  display: none;
}

.illus.mob {
  margin-top: 2.5em;
  margin-bottom: 1em;
}

@media (max-width: 750px) {
  .hrt {
    width: 60%;
    float: none;
  }
  .hrtalign {
    text-align: center;
  }
  .vidpen {
    margin-top: 5em;
  }
  .antianti {
    display: block;
  }
  .anti {
    display: none;
  }
  #product {
    margin-bottom: 1em;
  }
  .worktext {
    margin-top: 2em;
  }
  .prodtext.mobile {
    margin-top: 1em;
  }
}
p.center {
  text-align: center;
}

.illus {
  width: 70%;
}
</style>
