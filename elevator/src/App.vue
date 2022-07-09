<template>
  
  <table>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call5" class="call" @click="call_Elevator(5)" value="5" ref="button1">5</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call4" class="call" @click="call_Elevator(4)" value="4" ref="button2">4</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call3" class="call" @click="call_Elevator(3)" value="3" ref="button3">3</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call2" class="call" @click="call_Elevator(2)" value="2" ref="button4">2</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td class="lvl"> <button id="call1" class="call" @click="call_Elevator(1)" value="1" ref="button5">1</button> </td></tr>
    <div id="elev" class="elev">
     <img id="elevator" class="elevator" src="https://www.fujihd.com/wp-content/uploads/2018/12/HD-JX01.jpg" @transitionend="stop_Elevator()"/>
    </div>
  </table>
    
</template>

<script>

export default {
  name: 'App',
  components: { },
  data(){
    return{
      calls: [],
      call: 0
    }
  },

  mounted(){
    //загрузка из локала переменных
  },

  methods: {

    call_Elevator(lvl){
      console.log('lvl=', lvl)
      if(this.calls.length > 0){
        for(let i=0; i<this.calls.length; i++){ //проверяем очередь на совпадение с выбранным этажом
          if(lvl == this.calls[i]){
            return;
          }
        }
      }
      this.calls.push(lvl) //тут в локал

      this.command_calls()
    },

    command_calls(){
      console.log('command calls', this.calls.length)
      if(this.calls.length > 0){
        console.log('calls=', this.calls)
        this.call = this.calls[0] //тут в локал
        console.log('call=', this.call)
        this.move_Elevator()
      }
    },

    move_Elevator() {
      let options = { 
        5: '65px',
        4: '225px',
        3: '380px',
        2: '540px',
        1: '700px'
      }
      console.log(this.call)
      console.log(options)
      document.getElementById('elevator').style.top = options[this.call]
    }, 

    stop_Elevator(){
      console.log('Stop elevator')
      this.calls.shift() //тут в локал
      setTimeout(this.command_calls, 3000)
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
  transition: all 2.7s ease-in-out;
  -webkit-transition: all 2.7s ease-in-out; /** Chrome & Safari **/
  -moz-transition: all 2.7s ease-in-out; /** Firefox **/
  -o-transition: all 2.7s ease-in-out; /** Opera **/
}

.elevator{
    top: 699px;
    left: 15px;
}

</style>
