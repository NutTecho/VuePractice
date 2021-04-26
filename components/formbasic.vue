<template>
<form class="form-group" @submit.prevent="onSubmit">
    <p>
        <label for="name">Name : </label>
        <input v-model="name" id="name" required/>
    </p>
    <p>
        <label for="insertcomment">Comment : </label>
        <input v-model="insertcomment" id="insertcomment" required/>
    </p>
    <p>
        <label for="rating">Rating : </label>
        <select id="rating" v-model="rating">
            <option>5</option>
            <option>4</option>
            <option>3</option>
            <option>2</option>
            <option>1</option>
        </select>
    </p>
    <p>
        <input type="submit" value="Submit">
    </p>
</form>
</template>
<script>

export default ({
   data(){
       return{
           name:null,
           insertcomment:null,
           rating:null
       }
   },
   methods:{
       onsubmit(){
           let productReview = {
               name : this.name,
               insertcomment : this.insertcomment,
               rating : this.rating
           }
           this.name = null,
           this.insertcomment = null,
           this.rating = null
       }
   }
})
</script>
