<template>
  <ul>
    <li v-for="(Houses, i) in Houses" :key="i">
      <div class="card">
        <div class="row">
          <div class="innerLeft">
            <img
              class="imgCardRecom"
              src="../assets/images/img_placeholder_house@3x.png"
            />
          </div>
          <div class="innerRight">
            <div class="horizontal-card-footer">
              <h2 class="card-title-describtion1">{{ Houses.houseName }}</h2>
              <p></p>
              <span class="card-text-describtion1">1011 AA Amsterdam</span>
              <p></p>
              <span class="card-price-describtion1"
                ><img class="icon5" src="../assets/images/ic_bed@3x.png" />{{
                  Houses.bedrooms
                }}</span
              >
              <span class="card-price-describtion1"
                ><img class="icon5" src="../assets/images/ic_bath@3x.png" />{{
                  Houses.bathrooms
                }}</span
              >
              <span class="card-price-describtion1"
                ><img class="icon5" src="../assets/images/ic_size@3x.png" />120²</span
              >
              <p></p>
            </div>
          </div>
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
import style from "../assets/sass/styles.scss";
import Resources from '../assets/Resources'

export default {
  name: "app",
  data: () => ({
    selection: 1,
    drawer: true,
    Houses: Resources,
  }),
};
</script>

<style>
.card {
  background-color: white;
  display: block;
  width: 100%;
  border-radius: 5px;
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.innerLeft {
  display: inline-block;
  margin-right: -4px;
  vertical-align: top;
  width: 50%;
  text-align: center;
  padding: 5px;
}

.innerRight {
  display: inline-block;
  vertical-align: top;
  width: 50%;
  text-align: left;
  padding: 5px;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

li {
  padding: 2px 5px;
}

ul {
  display: inline-block;
  margin: auto;
  padding: auto;
  list-style-type: none;
}

.imgCardRecom {
  width: 100%;
  height: auto;
  border-radius: 15px;
}

.card-title-describtion1 {
  font-family: "MontserratBold";
  font-size: 15px;
  margin-left: 30px;
}

.card-text-describtion1 {
  font-family: "MontserratLight";
  font-size: 13px;
  margin-top: 40px;
  margin-left: 30px;
  color: #d4d4d4;
}

.card-price-describtion1 {
  font-family: "MontserratRegular";
  font-size: 15px;
  color: #4a4b4c;
  margin-top: 40px;
  margin-left: 30px;
}

.icon5 {
  width: 15px;
  height: 15px;
  margin-right: 10px;
}
.horizontal-card-footer {
  line-height: 1.8;
}
</style>