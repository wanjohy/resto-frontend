<template>
    <div class="nav">
        <router-link to="/">Home</router-link>
        <router-link to="add-restaurant">AddResto</router-link>
        <router-link to="update-restaurant">UpdateRest</router-link>
        <router-link to="#">Additional</router-link>
        <a v-on:click="logout" href="#">logout</a>
    </div>
</template>
<script>
export default{
    name: "HeaderComponent",
    methods:{
        logout(){
            alert("You will be logged out")
            localStorage.clear()
            this.$router.push({name:'LoginPage'})
        }
    }
}
</script>
<style>
.nav{
    background-color: #333;
    overflow: hidden;
}
.nav a{
    float:left;
    color: white;
    padding: 14px 16px;
    text-align: center;
    font-size: 17px;
    text-decoration: none;
    margin-right: 5px;

}
.nav a:hover{
    background: #ddd;
    color: #333;
}
</style>