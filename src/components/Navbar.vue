<template>
    <div>
        <b-navbar toggleable='lg' type="dark" variant="success">
           <div class="nav">
                <img src="https://freepngimg.com/download/innovation/3-2-innovation-transparent.png">
            </div>

            <div class="signin">
                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                <b-collapse id="nav-collapse" is-nav>
                <!-- Right align nav item -->
                <b-navbar-nav class="ml-auto">
                    <div class="nav-collapse"><b-nav-item @click="gotologin" active>Sign-In</b-nav-item></div>
                    <div class="nav-collapse"><b-nav-item @click="gotocart" active>Shopping Cart</b-nav-item></div>
                    

                   
                </b-navbar-nav>
            </b-collapse>
            </div>
            
        </b-navbar>



    </div>

</template>


<script>
export default {
    data() {
        return {
           
        }
    },
    created(){
        
    },
    methods:{
        gotocart(){
            this.$router.push('/cart')
        },
        gotologin(){
            this.$router.push('/login')
        },
        goHome(){
            this.$router.push('/')
        },
    }
}
</script>

<style>
.nav img{
    height: 35px;
    margin-left:118px ;
}

.signin{
    margin-left: 770px;
}

.nav-collapse{
    transition: transform 250ms;
}

.nav-collapse:hover{
    background-color: rgb(39, 37, 37);
    transform: scale(1.08);
    border-radius: 2px;
}
</style>