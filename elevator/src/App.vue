<template>

  <img id ="stop" class="stop" src="data:image/png;base64,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" alt="Stop">
  
  <table>
    <tr><td class="elevator_sh"> </td><td><button id="call5" @click="call_Elevator(5)">5</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td><button id="call4" @click="call_Elevator(4)">4</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td><button id="call3" @click="call_Elevator(3)">3</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td><button id="call2" @click="call_Elevator(2)">2</button> </td></tr>
    <tr><td class="elevator_sh"> </td><td><button id="call1" @click="call_Elevator(1)">1</button> </td></tr>
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
      call: 0,
    }
  },

  mounted(){ 
    console.log(localStorage)
    if(localStorage.getItem('call') != 0){
      this.call = localStorage.getItem('call')
      console.log('call=', this.call)
    }else{
      this.call = 0
    }
    console.log('localStorage.calls=', localStorage.calls)
    if(JSON.parse(localStorage.getItem('calls')).length != 0){
      this.calls = this.calls.concat(JSON.parse(localStorage.getItem('calls')))
      console.log('calls=', this.calls)
    }else{
      this.calls.length = 0
    }
    this.move_Elevator()
  },

  methods: {

    call_Elevator(lvl){
      if(this.calls.length > 0){
        for(let i=0; i<this.calls.length; i++){
          if(lvl == this.calls[i]){
            return;
          }
        }
      }
      this.calls.push(lvl)
      this.command_calls()
    },

    command_calls(){
      document.getElementById('stop').style.display = 'none'
      if(this.calls.length > 0){
        this.call = this.calls[0]
        localStorage.setItem('call', this.call)
        setTimeout(this.move_Elevator, 500)
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
      document.getElementById('elevator').style.top = options[this.call]
    }, 

    stop_Elevator(){
      this.calls.shift()
      localStorage.setItem('calls', JSON.stringify(this.calls))
      document.getElementById('stop').style.display = 'block'
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

img.up{
  display: none;
  padding-left: 900px;
  margin-left: 610px;
}

img.down{
  display: none;
  margin-left: 1500px;
  margin-top: 650px;
}

img.stop{
  display: none;
  margin-left: 1500px;
  margin-top: 300px;
}

</style>
