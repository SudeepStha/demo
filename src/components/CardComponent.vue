<template>
  <div class="card" style="width: 18rem">
    <img :src="image" class="card-img-top" alt="" />
    <div class="card-body">
      <h5 class="card-title">{{title}}</h5>
      <p class="card-text">
        {{description}}
      </p>
      <a href="#" class="btn btn-primary" @click="sayhello()">Go somewhere</a>
    </div>
  </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props:[
      'title',
      'description',
      'image'
    ],
    methods: {
      sayhello(){
        alert(this.description)
      }
    },
}
</script>