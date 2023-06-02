<template>

    <!-- SOCIALS -->
    <div class="socials">
        <h3>Connect with us:</h3>
        <div class="social-icons">
            <img id="icon" src="../images/google-icon.png" height="30" width="30" >
            <img id="icon" src="../images/facebook-icon.png" height="30" width="30" >
            <img id="icon" src="../images/twitter-icon.png" height="30" width="30" >
            <img id="icon" src="../images/instagram-icon.png" height="30" width="30" >
        </div>
    </div>
        <!-- SOCIALS -->

        <!-- FOOTER -->
    <div class='footer-wrapper'>

        <!-- FIRST COLUMN -->
        <div class="col first">
            <h2>Tasty & Fresh</h2>
            <h3>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam odio ratione perferendis rerum doloremque blanditiis exercitationem! Optio molestiae eaque beatae? Eaque adipisci illo expedita ipsam.</h3>
            <h3>@Tasty and fresh Copyright 2023. All rights reserved</h3>
        </div>
        <!-- FIRST COLUMN -->

        <!-- SECOND COLUMN -->
        <div class="col second">
            <h2>Products</h2>
            <p>Pasta</p>
            <p>Sushi</p>
            <p>Burgers</p>
            <p>Rice</p>
        </div>
        <!-- SECOND COLUMN -->
        
        <!-- THIRD COLUMN -->
        <div class="col third">
            <h2>Useful Links</h2>
            <p>Your account</p>
            <p>Booking</p>
            <p>Ordering</p>
        </div>
        <!-- THIRD COLUMN -->

        <!-- FOURTH COLUMN -->
        <div class="col fourth">
            <h2>Find us</h2>
            <p>tasty@fresh.com</p>
            <p>Tasty St. 188, Abidjan, C.I.</p>
            <p>(+225) 25 52 25 52</p>
        </div>
        <!-- FOURTH COLUMN -->
    </div>
    <!-- FOOTER -->
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Imbue:wght@100;200;300;400;500;600;700;800;900&display=swap');

.socials {
    background-image: linear-gradient( 58.2deg,  rgba(40,91,212,0.73) -3%, rgba(171,53,163,0.45) 49.3%, rgba(255,204,112,0.37) 97.7% );
    font-family: 'Imbue', serif;
    display: flex;
    justify-content: space-around;
    font-size: 22px;
    width: 100%;
}

.social-icons {
    padding-top: 1.5%;
    padding-left: 5px;
}

#icon {
    padding-left: 100px;
}

.footer-wrapper {
    font-family: 'Imbue', serif;
    background-color: black;
    color: white;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

.col {
    display: flex;
    flex-direction: column;
}

.first {
    width: 25%;
}

.col > p {
    font-size: 1    8px;
}

</style>