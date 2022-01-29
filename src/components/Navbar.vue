<template>

    <nav class="navbar navbar-expand-lg navbar-light py-4 bg-light" id="navbar">
    <div class="container-fluid" style="width:90%">
        <a href="/" class="logo me-auto navbar-brand"><img src="" alt="" class="img-fluid">HMS</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
            <li><router-link to="/" :class="{active : $route.name == 'Home'}" class="nav-link" >Home</router-link></li>
            <li><router-link to="/about" :class="{active : $route.name == 'About'}" class="nav-link" >About</router-link></li>
            <li><router-link to="/ranking" :class="{active : $route.name == 'Ranking'}" class="nav-link" >Contact Us</router-link></li>
            <!-- <li><router-link to="/contact-us" :class="{active : $route.name == 'Contact'}" class="nav-link" ></router-link></li> -->
            <!-- <li><router-link to="/rules" :class="{active : $route.name == 'Rules'}" class="nav-link" >Rules</router-link></li> -->
            


            <!-- <li class="dropdown"><a href="#"><span :class="{active : $route.name == 'PostNews' || $route.name == 'LatestNews'}">News</span> <i class="bi bi-chevron-down"></i></a>
            <ul>
                <li><router-link to="/news/postnews" :class="{active : $route.name == 'PostNews'}">Post News</router-link></li>
                <li><router-link to="/news/latestnews" :class="{active : $route.name == 'LatestNews'}">Latest News</router-link></li>
            </ul>
            </li> -->

            <li class="sign-button" ><router-link to="/login" class="nav-link sign-in">Sign In</router-link></li>
            <li class="sign-up-button " ><router-link to="/register" class="nav-link text-white ">Sign Up</router-link></li>
            <li v-if="token" class="refer-button " ><router-link to="/refer" class="nav-link text-white ">Refer</router-link></li>



            
        
        </ul>
        <ul>
        
            
            </ul>
        
        </div>
    </div>
    </nav>
</template>
<script>
export default {
    name : 'Navbar'
}
</script>

<style scoped lang="scss">
#navbar{
    position: sticky;
    left: 0;
    top: 0;
    z-index: 10000;
}
.logo{
    font-weight: 900;
    color: #398cebd3;
}
.sign-button{
    padding: 0px 15px;
    margin: 2px 10px;
    border-radius: 8px;
    // color: black;
    border: 1px solid #1067cad3;


}
.sign-up-button{
    padding: 0px 15px;
    margin: 2px 10px;
    border-radius: 8px;
    background-color: #1067cad3 ;
    color: #fff !important;
    
}
.refer-button{
    padding: 0px 15px;
    margin: 2px 10px;
    border-radius: 8px;
    background-color: #1067cad3 ;
    color: #fff !important;
}
.sign-button:hover{
    background-color: #1067cad3;
    transition: 1s;

    .sign-in{
        color: white;
    }
    
}

@media (max-width:700px){
    .sign-button{
        margin:0 0 !important;
    }
}
</style>