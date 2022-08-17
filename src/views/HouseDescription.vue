<template>
  <div class="BigContainerDescription" id="HouseDescribtion">
    <Back/>
    <div style="display: inline-block">
      <div class="w3-container">
        <div class="card1">
          <img class="HouseImg" src="../assets/images/img_placeholder_house@3x.png" />
          <div class="HouseDetails">
            <h2 class="card-title-describtion">Stockvisstraat 132</h2>
            <p></p>
            <span class="card-text-describtion"
              ><img class="icon4" src="../assets/images/ic_location@3x.png" /> 1011 AA
              Amsterdam</span
            >
            <p></p>
            <span class="card-price-describtion"
              ><img class="icon4" src="../assets/images/ic_price@3x.png" />500$</span
            >
            <span class="card-price-describtion"
              ><img class="icon4" src="../assets/images/ic_size@3x.png" />120²</span
            >
            <span class="card-price-describtion"
              ><img
                class="icon4"
                src="../assets/images/ic_construction_date@3x.png"
              />Built in 1990</span
            >
            <p></p>
            <div class="Text">
              <span class="card-text-text">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis
                ullam ipsam, exercitationem quia illum iste reiciendis nulla
                voluptatum reprehenderit, repellendus recusandae dolore tempore
                nobis a quos vitae dolores magni dolorum.
              </span>
            </div>
          </div>
        </div>
        <div class="card2">
          <div style="margin-top: 20px; margin-bottom: 20px">
            <span class="BigText2">Recommended for you</span>
          </div>
          <div class="smallCardsRecommended" v-for="(item, i) in resources" :key="i">
            <SmallCards v-bind:href="item" :item="item" target="_blank"></SmallCards>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SmallCards from "../components/smallCards.vue";
import Back from "../components/Back.vue";
import axios from "axios";

export default {
  name: "HomeDescription",
  data: () => ({
    selection: 1,
    drawer: true,
    resources: []
  }),
  mounted () {
    axios
      .get('https://api.intern.d-tt.nl/api/houses',{
        headers: {
          'X-Api-Key': '_KwzeY0H3LysA1Qj9Icg-Gv5Xn2EPTrf'
        }
      })
      .then(response => {
        this.resources = response.data
        console.log(response.data)
      })
      .catch(error => console.log(error))
  },
  components: { SmallCards, Back }
}
</script>

<style>

.BigContainerDescription{
  height: 15vh;
  width: 100%;
  display: flex;
  margin-left: 5rem;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  background-color: transparent;
  }

.Back {
  margin-top: 10px;
  padding-left: 30px;
}

.BigText1 {
  font-family: "MontserratSemiBold";
  font-size: 20px;
  margin-left: 10px;
}

.BigText2 {
  font-family: "MontserratBold";
  font-size: 18px;
  margin-left: 95px;
}

.icon3 {
  width: 20px;
  height: 20px;
  padding-top: 5px;
}

.icon4 {
  width: 15px;
  height: 15px;
  margin-right: 10px;
}

.left-column {
  width: 65%;
  position: relative;
  margin-left: 200px;
  margin-top: 40px;
}

.card1 {
  display: inline-block;
  width: 74%;
  max-width: 900px;
  border-radius: 5px;
  margin-left: 100px;
  margin-top: 40px;
  margin-bottom: 100px;
  border: #4a4b4c;
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.card2 {
  display: inline-block;
  margin-top: 20px;
  width: 50%;
  max-width: 700px;
  vertical-align: top;
  margin-left: 20px;
}

.HouseImg {
  width: 100%;
  border-radius: 5px;
  margin-top: 20px;
  margin: auto;
}

.card-title-describtion {
  font-family: "MontserratBold";
  font-size: 25px;
  margin-left: 50px;
  margin-top: 15px;
}

.card-price-describtion {
  font-family: "MontserratSemiBold";
  font-size: 15px;
  margin-left: 50px;
  margin-top: 40px;
  color: #4a4b4c;
}

.card-text-describtion {
  font-family: "MontserratSemiBold";
  font-size: 15px;
  margin-left: 50px;
  margin-top: 40px;
  color: #4a4b4c;
}

.card-text-text {
  font-family: "MontserratRegular";
  font-size: 15px;
  margin-top: 40px;
  margin-bottom: 100px;
  color: #4a4b4c;
}

.HouseDetails {
  line-height: 1.8;
}

.Text {
  margin-left: 50px;
  padding-bottom: 50px;
}
</style>