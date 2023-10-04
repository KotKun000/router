<template>
    <div id="app-container">
      <button @click="showForm">จองโต๊ะ</button>
      <div class="popup" v-if="isFormVisible">
        <div class="popup-content">
          <form @submit.prevent="submitForm">
            <label>จองโต๊ะ</label>
            <label for="name">ชื่อ:</label>
            <input type="text" id="name" v-model="formData.name" required>
  
            <label for="email">อีเมล:</label>
            <input type="email" id="email" v-model="formData.email" required>
  
            <label for="tel">เบอร์ติดต่อ:</label>
            <input type="text" id="tel" v-model="formData.tel" required>
  
            <label for="date">วันที่:</label>
            <input type="date" id="date" v-model="formData.date" required>
  
            <label for="time">เวลา:</label>
            <input type="time" id="time" v-model="formData.time" required>
  
            <label for="table">จำนวนโต๊ะ:</label>
            <input type="number" min="1" id="table" v-model="formData.table" required>
  
            <button type="submit">ยืนยัน</button>
            <button class="buttonc" @click="hideForm">ยกเลิก</button>
          </form>
        </div>
      </div>
    </div>
  
    <div>
      <table v-if="bookings.length > 0" style="margin-left: 30%;">
        <thead>
          <tr>
            <th scope="col">ชื่อ: </th>
            <th scope="col">อีเมล: </th>
            <th scope="col">เบอร์ติดต่อ: </th>
            <th scope="col">วันที่: </th>
            <th scope="col">เวลา: </th>
            <th scope="col">จำนวนโต๊ะ: </th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(booking, index) in bookings" :key="index">
            <td scope="row">&ensp;{{ booking.name }}&ensp;</td>
            <td scope="row">{{ booking.email }}&ensp;</td>
            <td scope="row">{{ booking.tel }}&ensp;</td>
            <td scope="row">{{ booking.date }}&ensp;</td>
            <td scope="row">{{ booking.time }}&ensp;</td>
            <td scope="row">{{ booking.table }}&ensp;</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const isFormVisible = ref(false);
  const formData = ref({
    name: '',
    email: '',
    tel: '',
    date: '',
    time: '',
    table: '',
  });
  
  const bookings = ref([]);
  
  const showForm = () => {
    formData.value = {
      name: '',
      email: '',
      tel: '',
      date: '',
      time: '',
      table: '',
    };
    isFormVisible.value = true;
  };
  
  const hideForm = () => {
    isFormVisible.value = false;
  };
  
  const submitForm = () => {
    const bookingData = {
      name: formData.value.name,
      email: formData.value.email,
      tel: formData.value.tel,
      date: formData.value.date,
      time: formData.value.time,
      table: formData.value.table,
    };
    bookings.value.push(bookingData);
    hideForm();
  };
  </script>
  
  <style scoped>
  .popup {
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .popup-content {
    background-color: white;
    padding: 20px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    border-radius: 5px;
    text-align: center;
  }
  
  form {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  
  label {
    font-weight: bold;
  }
  
  input {
    padding: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  button {
    padding: 5px 15px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .buttonc {
    padding: 5px 15px;
    background-color: #d50202;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  table, th, td {
    border: 1px solid #ccc;
  }
  
  th, td {
    padding: 10px;
    text-align: left;
  }
  
  a {
    text-decoration: none;
    color: #007bff;
    cursor: pointer;
  }
  
  a:hover {
    text-decoration: underline;
  }
  
  .buttonc:hover {
    background-color: #ff0000;
  }
  </style>
  