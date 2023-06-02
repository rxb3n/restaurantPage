<template>
    <!-- NAVBAR -->
    <div class="nav-wrapper">
        <!-- NAV LOGO -->
        <div class="nav-img">
            <img src="@/images/logo.jpg" alt="" height="75" width="250">
        </div>
         <!-- NAV LOGO -->

         <!-- NAV ITEMS -->
        <div class="nav-elements">
            <p>FOOD</p>
            <p>SUSHI</p>
            <p>CUISINE STUBS</p>
            <p>SKEWERS</p>
            <p>MORE</p>
        </div>
         <!-- NAV ITEMS -->

         <div class="separator"></div>

         <!-- NAV ICONS -->
         <div class="nav-icons">
            <img src="@/images/search-icon.png" height="35" width="35">
            <img src="@/images/person-icon.png" height="35" width="35">
            <img src="@/images/cart-icon.png" height="35" width="35">
         </div>
          <!-- NAV ICONS -->
    </div>
    <!-- NAVBAR -->
</template>

<style>

@import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');

.nav-wrapper {
    font-family: 'Anton', sans-serif;
    font-size: 22px;
    z-index: 999;
    position: sticky;
    top: 0;
    padding-left: 15%;
    width: 100%;
    color: white;
    background-color: black;
    display: flex;
    flex-direction: row;
}

.nav-elements {
    position: relative;
    padding-top: 0.5%;
    padding-left: 2%;
    width: 50%;
    display: flex;
    justify-content: space-around;
}

.nav-icons {
    position: relative;
    padding-top: 0.8%;
    display: flex;
    filter: invert();
    flex-direction: row;
    justify-content: space-around;
    padding-left: 5%;
    width: 10%;
}

.separator {
    border: 1px solid #212424
}



</style>
