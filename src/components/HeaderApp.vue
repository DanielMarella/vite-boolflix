<template>
    <header class="mb-5">
        <div class="container-fluid d-flex justify-content-between align-items-center mb-3" >
            <ul class="d-flex mt-3 align-items-baseline">
                <!-- img logo by Emanuela Pau class 98# Boolean -->
                <li><img src="../assets/img/boolflix_logo.png" alt=""></li>
                <li><a href="#">Home</a></li>
                <li><a href="#">Serie TV</a></li>
                <li><a href="#">Film</a></li>
                <li><a href="#">Originali</a></li>
                <li><a href="#">Aggiunti di recente</a></li>
                <li><a href="#">La mia lista</a></li>
            </ul>
            <ul class="user  mr-5 mt-3  ">
                <li><a href="#"><font-awesome-icon icon="fa-regular fa-bell" size="2x" style="color: #aeae03;" /></a></li>
                <li><a href="#"><font-awesome-icon icon="fa-regular fa-user" size="2x" style="color: #ff00009e;" /></a></li>
            </ul>
        </div>
    </header>
</template>


<script>
    name : 'HeaderApp'
export default {
    
}
</script>

<style lang="scss" scoped>

    header{
        border-bottom: 2px solid red;
        background-color: #2b2a33;
    }
    a{
        text-decoration: none;
        color: white;
    }

    ul{
        list-style-type: none;

        img{
            width: 100px;
        }
    }
    
    li{
        margin: 0 10px;
    }



    .user{
        display: flex;
        margin-right: 50px;
    }
</style>