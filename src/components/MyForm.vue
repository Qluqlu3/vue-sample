<template>
  <div>
    <form @submit.prevent="onSubmit">
      <div>
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="name" />
      </div>
      <div>
        <label for="age">Age:</label>
        <input type="number" id="age" v-model.number="age" />
      </div>
      <div>
        <button type="submit">Submit</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      age: ""
    };
  },
  methods: {
    onSubmit() {
      alert(`Name: ${this.name}, Age: ${this.age}`);
    }
  }
};
</script>