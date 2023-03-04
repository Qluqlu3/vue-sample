<template>
  <div class="flex flex-col w-full h-[300px] justify-center items-center bg-gray-200">
    <form @submit.prevent="onSubmit">
      <div class="p-4 flex flex-row">
        <label class="w-[70px]" for="name">Name:</label>
        <input type="text" id="name" v-model="name" class="rounded" />
      </div>
      <div class="p-4 flex flex-row justify-center">
        <label class="w-[70px]" for="age">Age:</label>
        <input type="number" id="age" v-model.number="age" class="rounded" />
      </div>
      <div>
        <button type="submit" class="p-3 flex justify-center hover:bg-blue-100 items-center mt-5 rounded-lg cursor-pointer bg-blue-200 ml-auto w-[200px]">Submit</button>
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

<style lang="css">
  @import "@/assets/main.css";
</style>
