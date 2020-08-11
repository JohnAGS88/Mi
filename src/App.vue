<template>
  <div id="app">
    <form action="">
      <div>
      <HelloWorld/>
          </div>
            <div class="container mr-4">
              <div class="columns">
                <div class="column is-4 is-offset-4">
                  <h3 class="title is-5">WEEK</h3>
                    <b-field label="Select a date">
                      <b-datepicker
                        placeholder="Type or select a date..."
                        icon="calendar-today"
                        editable>
                    </b-datepicker>
                  </b-field>
                <div class="field">
                  <label class="label">One Week</label>
                <div class="control">
                  <input class="input" type="number" v-model.number="ValorA"  placeholder="0">
                </div>
                  <label class="label">Two Weeks</label>
                <div class="control">
                  <input class="input" type="number" v-model.number="ValorB"  placeholder="0">
                </div>
                  <label class="label">Tree Weeks</label>
                <div class="control">
                  <input class="input" type="number" v-model.number="ValorC" placeholder="0">
                </div>
                  <label class="label">Four Weeks</label>
                <div class="control">
                  <input class="input" type="number" v-model.number="ValorD" placeholder="0">
                </div> 
                <div>
                  <p>Total {{ suma() }}<p/>
                </div>
                  <button type="summit" class="button is-primary mr-1" >Close</button>
                  <button type="summit" class="button is-danger" >Saves Changes</button>
              </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {  
  name: 'Form',
  data(){ 
    return{
      ValorA: '',
      ValorB: '',
      ValorC: '',
      ValorD: '',
    }
  },
  methods:{
    suma:function(){
        return "Decline:"+(this.ValorA+this.ValorB+this.ValorC+this.ValorD)
    }
  },
  components: {
    HelloWorld
  }
}
</script>




