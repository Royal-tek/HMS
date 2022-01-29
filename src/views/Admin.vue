<template>
<Navbar/>
    <div class="holder">
        <div class="container-fluid">
            <div class="row admin-row ">
                <div class="col-md-2 admin-link bg-light">
                    <div class="list">
                        <div class="admin-links" @click="page=1">
                            <i class="fa fa-bars fa-2x me-2"></i>
                            <h4>Referrals</h4>
                        </div>
                        <div class="admin-links" @click="page=2">
                            <i class="fa fa-home fa-2x me-2"></i>
                            <h4>Hospitals</h4>
                        </div>
                        <div class="admin-links" @click="page=3">
                            <i class="fa fa-heart fa-2x me-2"></i>
                            <h4>Patients</h4>
                        </div>
                        <div class="admin-links">
                            <i class="fa fa-users fa-2x me-2"></i>
                            <h4>Users</h4>
                        </div>
                    </div>
                
                </div>
                <div class="col">
                    <div class="container-fluid">
                        <div class="row my-3">
                        <div class="col">
                            <div class="card bg-light">
                                <div class="card-body card-up">
                                    <i class="fa fa-bars fa-3x "></i>
                                    <h4 class="text-justify">1</h4>
                                    
                                </div><hr>
                                <div class="cardfooter" @click="page=1">
                                    <h4 class="text-center">Referrals</h4>
                                </div>
                            </div>
                        </div>

                        <div class="col">
                            <div class="card bg-light">
                                <div class="card-body card-up">
                                    <i class="fa fa-home fa-3x "></i>
                                    <h4 class="text-justify">4</h4>
                                    
                                </div><hr>
                                <div class="cardfooter" @click="page = 2">
                                    <h4 class="text-center">Hospitals</h4>
                                </div>
                            </div>
                        </div>

                        <div class="col">
                            <div class="card bg-light">
                                <div class="card-body card-up">
                                    <i class="fa fa-heart fa-3x "></i>
                                    <h4 class="text-justify">10</h4>
                                    
                                </div><hr>
                                <div class="cardfooter" @click="page=3">
                                    <h4 class="text-center">Patients</h4>
                                </div>
                            </div>
                        </div>

                        <div class="col">
                            <div class="card bg-light">
                                <div class="card-body card-up">
                                    <i class="fa fa-users fa-3x "></i>
                                    <h4 class="text-justify">3</h4>
                                    
                                </div><hr>
                                <div class="cardfooter">
                                    <h4 class="text-center">Users</h4>
                                </div>
                            </div>
                        </div>

                        </div><hr style="background-color:blue">
                        <div class="row my-2">
                            
                            <div class="col-md-12">
                                <div class="container-fluid">
                                    <ManageRefers v-show="page == 1" />
                                    <Hospitals v-show="page == 2"/>
                                    <ManagePatients v-show="page==3"/>
                                    
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ManageRefers from '../components/ManageRefers.vue'
import ManagePatients from '../components/ManagePatients.vue' 
import Navbar from '../components/Navbar.vue'
import Hospitals from '../components/Hospitals.vue'
// import MakeReferral from '../components/MakeReferral.vue'
export default {
    name : 'holder',
    components : {
        Navbar, Hospitals, ManageRefers, ManagePatients
    },
    data() {
        return {
            page: 0
        }
    }
}
</script>

<style scoped lang="scss">
.admin-row{
    height: calc(100vh - 94px);
    
}

.admin-link{
    display: flex;
    // align-items: center;
    justify-content: center;
    border-top: 2px solid #1067cad3;
    // border-right: 2px solid #1067cad3;

    

}
.list{
    display: flex;
    align-items: center;
    width: 100%;
    flex-direction: column;
    margin: 10px 0 0 0;
}
.admin-links{
    width: 100%;
    margin: 20px 0;
    padding: 20px 15px;
    display: flex;
    background-color: #fff;
    border-radius: 10px;
    align-items: center;
    justify-content: space-around;
    border: 1px solid #1067cad3;
    cursor: pointer;
    transition: .5s;
    color: #1067cad3;

    
}
.admin-links:hover{
    background-color: #1067cad3;
    color: #fff;
}
.card{
    padding: 1px 15px 15px;

}
.card-up{
    display: flex;
    align-items: center;
    justify-content: space-between;

    i{
        color: #1067cad3;
    }

    h4{
        font-size: 40px;
        color: #1067cad3;
    }
}
.cardfooter{
    width: 100%;
    border: 1px solid transparent;
    padding: 10px;
    border-radius: 10px;
    background-color: #1067cad3;
    cursor: pointer;
    color: #fff;
    transition: .5s;

}
.cardfooter:hover{
    background-color: #fff;
    border: 1px solid #1067cad3;
    color: #1067cad3;
}
@media (max-width:1100px){
 
    .admin-link h4{
        // display: none;
        font-size: 15px;
    }
    .admin-link i{
        font-size: 20px;
    }
    .card-up h4{
        font-size: 20px;
    }
    .card-up i {
        font-size: 25px;
        margin-right: 10px;
    }
    .cardfooter h4{
        font-size: 14px;
    }
}
@media (max-width:768px){
    .admin-link{
        display: none;
    }
    .card{
        margin: 10px 0;
        padding: 8px .8px;
    }
    .cardfooter{
        width: 90%;
        margin: 0 auto;
    }
  
}
@media (max-width: 520px){
    .cardfooter{
        width: 90%;
        margin: 0 auto;
        
        h4{
            font-size: 10px;
        }
    }
    .card-up h4{
        font-size: 15px;
    }
    .card-up i{
        font-size: 18px;
    }
}

@media(min-width: 769px) 
{
    .cardfooter {
        pointer-events: none;
    }
}
</style>