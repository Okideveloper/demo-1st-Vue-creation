<template>
  <div class="hello">
    <h2>{{ name }}</h2>
    <h1>{{ msg }}</h1>
    <h3>Let's solve some Math!</h3>
    <p id="math">
      What is {{ num1 }} times {{ num2 }}?
      <span v-if="product">{{ product }}</span>
    </p>
    <button v-on:click="calculateProduct">Calculate</button>

    <h2>2 Things that are difficult in JavaScript</h2>

    <ol>
      <li>Naming things</li>
      <li>Recursion</li>
      <li>Off-by-ONE error</li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "hello",
  props: {
    msg: String
  },
  data() {
    return {
      name: "Amanda 'aka' Okideveloper",
      num1: 673,
      num2: 3,
      product: null
    };
  },
  methods: {
    calculateProduct: function() {
      this.product = this.num1 * this.num2;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
  padding-top: 20px;
}

h3 {
  padding-bottom: 25px;
}

#math {
  font-family: Georgia, Times, "Times New Roman", serif;
  font-size: 20px;
}

ol {
  list-style-type: upper-roman;
  width: 17%;
  margin: auto;
  font-weight: 500;
  line-height: 1.5;
}

li {
  display: list-item;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
