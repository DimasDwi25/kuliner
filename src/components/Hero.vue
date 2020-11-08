<template>
  <div class="hero">
    <!--Desktop-->
    <div class="d-none d-md-block">
      <div class="row mt-5">
        <div class="col-md">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Delicious Food Menu,</strong>
                <br />In Your Gadget
              </h2>
              <p>Ayo segera pilih dan pesan makanan favorit anda</p>
              <router-link to="/foods">
                <button class="btn btn-lg btn-success">
                  <b-icon-arrow-right></b-icon-arrow-right>Pesan
                </button>
              </router-link>
            </div>
          </div>
        </div>
        <div class="col-md">
          <img src="../assets/images/hero.png" width="100%" alt />
        </div>
      </div>
    </div>

    <!--Mobile-->
    <div class="row mt-5 d-md-block d-sm-none">
      <div class="col-md">
        <div class="col-md">
          <img src="../assets/images/hero.png" width="100%" alt />
        </div>
        <div class="d-flex h-100">
          <div class="justify-content-center align-self-center">
            <h2>
              <strong>Delicious Food Menu,</strong>
              <br />In Your Gadget
            </h2>
            <p>Ayo segera pilih dan pesan makanan favorit anda</p>
            <router-link to="/foods">
                <button class="btn btn-lg btn-success">
                  <b-icon-arrow-right></b-icon-arrow-right>Pesan
                </button>
              </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero"
};
</script>