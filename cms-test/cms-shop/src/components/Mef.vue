<template>
  <div class="test">
    <div class="inside">
      <!-- 1 -->
    <div class="row">
      <div width="55px" height="55px">
      <div class="border-around">
        <img class="avatar" src="../assets/hugh.jpg" alt="Hugh" />
        </div>
      </div>
      <div class="column-test">
        <label class="hugh">HUGH IS</label>
        <input placeholder="7" type="number" class="input-test input-bold" maxlength="40"/>
      </div>
      <p class="hours">hours old</p>
    </div>
    <!-- 2 -->
    <div class="row">
      <div width="55px" height="55px"> 
        <div class="border-around">
        <img class="avatar" src="../assets/hugh.jpg" alt="Hugh" />
        </div>
      </div>
      <div class="column-test">
        <label class="hugh">HUGH IS</label>
        <input placeholder="10000" value="10000" type="number" class="input-test input-bold" maxlength="40"/>
      </div>
        <p class="hours">hours old</p>
    </div>
    <!-- 3 -->
    <div class="row" v-bind:class="[flagColor2 ? 'colorClick' : '']">
      <div width="55px" height="55px"> 
        <div class="border-around">
        <img class="avatar" src="../assets/hugh.jpg" alt="Hugh" />
        </div>
      </div>
      <div class="column-test">
        <label class="hugh">HUGH IS</label>
        <input @click="toggle2"  @keypress="inputLarge($event)"  maxlength="20" v-if="flagWidth2"  placeholder="10000" value="10000" type="number" class="input-test input-bold" />

      </div>
        <p class="hours">hours old</p>
    </div>
    <!-- 4 -->
    <div class="row" v-bind:class="[flagColor ? 'colorClick' : '']" >
      <div width="55px" height="55px"> 
        <div class="border-around">
        <img class="avatar" src="../assets/hugh.jpg" alt="Hugh" />
        </div>
      </div>
      <div  class="column-test">
        <label class="hugh">HUGH IS</label>
        <input @click="toggle"  @keypress="inputLarge($event)"  maxlength="20" v-if="flagWidth"  placeholder="10000" value="10000" type="number" class="input-test input-bold" />
        <input @click="toggle"  @keypress="inputLarge($event)" maxlength="20" v-else width="widthIn" placeholder="10000" value="10000" type="number" class="input-test-large input-bold" />
      
      </div>
        <p class="hours">hours old</p>
    </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Mef",
  data() {
    return {
      flagWidth:true,
      flagWidth2:true,
      widthIn: null,
      flagColor: false,
      flagColor2: false,
    }
  },
  methods: {
    inputLarge(e){
      
      if (e.target.value.length > 5 && e.target.value.length<40 ) {
        this.widthIn = ((e.target.value.length +5)) +'px';
        console.log('widthIn',this.widthIn);
        return this.flagWidth = false
      }
      return this.flagWidth = true
      // console.log(e.target.value.length);
    },
    toggle(){
      return this.flagColor = !this.flagColor
    },
    toggle2(){
      return this.flagColor2 = !this.flagColor2
    },
  },
};
</script>
<style lang="css" scoped>
:root {
  --charcoal-grey: #36454F;
}
.test {
  position: absolute;
  width: 333px;
  height: 406px;
  border: 1px solid silver;
  top: 50%;
  left: 50%;
  margin-right: -50%;
  transform: translate(-50%, -50%);
}
.row {
  margin-left: auto;
  height: 60px;
  margin-top: 32px;
}
.colorClick .hugh  {
  color:  #2540ff
}
.colorClick .border-around{
  width: 60px;
  height: 60px;
  border: solid 2px #2540ff !important;
  border-radius: 50% 50% 50% 40%;
}
.colorClick .input-test {
  border-bottom: solid 2px #2540ff !important;
}
.input-test {
  width: 50px;
  margin: 8px 1px 0 0;
  border-bottom: 1px solid silver;
  padding-bottom: 8px;
  outline:none;
}
.input-test-large{
  width: 90px;
  margin: 8px 1px 0 0;
  border-bottom: 1px solid silver;
  padding-bottom: 8px;
  outline:none;
}
.column-test {
  display: flex;
  flex-direction: column;
  height: 50px;
  justify-content: space-around;
  margin-left: 16px;
  margin-right: 8px;
}
.hours{
  width: 59px;
  height: 17px;
  margin-top: 30px;
  font-family: 'Roboto';
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.21;
  letter-spacing: normal;
  color: var(--charcoal-grey);
}
.hugh{
  font-family: 'Roboto';
  font-size: 13px;
  font-weight: bold;
  font-stretch: condensed;
  font-style: normal;
  line-height: 1.31;
  letter-spacing: 0.8px;
  text-align: center;
  color: var(--charcoal-grey);
}

.input-bold{
  font-family: 'Roboto';
  font-size: 14px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.21;
  letter-spacing: normal;
  color: var(--charcoal-grey);
}
.inside{
  margin: 24px 0px 62px 20px !important;
}
.avatar{
  border-radius: 50%;
}
</style>
