<template lang="">
  <div class="about">
    <Back/>
    <div class="BigContainer" id="HouseDescribtion"> 
      <div style="display: inline-block;">
                <div class="divContainer">
                    <p></p>
                </div>
                <div class="columnContainer">
                    <h1 class="BigTextAbout">About DTT Real Estate</h1>
                </div>
                <div class="textContainer">
                    <p class="card-text-text">
                      Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis
                      ullam ipsam, exercitationem quia illum iste reiciendis nulla
                      voluptatum reprehenderit, repellendus recusandae dolore tempore
                      nobis a quos vitae dolores magni dolorum. Omnis
                      ullam ipsam, exercitationem quia illum iste reiciendis nulla
                    </p>
                </div>
                <div class="textContainer">
                    <p class="card-text-text">
                      Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    </p>
                </div>
                <div class="columnContainer">
                    <h1 class="BigTextAbout">Design and Development</h1>
                </div>
                <div class="columnContainer">
                    <div class="divContainer">
                      <img class="DTTLogo" src='../assets/images/img_logo_dtt@3x.png'/>
                    </div>
                    <div class="divContainer">
                      <p class="card-textLink1">By DTT</p>
                      <p class="card-textLink2">www.d-tt.nl</p>
                    </div>
                </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>

.about{
  background-color: #F6F6F6;
}

.BigContainer{
  height: 15vh;
  width: 100%;
  display: flex;
  margin-left: 8rem;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  background-color: transparent;
  }

.divContainer {
  height: 15vh;
  width: 40%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  padding: 1rem;
}

.textContainer {
  display: flex;
  flex-direction: row;
  height: 15%;
  width: 60%;
  justify-content: space-between;
  align-items: flex-start;
}

.columnContainer {
  display: flex;
  flex-direction: row;
  width: 60%;
  justify-content: space-between;
  align-items: flex-start;
  padding-top: 1rem;
}

.divSmallContainer {
  height: 15vh;
  width: 70%;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  border: solid black;
}

.divLogoContainer {
  height: 15vh;
  width: 50%;
  display: inline-block;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
}

.DTTLogo{
  width: 70%;
  height: 100%;
}

.card-text-text {
  font-family: "MontserratRegular";
  font-size: 15px;
  color: #4a4b4c;
}

.card-textLink1{
  font-family: "MontserratSemiBold";
  font-size: 20px;
  color: #4a4b4c;
}

.card-textLink2{
  font-family: "MontserratSemiBold";
  font-size: 20px;
  color: #067BC2;
}

.BigTextAbout {
  font-family: "MontserratBold";
  font-size: 25px;
}

</style>