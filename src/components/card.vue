<template>
  <div class="card w-[50em] h-[22.5em] glass m-6">
    <!-- <figure><img src="/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" alt="car!"/></figure> -->
    <div class="card-body">
      <h1>Easily shortened URLs!</h1>
      <h2>Just paste the URL, submit and it's done!</h2>
      <form class="p-0">
        <!-- @submit.prevent="shorten" -->
        <div class="input-container my-4">
          <input placeholder="Enter Link here" type="text" class="input"  v-model="link"/>
          <!-- v-model="this.data.url" -->

          <div class="underline"></div>
        </div>
        <div class="flex justify-center">
          <a class="btn w-32" @click="getlink">Shorten it!</a>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      link: "",
    };
  },
  methods: {
    getlink(){
        
      console.log(this.link);
    },
    shortenlink() {
      axios.defaults.headers.common["Authorization"] =
        "Bearer " + this.$store.state.token;
      axios
        .get(this.$store.state.baseUrl + "/api/user/allclients")
        .then((response) => {
          if (response.data.rc == 1) {
            this.link = response.data.data;
          }
        })
        .catch(() => {
          console.error("ERROR");
          self.$router.push({ name: "Sign In" });
        })
        .finally(() => {
          this.loading = false;
        });
    },
  },
};
</script>

<style>
.input-container {
  position: relative;
  /* margin: 20px; */
}

label {
  display: block;
  margin-bottom: 5px;
  color: #333;
}

.input[type="text"] {
  padding: 10px;
  font-size: 16px;
  border: none;
  border-radius: 4px;
  width: 100%;
  outline: none;
}

.underline {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 4px;
  background-color: #4158d0;
  background-image: linear-gradient(
    43deg,
    #4158d0 0%,
    #c850c0 46%,
    #ffcc70 100%
  );
  transition: width 0.5s;
}

.input[type="text"]:focus + .underline {
  width: 100%;
}

@keyframes floating-label {
  0% {
    transform: translateY(0);
    opacity: 1;
  }

  100% {
    transform: translateY(-25px);
    opacity: 0;
  }
}

.input[type="text"]:placeholder-shown + label {
  position: absolute;
  top: 50%;
  left: 10px;
  transform: translateY(-50%);
  font-size: 14px;
  color: #777;
  pointer-events: none;
  transition: transform 0.3s, font-size 0.3s, color 0.3s;
}

.input[type="text"]:focus:not(:placeholder-shown) + label {
  transform: translateY(-25px);
  font-size: 12px;
  background-color: #4158d0;
  background-image: linear-gradient(
    43deg,
    #4158d0 0%,
    #c850c0 46%,
    #ffcc70 100%
  );
  animation: floating-label 0.3s forwards;
}
</style>