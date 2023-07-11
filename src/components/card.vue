<template>
  <div class="card w-[50em] h-[22.5em] glass">
    <!-- <figure><img src="/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" alt="car!"/></figure> -->
    <div class="card-body">
      <h1>Easily shortened URLs!</h1>
      <h2>Just paste the URL, submit and it's done!</h2>
      <form @submit.prevent="shorten" class="">
        <div class="input-container">
          <!-- <label for="name" class="name">Name:</label> -->
          <input
            placeholder="Enter Link here"
            type="text"
            class="input"
            v-model="url"
          />
          <div class="underline"></div>
        </div>
        <div class="flex justify-center">
          <button class="btn w-32">Shorten it!</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.input-container {
  position: relative;
  margin: 20px;
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
  color: #333;
  width: 100%;
  outline: none;
}

.underline {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #4158d0;
  background-image: linear-gradient(
    43deg,
    #4158d0 0%,
    #c850c0 46%,
    #ffcc70 100%
  );
  transition: width 0.3s;
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