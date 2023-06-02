<template>

<Navbar />

<!-- HEADER -->

<div class="header-wrapper">
  <div >
    <img src="@/images/header.jpg" class="header-image" >
  </div>
</div>

<!-- HEADER -->

<h1 id="our-food">OUR FOOD</h1>

<!-- ITEMS -->

<div class="items-wrapper">
  <div v-for="item in items" :key="item.id" class="all-items">
    <div class="card">
      <img class="item-img" :src="`http://localhost:1337${item.attributes.image.data.attributes.formats.thumbnail.url}`"/>
      <h1 class="item-name">{{ item.attributes.name }}</h1>
      <h3 class="item-price">{{ item.attributes.price }}€</h3>
      <h2 class="item-description">{{ item.attributes.description }}</h2>
    </div>
  </div>
</div>

<!-- ITEMS -->

<!-- FOOTER -->
<Footer />
<!-- FOOTER -->

</template>


<script>
import Navbar from "./components/Nav.vue"
import Footer from "./components/Footer.vue"


export default {
  components: {
    Navbar,
    Footer
  },

  data() {
    return {
      items: [],
      api_url: "http://localhost:1337",
    }
  },

  
methods: {
  async getItems() {
            try {
              fetch('http://localhost:1337/api/items?populate=*')
                .then(response => response.json())
                .then(data => {
                  const items = Object.values(data)[0];
                  for ( let i = 0; i < items.length; i++) {
                    this.items.push(items[i])
                  }
        
                  console.log(items)
                })
                .catch(error => {
                  console.error(error);
                });
        
            } catch (error) {
              console.error(error);
            }
            },
            
            emptyStore() {
              this.items = [];
            }
},

created() {
  this.getItems()
  console.log(this.items)
},
}



</script>

<style >

@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Imbue:wght@100;200;300;400;500;600;700;800;900&display=swap');


body {
  font-family: 'Dancing Script', cursive;
    margin: 0;
    padding: 0;
    max-width: 100%;
    overflow-x: hidden;
    background-image: linear-gradient( 111.4deg,  rgba(238,113,113,1) 1%, rgba(246,215,148,1) 58% );
}

#our-food {
  font-weight: 700;
  font-size: 36px;
  color: black;
  position: relative;
  left: 45%;
  margin-bottom: 5%;
  margin-top: 5%;
}

.header-image {
  max-width: 100%;
  height: auto;
}


.header-wrapper {
  margin-bottom: 1%;
}

.items-wrapper {
  width: 100%;
  display: flex;
  flex-basis: 10%;
  flex-wrap: wrap;
  justify-content: space-around;
}

.item-img {
  position: relative; 
  left: 25%;
  width: 100%;
  margin-top: 2.5%;
  border: 2px solid black;
  border-radius: 40px;
  height: 25%;
  width: 50%;
}

.all-items {

}

.card {
  z-index: -1;
  color: white;
  border: 5px solid black;
  border-radius: 40px;
  background: linear-gradient(to right, #fc4a1a, #f7b733);
  width: 25vw;
  margin-left: 1%;
  margin-bottom: 8%;
  display: flex;
  flex-direction: column;
  text-overflow: ellipsis;
  transition: 0.2s ease-in-out;
  
}



.card:hover {
  transform: scale(1.1);
  background-image: linear-gradient( 111.4deg,  rgba(238,113,113,1) 1%, rgba(246,215,148,1) 58% );
}

.item-name {
  position: relative;
  left: 0%;
}

.item-price {
  font-family: 'Imbue', serif;
  font-weight: 900;
  color: black;
  font-size: 22px;
}

.item-description {
  font-family: 'Imbue', serif;
  font-size: 26px;
}


</style>