<template>
  
  <table>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call5" class="call" @click="call_Elevator(5)" value="5" ref="button1">5</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call4" class="call" @click="call_Elevator(4)" value="4" ref="button2">4</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call3" class="call" @click="call_Elevator(3)" value="3" ref="button3">3</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call2" class="call" @click="call_Elevator(2)" value="2" ref="button4">2</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call1" class="call" @click="call_Elevator(1)" value="1" ref="button5">1</button> </td></tr>
    <div id="elev" class="elev">
     <img id="elevator" class="elevator" src="https://www.fujihd.com/wp-content/uploads/2018/12/HD-JX01.jpg"/>
    </div>
    </table>
    
</template>

<script>

export default {
  name: 'App',
  components: { },
  data(){
    return{
      calls: []
    }
  },

  methods: {

    call_Elevator(lvl){
      this.calls.push(lvl)
      console.log(this.calls)
        if(this.calls[0] == 1){
          this.move_Elevator1()
          this.calls.shift()
          console.log(this.calls)
        }else if(this.calls[0] == 2){
          this.move_Elevator2()
          this.calls.shift()
          console.log(this.calls)
        }else if(this.calls[0] == 3){
          this.move_Elevator3()
          this.calls.shift()
          console.log(this.calls)
        }else if(this.calls[0] == 4){
          this.move_Elevator4()
          this.calls.shift()
          console.log(this.calls)
        }else if(this.calls[0] == 5){
          this.move_Elevator5()
          this.calls.shift()
          console.log(this.calls)
        }
      },

    move_Elevator5() {
      document.getElementById('elevator').style.top= "65px"
      document.getElementById('call5').disabled = true
      setTimeout(3000)
      document.getElementById('call5').disabled = false
      },

    move_Elevator4() {
      document.getElementById('elevator').style.top= "225px"
      document.getElementById('call4').disabled = true
      setTimeout(() => 3000)
      document.getElementById('call5').disabled = false
    }, 

    move_Elevator3() {
      document.getElementById('elevator').style.top= "380px"
      document.getElementById('call3').disabled = true
      setTimeout(() => 3000)
      document.getElementById('call5').disabled = false
    }, 

    move_Elevator2() {
      document.getElementById('elevator').style.top= "540px"
      document.getElementById('call2').disabled = true
      setTimeout(() => 3000)
      document.getElementById('call5').disabled = false
    }, 

    move_Elevator1() {
      document.getElementById('elevator').style.top= "700px"
      document.getElementById('call1').disabled = true
      setTimeout(() => 5000)
    },   
  }
}

</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

table {
   border: 1px solid black;
    width: 1500px;
    height: 500px;
    text-align: left;
}

tr{
  border: 1px solid black;
  width: 1000px;
}

td {
   border: 2px solid black;

}

td.elevator_sh{
  width: 150px;
  height: 150px;
}

img{
  width: 150px;
  height: 150px;
  position: absolute;
  transition: all 2.5s ease-in-out;
  -webkit-transition: all 2.5s ease-in-out; /** Chrome & Safari **/
  -moz-transition: all 2.5s ease-in-out; /** Firefox **/
  -o-transition: all 2.5s ease-in-out; /** Opera **/
}

.elevator{
    top: 699px;
    left: 15px;
}

#elev .move-up5 {
    transform: translate(0,-636px);
    -webkit-transform: translate(0,-636px);
    -o-transform: translate(0,-636px);
    -moz-transform: translate(0,-636px);
} 

#elev .move-up4 {
    transform: translate(0,-477px);
    -webkit-transform: translate(0,-477px);
    -o-transform: translate(0,-477px);
    -moz-transform: translate(0,-477px);
} 

#elev .move-up3 {
    transform: translate(0,-318px);
    -webkit-transform: translate(0,-318px);
    -o-transform: translate(0,-318px);
    -moz-transform: translate(0,-318px);
} 

#elev .move-up2 {
    transform: translate(0,-159px);
    -webkit-transform: translate(0,-159px);
    -o-transform: translate(0,-159px);
    -moz-transform: translate(0,-159px);
} 

#elev .move-up1 {
    transform: translate(0,0px);
    -webkit-transform: translate(0, 0px);
    -o-transform: translate(0,0px);
    -moz-transform: translate(0,0px);
} 

</style>
