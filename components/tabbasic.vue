<template>
    <div>
        <span class="tab"
        :class="{activeTab : selecttabs === tab}"
        v-for="(tab,index) in tabs" :key="index"
        @click="selecttabs = tab">
        {{tab}}
        </span>
        <div v-show="selecttabs === 'Review'">
                <p>tab review select</p>
        </div>
        <div v-show="selecttabs === 'Vote'">
            <Formbasic></Formbasic>
        </div>
    </div>
</template>
<script>
import Formbasic from '~/components/formbasic.vue';
export default ({
    components:{ Formbasic},
    props:{
        review:{
            type:Array,
            require:false
        }
    },
    data(){
        return{
            tabs:["Review","Vote"],
            selecttabs:"Vote",
        }
    }
})
</script>
