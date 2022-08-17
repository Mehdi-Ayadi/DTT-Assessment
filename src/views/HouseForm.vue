<template>
  <div class="Form1">
    <Back/>
    <div class="BigContainer" id="HouseDescribtion">
      <div style="display: inline-block;">
            <div class="w3-container" v-on:submit.prevent="submitForm">
                <div class="divContainer">
                    <h1 class="BigText3">Create new listing</h1>
                </div>
                <div class="divContainer">
                    <h3 class="titleForm">Street name*</h3>
                    <input placeholder="Enter the street name" class="boxForm"/>
                </div>
                <div class="columnContainer">
                    <div class="divContainer">
                        <a class="titleForm2">House Number*</a>
                        <input placeholder="Enter the house number" class="boxFormSmall"/>
                    </div>
                    <div class="divContainer">
                        <a class="titleForm2">Additional (optional)*</a>
                        <input placeholder="e.g.A" class="boxFormSmall"/>
                    </div>
                </div>
                <div class="divContainer">
                    <h3 class="titleForm">Postal code*</h3>
                    <input placeholder="e.g 1000 AA" class="boxForm"/>
                </div>
                <div class="divContainer">
                    <h3 class="titleForm">City*</h3>
                    <input placeholder="e.g Utrecht" class="boxForm"/>
                </div>
                <div class="divContainer">
                    <h3 class="titleForm">Upload picture (PNG or JPG)*</h3>
                    <img class="imgUpload" onclick="history.back()" src="../assets/images/ic_upload@3x.png"/>
                </div>
                <div class="divContainer">
                    <h3 class="titleForm">Price*</h3>
                    <input placeholder="e.g 150.000$" class="boxForm"/>
                </div>
                <div class="columnContainer">
                    <div class="divContainer">
                        <a class="titleForm2">Size*</a>
                        <input placeholder="Enter the house number" class="boxFormSmall"/>
                    </div>
                    <div class="divContainer">
                        <a class="titleForm2">Garage*</a>
                        <input placeholder="Enter the house number" class="boxFormSmall"/>
                    </div>
                </div>
                <div class="columnContainer">
                    <div class="divContainer">
                        <a class="titleForm2">Bedroom number*</a>
                        <input placeholder="Enter amount" class="boxFormSmall"/>
                    </div>
                    <div class="divContainer">
                        <a class="titleForm2">Bathroom number*</a>
                        <input placeholder="Enter amount" class="boxFormSmall"/>
                    </div>
                </div>
                <div class="divContainer">
                    <h3 class="titleForm">Construction date*</h3>
                    <input placeholder="e.g 1990" class="boxForm"/>
                </div>
                <div class="divContainer">
                    <h3 class="titleForm">Description*</h3>
                    <input placeholder="Enter description" class="boxFormDescription"/>
                </div>
                <div class="divContainer">
                    <button class="button1">Submit</button>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import Back from '../components/Back.vue'
import axios from 'axios'

export default {
  name: 'List',
  // data () {
  //   return {
  //     resources: []
  //   };
  // },
  // mounted () {
  //   axios
  //     .get('https://api.intern.d-tt.nl/api/houses',{
  //       headers: {
  //         'X-Api-Key': '_KwzeY0H3LysA1Qj9Icg-Gv5Xn2EPTrf'
  //       }
  //     })
  //     .then(response => {
  //       this.resources = response.data
  //       console.log(response.data)
  //     })
  //     .catch(error => console.log(error))
  // },

  // methods: {
  //   submitForm () {
  //     axios.post('https://api.intern.d-tt.nl/api/houses/:houseId', this.resources)
  //       .then((res) => {
  //         //Perform Success Action
  //       })
  //       .catch((error) => {
  //         // error.response.status Check status code
  //     }).finally(() => {
  //         //Perform action in always
  //       });
  //   }
  // },
  components: { Back }
}
</script>

<style>
.imgUpload {
  width: 24px;
  height: 24px;
  margin-left: 200px;
  margin-top: 60px;
  margin-bottom: 20px;
}

.divContainer {
  height: 15vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  padding: 1rem;
}

.columnContainer {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
}

.Form1 {
  width: 100%;
  height: 100%;
  z-index: 1;
  position: absolute;
  background: url(../assets/images/img_background@3x.png) no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}

.boxForm {
  width: 100%;
  font-size: 15px;
  padding: 15px 20px;
  background-color: #fff;
  border-radius: 20px;
  border-color: transparent;
  font-family: "MontserratRegular";
}

.BigContainer{
  height: 15vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  padding-left: 10rem;
  background-color: transparent;
}

.boxFormDescription {
  width: 600px;
  height: 400px;
  font-size: 15px;
  padding: 20px 20px;
  background-color: #fff;
  border-radius: 20px;
  border-color: transparent;
  font-family: "MontserratRegular";
}

.boxFormSmall{
  width: 262px;
  font-size: 18px;
  padding: 15px 20px;
  background-color: #fff;
  border-radius: 20px;
  border-color: transparent;
  font-family: "MontserratRegular";
  font-size: 15px;
}

.boxFormSmallMultiple {
  width: 260px;
  height: 60px;
  overflow: hidden;
  font-size: 18px;
  padding: 15px 20px;
  background-color: #fff;
  border-radius: 20px;
  border-color: transparent;
  font-family: "MontserratLight";
  font-size: 15px;
}

.titleForm {
  font-family: "MontserratBold";
  font-size: 15px;
}

.titleForm2 {
  font-family: "MontserratBold";
  font-size: 15px;
}

.titleForm3 {
  font-family: "MontserratBold";
  font-size: 15px;
}

.titleForm4 {
  font-family: "MontserratLight";
}

.BigText3 {
  font-family: "MontserratBold";
  font-size: 40px;
}
</style>