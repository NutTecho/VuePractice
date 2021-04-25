<template>
<div class="container">
    <div class="card bg-dark text-white">
        <div class="card-body">
            <h2 class="card-title">
                {{headtitle}}
            </h2>
            <p class="card-text">
                content :{{datacontent}}
                Price : {{getprice}}
                Shipping : {{Shipping}}
            </p>
            <button @click="addtoCart" class="btn btn-success">click</button>
        </div>
    </div>
</div>
    
</template>
<script>
export default {
    props :
    {
        headtitle:{
            type:String,
            default:null
            //required:true
        },
        datacontent:{
            type:String,
            //required:true
        },
        getprice:{
            type:Number,
            required:true,
        }
        
    },
    methods:{
        addtoCart(){
            this.$emit('add-to-cart');
        },
    },
    computed:{
        Shipping(){
            if(this.getprice)
            {
                return "no fee"
            }
            return 2.00
        }
    }
}
</script>