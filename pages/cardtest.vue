<template>
    <div class="container-fluid">
        <h2 class="text-center">Assembly Line {{$route.params.name}}</h2>
        <hr/>
        <div class="card-deck">
            <div class="card bg-danger border-light mb-3 text-white"
             v-for="item in items" :key="item.id">
                <div class="card-body">
                    <h1 class="card-title text-right"><b>{{item.line}}</b></h1>
                    <p class="card-text" >
                        Assembly Line {{item.ndata}}
                    </p>
                    <p>
                        <nuxt-link :to="{ name: 'rawdata' ,params: { xline: item.line ,partstock:8}}" class="btn button--grey">
                            Rawdata
                        </nuxt-link>
                    </p>
                    
                </div>
            </div>
        </div>
        <div>
            <Cardassy
            headtitle="testprops"
            datacontent="xxxxx"
            :getprice="50"
            />
            <nuxt-child/> 
        </div>
       
    </div>
    
</template>

<script>
import Cardassy from '~/components/cardassy.vue';
export default {
    layout : "corelayout",
    components:{ Cardassy },
    data(){
        return {
          items: [
                {line:"A",ndata: 10},
                {line:"B",ndata: 12},
                {line:"C",ndata: 14},
                {line:"D",ndata: 16},
                {line:"E",ndata: 18},
            ]

        }
    },
     methods: {
      hoverHandler(isHovered) {
        if (isHovered) {
          // Do something
          console.log('hover on');
        } else {
          // Do something else
          console.log('hover off')
        }
      }
    }
    
}
</script>
<style>
    .card{
        transition:  trasform .2s;
    }
    .card:hover{
        transform: scale(1.2);
    }

</style>