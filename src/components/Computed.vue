<template>
  <div>
    <!-- 
      if(newProduct.price < 100) {
        document.write('You need to buy more)
      } else if (newProduct.quantity > 10) {
        document.write('You have crossed the limit!!)
      } else {
        document.write('Weldone!')
      }
     -->
    <div class="okay" v-if="newProduct.price < 100">
      <p>You neew to buy more</p>
    </div>
    <div class="error" v-else-if="newProduct.quantity > 10">
      <p>You have crossed the limit!!</p>
    </div>
    <div v-else>
      <p>Welldone!</p>
    </div>
    <form v-on:submit.prevent>
      <div class="form__item">
        <label for="name">Name</label>
        <input type="name" name="name" id="" v-model="newProduct.name">
      </div>
      <div class="form__item">
        <label for="price">Price</label>
        <input type="number" name="price" id="" v-model.number="newProduct.price">
      </div>
      <div class="form__item">
        <label for="quantity">Quantity</label>
        <input type="number" name="quantity" id="" v-model.number="newProduct.quantity">
      </div>
      <p>Subtotal: {{ subTotal }}</p>
      <button @click="submitForm" v-show="subTotalLess">Add to List</button>
    </form>
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Price</th>
          <th>Qanutity</th>
          <th>SubTotal</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(ore, index) in list" v-bind:key="index">
          <td>{{ ore.name }}</td>
          <td>{{ ore.price }}</td>
          <td>{{ ore.quantity }}</td>
          <td>{{ ore.price * ore.quantity }}</td>
        </tr>
      </tbody>
    </table>
    <h2>
      Total Price: {{ totalPrice }}
    </h2>
  </div>
</template>
<script>
  export default {
    name: 'ComputedComponent',
    data() {
      return {
        list: [
          {
            name: 'shoes',
            price: 20000,
            quantity: 1,
          },
          {
            name: 'shirts',
            price: 5000,
            quantity: 1,
          }
        ],
        newProduct: {
          name: '',
          price: 0,
          quantity: 1
        }
      }
    },
    methods: {
      submitForm() {
        this.list.push(this.newProduct)
        this.newProduct = {
          name: '',
          price: 0,
          quantity: 1,
        }
      }
    },
    computed: {
      totalPrice() {
        let total = 0;
        this.list.map(item => total = total + (item.price * item.quantity))
        return total;
      },
      subTotal() {
        return this.newProduct.price * this.newProduct.quantity
      },
      subTotalLess() {
        return this.subTotal > 500;
      }
    }
  }
</script>
<style scoped>
.error {
  color: red;
}
</style>