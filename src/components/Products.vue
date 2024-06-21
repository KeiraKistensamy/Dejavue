<template>
  <div class="container">
    <div class="row">
    <Card v-for="product in products" :key="product.id">
        <template #cardHeader>
          <img class="img-fluid" :src="product.productProfile" :alt="product.productName" loading="lazy"/>
        </template>
        <template #cardBody>
          <p>{{product.productName}}</p>
          <p>{{product.productDescription}}</p>
          <p>{{product.productPrice}}</p>
          <p>{{product.productStatus}}</p>
        </template>
          </Card>
          </div>
    </div>
</template>


<script>
import Card from "./Card.vue";

export default {
  name: "ProductComp",
  components: {
    Card,
  },
  data() {
    return {
      products: [
        {
         id: 1,
          productName: "Garnier Pure Active Intensive",
          productDescription: "Garnier Pure Active 3in1 Anti Blackhead Charcoal can be used as a face wash, blackhead scrub and charcoal face mask to visibly reduce the appearance of blackheads, and help to protect against their reappearance. (150ml)",
          productPrice: 124.00,
          productStatus: "Available",
          productProfile: "https://keirakistensamy.github.io/allimages/images/KeiraKistensamy.png",
          },
        {
            id: 2,
          productName: "Garnier Micellar Cleanser",
          productDescription: "Garnier Micellar Cleansing Water 100 ml will quickly become an essential in your daily skincare routine because of its convenience and efficacy. This all-in-one cleanser lifts dirt from the skin, while nourishing it, in a simple wiping motion without the need for rinsing after.",
          productPrice: 59.99,
          productStatus: "Sold Out",
          productProfile: "https://keirakistensamy.github.io/allimages/images/KeiraKistensamy.png",
          },
        {
            id: 3,
          productName: "Garnier Skin Naturals Instant Radiance Scrub.(100ml)",
          productDescription: "Garnier Skin Naturals Instant Radiance Scrub 100ml removes dead cells to reveal your skin's radiance from the first wash. An ultra-foaming texture enriched with pure lemon essence, smoothes and evens your skin while micro-beads gently remove impurities and exfoliate dead skin cells.",
          productPrice: 79.99,
          productStatus: "Sold Out",
          productProfile: "https://keirakistensamy.github.io/allimages/images/KeiraKistensamy.png",
          },
        {
            id: 4,
          productName: "Garnier Pure Active Ideal Complexion Daily Cream.(40ml)",
          productDescription: "Garnier Skin Naturals Even Matte Daily Cream 40ml uses specially selected ingredients to visibly even out skin tone over time and reduce oil and shine for a beautifully matte complexion. Made with lemon essence and contains UV filters.",
          productPrice: 90.99,
          productStatus: "Available",
          productProfile: "https://keirakistensamy.github.io/allimages/images/KeiraKistensamy.png",
          },

      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
