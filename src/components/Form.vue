<template>
  <div>
    <form @submit.prevent="submitForm" v-if="!formSubmitted">
      <span>Full Name</span><br>
      <input
          v-model="name"
          type="text"
          placeholder="Enter your name"
      /><br>
      <span>Email</span><br>
      <input
          v-model="email"
          type="email"
          placeholder="Enter your email"
      /><br>
      <span>Phone</span><br>
      <input
          v-model="phone"
          type="number"
          placeholder="Enter phone number"
      /><br>
      <span>Gender</span><br>
      <input
          type="radio"
          id="male-radio"
          v-model="gender"
          value="Male"
      />
      <label for="male-radio">Male</label>
      <input
          type="radio"
          id="female-radio"
          v-model="gender"
          value="Female"
      />
      <label for="female-radio">Female</label><br>
      <button
          class="btn btn-primary"
          type="submit"
          value="Submit"
      >Submit</button>
    </form>
    <div v-if="formSubmitted">
      <h3>Form Submitted</h3>
      <p>Name: {{ name }}</p>
      <p>Email: {{ email }}</p>
      <p>Phone: {{ phone }}</p>
      <p>Gender: {{ gender }}</p>
      <small>Click on run to launch the app again.</small>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      gender: "",
      phone: "",
      formSubmitted: false
    };
  },
  methods: {
    submitForm: function () {
      this.formSubmitted = true
    }
  },
};
</script>
<style>
form {
  padding: 10px;
  border: 2px solid black;
  border-radius: 5px;
}

input {
  padding: 4px 8px;
  margin: 4px;
}

span {
  font-size: 18px;
  margin: 4px;
  font-weight: 500;
}

.submit {
  font-size: 15px;
  color: #fff;
  background: #222;
  padding: 6px 12px;
  border: none;
  margin-top: 8px;
  cursor: pointer;
  border-radius: 5px;
}
h1 {
  color: #3d4852;
}
.btn {
  border: none;
  border-radius: 3px;
  margin: auto 0;
  padding: 0.5rem 0.75rem;
  flex-shrink: 0;
  cursor: pointer;
  font-size: 0.9rem;
  letter-spacing: 0.5px;
  transition: all 0.1s ease-in;
}
.btn-primary {
  background: #0073cf;
  color: #fff;
}
input {
  border-radius: 3px;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
  border: 1px solid #f1f5f8;
  color: #606f7b;
  padding: 0.5rem 0.75rem;
  box-sizing: border-box;
  font-size: 1rem;
  letter-spacing: 0.5px;
  margin: 0.5rem 0;
}


</style>