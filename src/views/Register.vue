<template>
<Navbar/>
    <div class="register-holder">
        <!-- <h1>This is the register page</h1> -->
        <div class="container">
        <div class="row">
    
        <div class="col-md-12 register-part">
            <form action="" class = "register-form  bg-light" @submit.prevent="register">
            <h1 class="text-dark text-center py-3 text-uppercase reg-text">Register</h1>
            <div class="input-group">
                <input type="text" v-model="first_name" class="form-control shadow-none" placeholder="FirstName">
            </div>
            <div class="input-group ">
                <input type="text" v-model="last_name" class="form-control shadow-none" placeholder="LastName">
            </div>
            <div class="input-group">
            <select name="" id="" class="form-control" v-model="gender">
                <option value="">*** Select Gender ***</option>
                <option value="MALE">Male</option>
                <option value="FEMALE">Female</option>
            </select>
            </div>

            <div class="input-group">
                <input type="date" v-model="dob" class="form-control shadow-none" placeholder="Date Of Birth">
            </div>
            <div class="input-group">
                <input type="email" v-model="email" class="form-control shadow-none" placeholder="Email">
            </div>
            <div class="input-group">
                <input type="password" v-model="password" class="form-control shadow-none" placeholder="Password">
            </div>
            
            <div class="input-group">
                <input type="password" v-model="confirm_password" class="form-control shadow-none" placeholder="Confirm Password">
            </div>
            <input type="submit" value="SUBMIT" class="btn register-button">
            <p class="info-text">Already have an account? <span><router-link to="login">Login</router-link></span></p>
        </form>

        </div>
        
        </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
import Navbar from '../components/Navbar.vue'
export default {
    name : 'Register',
    components : {
        Navbar,
    },
    data(){
        return{
            first_name : "",
            last_name : "",
            gender : "",
            dob : "",
            email : "", 
            password : "",
            confirm_password : ""
        }

    },
    methods : {
        register(){
            const Formdata = {
                first_name : this.first_name,
                last_name : this.last_name,
                gender : this.gender,
                dob : this.dob,
                email : this.email,
                password : this.password,
                confirm_password : this.confirm_password
            }
            axios.post('https://hms-lmu.herokuapp.com/api/auth/register/', Formdata)
            .then(response=>{
                console.log(response)
            })
            .catch(error=>{
                console.log(error)
            })
        }
    }

}
</script>

<style scoped lang="scss">
    .register-holder{
        background: radial-gradient(rgba(42, 42, 46, 0.7), rgba(148, 151, 199, 0.5)) , url(/images/group.jpg);
        width:100%;
        height: calc(100vh - 94px);
        display: flex;
        align-items: center;
        justify-content: center;
        background-position: center;
        background-attachment: fixed;
        background-size: cover;
    }
    .reg-text::after{
        display: block;
        margin: 10px auto;
        height: 3px;
        width: 50px;
        content: '';
        background-color: #1067cad3 ;
    }

    .register-form input {
        padding: 15px;
        font-family: inherit;
        font-size: 16px;
        border-radius: 10px;
    }


    .register-form{
        padding: 1em 3em;
        // opacity: .8;
        z-index: 100;
        border-radius: 30px;
        max-width: 600px;
        margin: 0 auto;
    }

.register-form > div {
    margin-bottom:20px ;
}

    .register-button{
        display: block;
        margin: 0 auto;
        background: #1067cad3;
        color: #fff;
        font-family: inherit;
        font-size: 16px;
        text-transform: capitalize;
        width: 100%;
        font-weight: bold;
    }
    .register-button:hover{
        background: #2482eed3;
        color: white;
        
        transition: 1s;
    }
    .info-text{
        padding: 10px 0;
        text-align: center;
        // font-weight: bold;
        color: black;
        // margin: 0 auto;
        
        span a{
            text-decoration: none;
            font-weight: bold;
            color: #1067cad3 ;
        }
    }
</style>