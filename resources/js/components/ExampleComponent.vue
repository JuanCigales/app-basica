<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Skills</div>

                    <div class="card-body">
                        <div v-for="(input, i) in inputs" :key="i" class="d-flex p0">
                            <div class="col-10">
                                <input class="form-control" type="text" name="skills[]" v-model="inputs[i]"> 
                            </div>
                            <div class="col-2">
                                <button class="btn btn-danger">Delete</button>
                            </div>
                        </div>
                        <div>
                            <button class="btn btn-primary">Add</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        },

        data(){
            return{
                inputs: ['uno', 'dos', 'tres'],
            }
            },

        methods:{
            sumNum(){
                this.num++;  
            }
        }
    }
</script>
