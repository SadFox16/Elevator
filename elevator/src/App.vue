<template>
  
  <table>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call5" class="call" @click="move_Elevator5()" value="5" ref="button1">5</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call4" class="call" @click="move_Elevator4()" value="4" ref="button2">4</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call3" class="call" @click="move_Elevator3()" value="3" ref="button3">3</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call2" class="call" @click="move_Elevator2()" value="2" ref="button4">2</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call1" class="call" @click="move_Elevator1()" value="1" ref="button5">1</button> </td></tr>
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
      lvl: 0,
      el: ''
    }
  },

  methods: {

    move_Elevator5() {
      //let el = document.getElementById('elevator').style.top= "-636px"
      //.el.classList.add('move-up5')
      // setTimeout(() =>{ //задержка в ~3 сек и отправляем лифт вниз
      // this.get_Down5() }, 5000)
      //this.lvl = 5
      document.getElementById('elevator').style.top= "65px"
      // document.getElementById('call5').disabled = true
      // document.getElementById('call4').disabled = true
      // document.getElementById('call3').disabled = true
      // document.getElementById('call2').disabled = true
      // document.getElementById('call1').disabled = true
      setTimeout(function(){
      document.getElementById('call4').disabled = false
      document.getElementById('call3').disabled = false
      document.getElementById('call2').disabled = false
      document.getElementById('call1').disabled = false
      },3000);
      // setTimeout(() => 3000)
      // document.getElementById('call4').disabled = 'false'
      // document.getElementById('call3').disabled = 'false'
      // document.getElementById('call2').disabled = 'false'
      // document.getElementById('call1').disabled = 'false'
      },
    // get_Down5(){
    //   let el = document.getElementById('elevator')
    //   el.classList.remove('move-up5') //двигаемся вниз, удаляя класс
    //   this.lvl = 0
    // }, 

    move_Elevator4() {
      // this.lvl = 4
      // let el = document.getElementById('elevator')
      // el.classList.add('move-up4')
      // setTimeout(() =>{ //задержка в ~3 сек и отправляем лифт вниз
      // this.get_Down4() }, 5000)
      document.getElementById('elevator').style.top= "225px"
      // document.getElementById('call5').disabled = true
      // document.getElementById('call4').disabled = true
      // document.getElementById('call3').disabled = true
      // document.getElementById('call2').disabled = true
      // document.getElementById('call1').disabled = true
      setTimeout(function(){
      document.getElementById('call5').disabled = false
      document.getElementById('call3').disabled = false
      document.getElementById('call2').disabled = false
      document.getElementById('call1').disabled = false
      },3000);
      //  setTimeout(() => 3000)
      // },
    // get_Down4(){
    //   let el = document.getElementById('elevator')
    //   el.classList.remove('move-up4') //двигаемся вниз, удаляя класс
    //   this.lvl = 0
    }, 

    move_Elevator3() {
      // let el = document.getElementById('elevator')
      // el.classList.add('move-up3')
      // setTimeout(() =>{ //задержка в ~3 сек и отправляем лифт вниз
      // this.get_Down3() }, 5000)
       //this.lvl = 3
      document.getElementById('elevator').style.top= "380px"
      // document.getElementById('call5').disabled = true
      // document.getElementById('call4').disabled = true
      // document.getElementById('call3').disabled = true
      // document.getElementById('call2').disabled = true
      // document.getElementById('call1').disabled = true
      setTimeout(function(){
      document.getElementById('call5').disabled = false
      document.getElementById('call4').disabled = false
      document.getElementById('call2').disabled = false
      document.getElementById('call1').disabled = false
      },3000);
      // setTimeout(() => 3000)
      // },
    // get_Down3(){
    //   let el = document.getElementById('elevator')
    //   el.classList.remove('move-up3') //двигаемся вниз, удаляя класс
    }, 

    move_Elevator2() {
      // let el = document.getElementById('elevator')
      // el.classList.add('move-up2')
      // // setTimeout(() =>{ //задержка в ~3 сек и отправляем лифт вниз
      // // this.get_Down2() }, 5000)
      //  this.lvl = 2
      document.getElementById('elevator').style.top= "540px"
      // document.getElementById('call5').disabled = true
      // document.getElementById('call4').disabled = true
      // document.getElementById('call3').disabled = true
      // document.getElementById('call2').disabled = true
      // document.getElementById('call1').disabled = true
      setTimeout(function(){
      document.getElementById('call5').disabled = false
      document.getElementById('call4').disabled = false
      document.getElementById('call3').disabled = false
      document.getElementById('call1').disabled = false
      },3000);
      // setTimeout(() => 3000)
      // },
    // get_Down2(){
    //   let el = document.getElementById('elevator')
    //   el.classList.remove('move-up2') //двигаемся вниз, удаляя класс
    }, 

    move_Elevator1() {
      // let el = document.getElementById('elevator')
      // el.classList.add('move-up1')
      // setTimeout(() =>{ //задержка в ~3 сек и отправляем лифт вниз
      // this.get_Down1() }, 5000)
       //this.lvl = 1
      document.getElementById('elevator').style.top= "700px"
      // document.getElementById('call5').disabled = true
      // document.getElementById('call4').disabled = true
      // document.getElementById('call3').disabled = true
      // document.getElementById('call2').disabled = true
      // document.getElementById('call1').disabled = true
      setTimeout(function(){
      document.getElementById('call5').disabled = false
      document.getElementById('call4').disabled = false
      document.getElementById('call3').disabled = false
      document.getElementById('call2').disabled = false
      },3000);
      // setTimeout(() => 5000)
      // },
    // get_Down1(){
    //   let el = document.getElementById('elevator')
    //   el.classList.remove('move-up1') //двигаемся вниз, удаляя класс
    },   
  },
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
