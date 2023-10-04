<template>
  <div class="home-container">
    <div class="cafe-list">
      <div class="cafe" v-for="cafe in cafes" :key="cafe.id">
        <img :src="cafe.image" alt="Cafe Image" class="cafe-image" />
        <h2 class="cafe-name">{{ cafe.name }}</h2>
        <p class="cafe-description">{{ cafe.description }}</p>
        <Button :cafe="cafe" @bookTable="bookTable" />
      </div>
    </div>
  </div>
</template>

<script>
import Button from '@/components/Button.vue';

export default {
  components: {
    Button,
  },
  data() {
    return {
      cafes: [
        {
          id: 1,
          name: 'aday in chiang mai coffee brew',
          description: 'ทุกวัน 9:00-17:00 น.',
          image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/9h6mhqdj4p7f.jpg',
        },
        {
          id: 2,
          name: 'YEllOO',
          description: 'ทุกวัน 8:00-19:00 น.',
          image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/dlw2awazbkkr.jpg',
        },
        {
          id: 3,
          name: 'EVERGREEN',
          description: 'ทุกวัน 8:00-17:00 น.',
          image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/0wq31ij3a2u8.jpg',
        },
        {
          id: 4,
          name: 'Undostudio',
          description: '8:30-17:00 น. (ปิดวันอังคาร)',
          image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/yvp5j6hkerng.jpg',
        },
        {
          id: 5,
          name: 'Karoon • กรุณ',
          description: '9:00-17:00 น. (ปิดวันจันทร์)',
          image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/aogkfqrgigsf.jpg',
        },
        {
          id: 6,
          name: 'Bar Cha - Matcha and Bakery バーチャ ',
          description: 'ทุกวัน 8:00-18:00 น.',
          image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/w3uh9bdry6hz.jpg',
        },
      ],
    };
  },
  methods: {
    bookTable(cafe) {
      console.log(`จองโต๊ะในร้าน: ${cafe.name}`);
    },
  },
};
</script>

<style scoped>
.home-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}

.cafe-list {
  display: grid;
  grid-template-columns: auto auto auto;
  gap: 20px;
}

.cafe {
  width: 300px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  text-align: center;
  background-color: white;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.cafe-image {
  max-width: 100%;
  border-radius: 10px;
  margin-bottom: 10px;
}

.cafe-name {
  font-size: 20px;
  font-weight: bold;
  margin: 0;
}

.cafe-description {
  font-size: 16px;
  margin: 10px 0;
}

.button-container {
  display: flex;
  justify-content: center;
  margin-top: 10px;
}

</style>
