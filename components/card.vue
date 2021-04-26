<template>
<b-container class="card mb-3 bg-transparent">
  <b-row class="no-gutters">
    <b-col cols=3>
      <img :src="require(`~/assets/${image}.png`)" class="card-img" alt="..." />
    </b-col>
    <b-col cols=9 style="padding: 0">
      <div class="card-body">
        <h5 class="card-title">{{ name }}</h5>
        <p class="card-text">{{ text }}</p>
      </div>
    </b-col>
  </b-row>
</b-container>
</template>

<style>
.card {
  border: none; 
  padding: 15px 0 0 0;
}
.card-title {
  font-family: 'Montserrat-Bold';
  color: #fff;
  margin: 0;
}
.card-text {
  color: #fff;
  font-family: 'Montserrat';
}
.card-img {
  border-radius: 50%;
  background: #fff;
}
.no-gutters {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}
.card-body {
  padding: 0 0 0 15px;
}
@media only screen and (max-width: 770px) {
    .card-text {
      font-size: 10px;
    }
    .card-title {
      font-size: 13px;
    }
}
@media only screen and (min-device-width: 770px) {
    .card-text {
      font-size: 15px;
    }
    .card-title {
      font-size: 18px;
    }
}
</style>

<script>
export default {
    props: ['name', 'text', 'image']
}
</script>