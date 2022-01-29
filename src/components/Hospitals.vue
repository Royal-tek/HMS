<template>
<div class="holder bg-light">
    <div class="second-holder">
        <div class="hospital-menu">
            <div @click="page=1">Add Hospital</div>
            <div @click="page=2">Manage Hospitals</div>
        </div>
        
    </div>
    <!-- <div v-show=""></div> -->
    <AddHospital v-show="page == 1"/>
    <ManageHospitals v-show="page == 2"/>
    
</div>
</template>

<script>
import ManageHospitals from './ManageHospitals.vue'
import AddHospital from './AddHospital.vue'
export default {
    name : 'Hospital',
    components:{
        ManageHospitals, AddHospital
    },
    data(){
        return{
            page:0
        }
    }
}
</script>

<style scoped lang="scss">

.second-holder{
    width: 100%;
    // height: auto;
    display: flex;
    padding: 20px;
    justify-content: center;
    overflow: auto;
}
.hospital-menu{
    display: flex;
    border: 1px solid #1067cad3;
    align-items: center;
    justify-content: center;
    // background-color: red;
    width: 100%;
    
    div{
        margin: 10px 20px;
        padding: 25px 30px;
        border-radius: 10px;
        display: flex;
        align-items: center;
        background-color: #1067cad3;
        color: #fff;
        height: 5%;
        cursor: pointer;
        // border: 1px solid transparent;
        transition: 1s;

        &:hover{
            color: #fff;
            background-color: #06468fd3;
            // border: 1px solid #1067cad3;
        }
    }
}
@media (max-width:600px){
    .hospital-menu {
        div{
            font-size: 14px;
            text-align: center;
        }
    }
    
}
</style>