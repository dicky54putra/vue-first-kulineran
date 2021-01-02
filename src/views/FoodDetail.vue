<template>
  <div class="food">
    <Navbar />
    <div class="container">
      <!-- Breadcrump -->
      <div class="row mt-4">
        <div class="col">
          <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
              <li class="breadcrumb-item">
                <router-link to="/">Home</router-link>
              </li>
              <li class="breadcrumb-item">
                <router-link to="/foods">Foods</router-link>
              </li>
              <li class="breadcrumb-item active" aria-current="page">
                Food <strong>Detail</strong>
              </li>
            </ol>
          </nav>
        </div>
      </div>

      <!-- Detail -->
      <div class="row mt-3">
        <div class="col-md-6">
          <img
            :src="'../assets/images/' + product.gambar"
            class="img-fluid shadow"
          />
        </div>
        <div class="col-md-6">
          <h2>
            <strong>{{ product.nama }}</strong>
          </h2>
          <hr />
          <h4>
            Harga: <strong>Rp. {{ product.harga }}</strong>
          </h4>

          <form action="" method="post" class="mt-4">
            <div class="form-group">
              <label for="jumlah-pesanan" class="form-label"
                >Jumlah Pesanan</label
              >
              <input type="number" class="form-control" id="jumlah-pesanan" />
            </div>
            <div class="form-group">
              <label for="keterangan" class="form-label">Keterangan</label>
              <textarea
                class="form-control"
                name=""
                id="keterangan"
                rows="3"
                placeholder="Keterangan seperti: Pedes, Nasi setengah, dsb.."
              ></textarea>
            </div>
            <div class="form-group">
              <button type="submit" class="btn btn-success">
                <b-icon-cart></b-icon-cart> Pesan
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import axios from "axios";

export default {
  name: "FoodDetail",
  components: {
    Navbar,
  },
  data() {
    return {
      product: [],
    };
  },
  methods: {
    setProduct(data) {
      this.product = data;
    },
  },
  mounted() {
    // Make a request for a user with a given ID
    axios
      .get("http://localhost:3000/products/" + this.$route.params.id)
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log("gagal", error));
  },
};
</script>

<style>
</style>