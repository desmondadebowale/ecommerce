<template>
  <div id="app" class="container-fluid">
      <Header />
      


    <div class="row">
      <div class="col-md-4">
        <Category v-for="category in categories" :listcategory = "category" :key="category.id"/>
        
      </div>

      <div class="col-md-8">
        <productslider/>
        <div class="row row-cols-1 row-cols-md-3">
          
        <Products v-for="cardproduct in productdisplay" :listproducts = "cardproduct" :key="cardproduct.id"/>
      </div>
        </div>
      </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Products from './components/Products'
import Category from './components/Category'
import productslider from './components/productslider'

export default {
  name: 'App',
  components: {
    Header,
    Products,
    Category,
    productslider
  },
  data(){
    return {
      categories: [{
        id: 1,
        name: "Laptops"
      },
      {
        id: 2,
        name: "Computing"
      },
      {
        id: 3,
        name: "Fashion"
      },
      {
        id: 4,
        name: "Electronics"
      }
      ],
      productdisplay: [{
        id: 1,
        name: "Watch",
        categoryid: 4,
        image: require('@/assets/productimage/watch.jpg'),
        price: 200000
      },
      {
        id: 2,
        name: "Shoe",
        categoryid: 3,
        image: require('@/assets/productimage/shoe.jpg'),
        price: 10000
      },
      {
        id: 3,
        name: "furniture",
        categoryid: 3,
        image: require('@/assets/productimage/office-furniture.jpg'),
        price: 3000000
      },
      {
        id: 4,
        name: "Computing",
        categoryid: 2,
        image: require('@/assets/productimage/alienware-laptop.jpg'),
        price:500000
      }
      ]
    }
  }
}
</script>
