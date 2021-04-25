<template>
<div class="container-fluid">
    <b-row>
       <Header/> 
    </b-row>
    <div class="container">
        <Postcontent/>
    </div>
   <div class="container" v-for="post in posts" :key="post.getid">
            <p>{{post.getid}} | {{post.FirstName}} | {{post.LastName}} | {{post.Age}} | {{post.Toy}}</p>
     </div>
   
</div>
</template>

<script>
import Header from '@/components/header'
import Postcontent from '@/components/postcontent'
export default {
    layout:"corelayout",
    components:{ Header,Postcontent },
     data(){
        return {
             posts: [],
        }
    },
    async asyncData({ $axios },callback) {
         //  get('https://jsonplaceholder.typicode.com/todos')
        await $axios.get('http://localhost:8080/adddata/getold')
        .then((res) => {
            callback(null,{posts : res.data})
        })
        },
     head: {
        title: 'รายการโพสต์'
    }

    }
   
</script>
