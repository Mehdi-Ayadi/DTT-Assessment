<template>
    <div>
        <div class="Back">
            <div class="divContainer" style="padding-top: 120px; padding-left: 100px; padding-right: 100px; display: inline-block;">
                    <img class="icon3" onclick="history.back()" src="../assets/images/ic_back_grey@3x.png"/>
                    <span class="BigText1">Back to overview</span>
            </div>
      </div>
    </div>
</template>
<script>
export default {
}
</script>
<style>

.Back{
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 1rem;
  padding-left: 20px;
}

.BigText1{
  font-family: "MontserratSemiBold";
  font-size: 20px;
}

.icon3{
  width: 20px;
  height: 20px;
  padding-top: 5px;
}

</style>