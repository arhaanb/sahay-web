<template>
  <div class="vh">
    <div class="container">
      <div class="six columns home">
        <h1 class="zero semi">Sahay</h1>
        <h5>All in one hospital management.</h5>

        <router-link to="/about">
          <button class="cool">Learn more</button>
        </router-link>
      </div>
      <div class="six columns">
        <br class="anti" /><br class="anti" />
        <div>
          <p class="center">
            <img
              src="@/assets/illustration.svg"
              draggable="false"
              alt="illustration"
							class="illus"
            />
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped>
.home {
  margin-top: 9em;
}

.vh {
  margin: 4em 0 8em 0;
}

.anti {
  display: none;
}
@media (max-width: 750px) {
  .vh {
    margin: 4em 0;
  }
  .home {
    margin: 0;
  }
  .anti {
    display: block;
  }
}
p.center {
  text-align: center;
	margin: 0;
}
.illus {
	margin-top: 2em;
}
</style>
