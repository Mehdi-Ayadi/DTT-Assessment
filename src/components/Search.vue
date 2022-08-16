<template>
    <div>
        <div class="ButtoncolumnContainer">
            <div class="ButtondivContainer">
                <input placeholder="Search for houses" class="Search" v-model="searchQuery">
            </div>
            <div class="ButtondivContainer" style="display: inline-block">
                <button class="button2">Price</button>
                <button class="button2">Size</button>
            </div>
        </div>
        <div class="table-responsive">
            <div v-if="resources.length > 0" class="table">
                <div>
                    <div v-for="(item, i) in resultQuery" :key="i">
                        <div>
                            <Cards v-bind:href="item.city" target="_blank">{{ item.city }}</Cards>
                        </div>
                    </div>
                </div>
            </div>
            <div v-else-if="!item in resultQuery" :key="i" class="div">
                <img class="NotFound" src="../assets/images/img_empty_houses@3x.png"/>
            </div>
        </div>
    </div>
</template>

<script>
import Cards from './CardHouses.vue'
import Resources from '../assets/Resources'

export default ({
  name: 'Search',
  data () {
    return {
      searchQuery: null,
      resources: Resources
    };
  },
  computed: {
    resultQuery () {
      if (this.searchQuery) {return this.resources.filter((item) => {return this.searchQuery.toLowerCase().split(' ').every(v => item.city.toLowerCase().includes(v)) }) } else if (this.searchQuery) { return null } else {
        return this.resources
      }
    }
  },
  components: { Cards }
})

</script>

<style>
.Search {
  width: 400px;
  font-size: 18px;
  padding: 8px 20px;
  background-color: #e8e8e8;
  border-radius: 5px;
  border-color: transparent;
  margin-left: 2%;
  font-family: "MontserratLight";
}

.ButtondivContainer {
  height: 100%;
  width: 100%;
  flex-shrink: unset;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  padding: 1rem;
  }

.ButtoncolumnContainer {
  display: flex;
  width: 100%;
  height: 100%;
  flex-direction: row;
  padding-top: 1rem;
  justify-content: flex-start;
  align-items: flex-start;
}

.button2 {
  box-sizing: content-box;
  border-radius: 5px;
  border: 1px solid white;
  padding: 10px 55px;
  background: #eb5440;
  font-size: 15px;
  color: white;
  cursor: pointer;
  font-family: "MontserratSemiBold";
}

.button2:hover {
  background: white;
  color: #eb5440;
}

.NotFound{
  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>