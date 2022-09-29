<template>
<div>
    <template-view>
        <div class="container mt-3">
            <div class="row">
                <div class="col-md-12">
                    <div class="card">
                        <div class="card-body">
                                <div class="row">
                                    <div class="col-md-4">
                                    <label for="name">Your Name: </label>
                                    <input class="form-control" type="text" placeholder="Enter First Name" v-model="name">
                                    </div>
                                    <div class="col-md-4">
                                        <label for="faculty">Faculty: </label>
                                        <input class="form-control" type="text" placeholder="Enter Your Faculty" v-model="faculty">
                                    </div>
                                    <div class="col-md-4">
                                        <label for="semester">Semester: </label>
                                        <input class="form-control" type="text" placeholder="Enter Your Semseter" v-model="semester">
                                    </div>
                                    <div class="row pt-5">
                                        <div class="col-md-12">
                                            <label for="description">Description: </label>
                                            <textarea class="form-control" type="text" placeholder="description" v-model="description"></textarea>
                                        </div>
                                    </div>
                                </div>
                                <button class="badge btn bg-primary float-end mt-3" @click="create_cv()">Submit</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <hr class="text-danger">
        <div class="container mt-3">
            <div class="row">
                <div class="col-md-10">
                    <div class="card" style="width: 500px; height: 300px; background-color: gray">
                        <span class="text-info">{{ result }}</span>
                    </div>
                </div>
            </div>
        </div>
    </template-view>
</div>
</template>

<script>
import TemplateView from './TemplateView.vue'

export default {
    name: 'GenerateView',
    components: { TemplateView },

    data(){
        return{
            name: null,
            faculty: null,
            semester: null,
            description: null,
            result: null,
        }
    },

    methods: {
        create_cv(){
            this.result = "My name is " + this.name + ". I am from " + this.semester + " and from "  
            + this.faculty + "." + " " + this.description
        }
    }
}
</script>

<style scoped>

</style>