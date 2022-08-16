<template>
<div class="Div1">
      <div class="BigContainer">
        <div class="divContainer" style="display: inline-block;">>
            <div class="CreationcolumnContainer">
              <div class="CreationdivContainer">
                <h1 class="BigTextHome">Houses</h1>
              </div>
              <div class="CreationdivContainer">
                <router-link :to="{ path: '/HouseForm' }">
                    <button class="button1">+ CREATE NEW</button>
                </router-link>
              </div>
              </div>
              <div class="columnContainerHome">
                <div style="display: block">
                  <Search/>
                </div>
              </div>
          </div>
      </div>
</div>
</template>

<script>

import style from '../assets/sass/styles.scss'
import CardHouses from '@/components/CardHouses.vue'
import Search from '../components/Search.vue'
export default {
  name: "app",
  components: { CardHouses, Search }
}

</script>

<style>
#app {
  background-color: #f6f6f6;
}

.Div1 {
  font-family: "Montserrat";
  font-size: 20px;
}

.BigTextHome{
  font-family: "MontserratBold";
  font-size: 30px;
  padding-left: 0.5rem;
}

.columnContainerHome{
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  margin-bottom: -5rem;
  margin-top: -5rem;
  align-items: flex-start;
}

.CreationcolumnContainer{
  display: flex;
  flex-direction: row;
  margin-top: 5rem;
  justify-content: space-between;
  align-items: flex-start;
}

.CreationdivContainer{
  height: 15vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  padding: 1rem;
}

.button1:hover {
  background: white;
  color: #eb5440;
}

.button1 {
  box-sizing: content-box;
  width: 200px;
  border-radius: 5px;
  border: 1px solid white;
  padding: 10px 10px;
  margin-left: 4rem;
  background: #eb5440;
  font-size: 15px;
  color: white;
  cursor: pointer;
  font-family: "MontserratSemiBold";
}
</style>
