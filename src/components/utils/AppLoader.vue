<template>
  <div class="loaderContainer">
    <span class="loader"></span>
  </div>
</template>

<script>
export default {
  name: "AppLoader",
};
</script>

<style scoped>
.loaderContainer {
  min-height: 50vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.loader {
  animation: rotate 1s infinite;
  height: 50px;
  width: 50px;
}

.loader:before,
.loader:after {
  border-radius: 50%;
  content: "";
  display: block;
  height: 20px;
  width: 20px;
}
.loader:before {
  animation: ball1 1s infinite;
  background-color: #fff;
  box-shadow: 30px 0 0 #4493c2;
  margin-bottom: 10px;
}
.loader:after {
  animation: ball2 1s infinite;
  background-color: #4493c2;
  box-shadow: 30px 0 0 #fff;
}

@keyframes rotate {
  0% {
    transform: rotate(0deg) scale(0.8);
  }
  50% {
    transform: rotate(360deg) scale(1.2);
  }
  100% {
    transform: rotate(720deg) scale(0.8);
  }
}

@keyframes ball1 {
  0% {
    box-shadow: 30px 0 0 #4493c2;
  }
  50% {
    box-shadow: 0 0 0 #4493c2;
    margin-bottom: 0;
    transform: translate(15px, 15px);
  }
  100% {
    box-shadow: 30px 0 0 #4493c2;
    margin-bottom: 10px;
  }
}

@keyframes ball2 {
  0% {
    box-shadow: 30px 0 0 #fff;
  }
  50% {
    box-shadow: 0 0 0 #fff;
    margin-top: -20px;
    transform: translate(15px, 15px);
  }
  100% {
    box-shadow: 30px 0 0 #fff;
    margin-top: 0;
  }
}
</style>
