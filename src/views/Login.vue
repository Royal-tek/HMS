<template>
  <div>
    <Navbar />
    <div class="login-holder">
    <div class="container">
        <div class="row">
            <div class="col-md-12 login-part">
            <form action="" class="login-form bg-light">
                <h1 class="login-text text-uppercase text-center py-2">Login</h1>
                <div class="input-group">
                    <input type="text" placeholder="Username" class="form-control shadow-none">
                </div>
                <div class="input-group">
                    <input type="text" placeholder="Password" class="form-control shadow-none">
                </div>
                <input type="submit" value="LOGIN" class="btn login-btn">
                <p class="text-dark info-text">Don't have an account? <span><router-link to="register">Sign Up </router-link></span></p>

            </form>
            </div>
        </div>
        </div>
    </div>
    </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
export default {
  name: "Login",
  components: {
    Navbar,
  },
};
</script>

<style scoped lang="scss">
.login-holder{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: calc(100vh - 94px);
    background: radial-gradient(rgba(42, 42, 46, 0.7), rgba(148, 151, 199, 0.5)) , url(/images/group.jpg);
    background-position: center;
    background-attachment: fixed;
    background-size: cover;
}
.login-form{
    max-width: 600px;
    // opacity: .8;
    z-index: 100;
    border-radius: 20px;
    padding: 3em 3em;
    margin: 0 auto;

    .input-group input{
        margin: 10px 0;
        padding: 15px;
    } 
    
}
.login-text{
    color: #000;
}
.login-text::after{
    
        content: '';
        display: block;
        margin: 10px auto;
        width: 30px;
        height: 3px;
        background-color: #1067cad3;
    
}
.login-btn{
    width: 100%;
    background-color: #1067cad3;
    margin: 10px 0 auto;
    display: block;
    font-weight: bold;
    font-size: 16px;
    transition: 1s;
    z-index: 101;
    padding: 13px;
    color: #fff;
}
.login-btn:hover{
    background-color: #2482eed3;
    
}
.info-text{
        padding: 10px 0;
        text-align: center;
        // margin: 0 auto;

        span a{
            text-decoration: none;
            font-weight: bold;
            color: #1067cad3 ;
        }
    }
</style>