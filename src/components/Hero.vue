<template>
  <div class="hero">
    <!-- desktop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Delicious Food Menu, </strong><br />in your gadget.
              </h2>
              <p>Ayo segera pilih dan pesan makanan faforit anda.</p>
              <router-link to="/foods" class="btn btn-lg btn-success">
                <b-icon icon="arrow-right"></b-icon> Pesan
              </router-link>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/ilustrasi.png" width="100%" />
        </div>
      </div>
    </div>
    <!-- mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-3">
          <img src="../assets/images/ilustrasi.png" width="100%" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Delicious Food Menu, </strong><br />in your gadget.
              </h2>
              <p>Ayo segera pilih dan pesan makanan faforit anda.</p>
              <button class="btn btn-lg btn-success">
                <b-icon icon="arrow-right"></b-icon> Pesan
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style>
</style>