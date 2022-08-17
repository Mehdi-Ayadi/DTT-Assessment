<template>
<div class="w3-container">
        <p></p>
        <div class="ContainerCard">
        <div style="display: inline-block;">
              <div class="card">
                <div class="row">
                  <div class="innerLeft">
                    <img class="imgCard" v-bind:src="item.image"/>
                  </div>
                  <div class="innerRight">
                    <div class="horizontal-card-footer">
                      <router-link :to="{ path: '/HouseForm' }">
                        <img class="iconModify" src="../assets/images/ic_edit@3x.png" />
                      </router-link>
                      <img class="iconDelete" src="../assets/images/ic_delete@3x.png" />
                      <h2 class="card-title">{{ item.location.street }}</h2>
                      <p></p>
                      <span class="card-price">{{ item.price }}$</span>
                      <p></p>
                      <span class="card-text">{{ item.location.zip }}{{ item.location.city }}</span>
                      <p></p>
                      <span class="cardDetails"><img class="iconCard" src="../assets/images/ic_bed@3x.png" />{{ item.bedrooms}}</span>
                      <span class="cardDetails"><img class="iconCard" src="../assets/images/ic_bath@3x.png" />{{ item.bathrooms }}</span>
                      <span class="cardDetails"><img class="iconCard" src="../assets/images/ic_size@3x.png" />{{ item.size }}m²</span>
                      <p></p>
                    </div>
                  </div>
                </div>
                <div class="row">
                  <div class="innerRight">
                    <router-link :to="{ path: '/HouseDescription' }">
                      <button class="button2" style="margin-left: 450px" link="">
                        See Offer
                      </button>
                    </router-link>
                  </div>
                </div>
            </div>
            </div>
        </div>
  </div>
</template>

<script>
export default {
  props: ['item'],
  data: () => ({
    selection: 1,
    drawer: true,
    Houses: this.item
  }),
  mounted () {
    console.log(this.item)
  },
}

</script>

<style>

.ContainerCard{
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  background-color: transparent;
  padding-left: 2rem;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}

.card{
  width: 74%;
  border-radius: 5px;
  padding-top: 2%;
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.innerLeft {
  display: inline-block;
  margin-right: -4px;
  vertical-align: top;
  width: 30%;
  text-align: center;
  padding: 5px;
}

.innerRight {
  display: inline-block;
  vertical-align: top;
  width: 70%;
  text-align: left;
  padding: 5px;
}

.BigText{
  font-family: "MontserratBold";
  font-size: 30px;
}

.card-title {
  font-family: "MontserratBold";
  font-size: 15px;
}

.card-price {
  font-family: "MontserratSemiBold";
  font-size: 15px;
}

.card-text {
  display: inline-block;
  font-family: "MontserratLight";
  font-size: 15px;
}

.cardDetails{
  font-family: "MontserratRegular";
  font-size: 15px;
  color: #4a4b4c;
  margin-top: 40px;
  margin-left: 5px;
}

.iconCard {
  width: 15px;
  height: 15px;
  margin-right: 15px;
  margin-left: 5px;
}

.card:hover {
  box-shadow: 0 5px 35px 0 rgba(0, 0, 0, 0.2);
}

.imgCard {
  width: 80%;
  height: auto;
  border-radius: 15px;
}

.iconModify {
  width: 24px;
  height: 24px;
  margin-left: 90%;
  margin-right: 2%;
}

.iconDelete {
  width: 24px;
  height: 24px;
}

.container {
  position: relative;
  margin: auto;
  overflow: hidden;
  width: stretch;
  height: 250px;
  background: white;
  box-shadow: 5px 5px 15px black;
  border-radius: 10px;
}
</style>