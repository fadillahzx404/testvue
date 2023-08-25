<template>
    <div id="dashboard" class="dashboard">
        
        <SidebarCom />

    <div class="dashboard-page vw-100">
        <NavbarDash />
        <div class="container-fluid dashboard-content">
            <h1>Dashboard</h1>
            <div class="text-center mt-5">
            <h1 class="text-control">Welcome user this just a begin.</h1>
            </div>
        </div>
        
    </div>
</div>

</template>


<script>
import "bootstrap/dist/css/bootstrap.css";
import SidebarCom from '@/components/Sidebar.vue';
import NavbarDash from '@/components/NavbarDash.vue';

export default {
    name: "DashboardView",
    components: {
        SidebarCom,
        NavbarDash,
    },
};

</script>

<style lang="scss" scoped>

#dashboard{
 display: flex;

 
 main{
    flex: 1 1 0;
    padding: 2rem;

    @media (min-width: 768px){
        padding-left: 6rem;
    }

}   
}

</style>