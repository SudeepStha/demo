<template>
  <div>
    <template-view>
        <div class="container">
            <h1>This is my ContactView Page</h1>
            <input type="text" placeholder="Enter your name.." v-model="name">
            <button @click="sayhello()">Submit</button>

            <div>
              <div class="class">
                {{result}}
              </div>
            </div>

        </div>
    </template-view>
  </div>
</template>

<script>
import TemplateView from './TemplateView.vue'

export default {
  name: 'ContactView',
  components: { TemplateView },

  //Data 
  data(){
    return{
      name: null,
      result: null,
    }
  },
  //Computed
  //Methods
  methods: {
    sayhello(){
      this.result = "Hello" + " " + this.name + " " + "How are you today?"
    }
  }
  //Mounted
  //Created
  //Watch
}
</script>

<style scoped>
.class{
  height: 20px;
  /* background-color: red; */
}
</style>