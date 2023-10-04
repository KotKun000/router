<template>
    <div class="review-container">
      <div class="cafe-list">
        <div class="cafe" v-for="cafe in cafes" :key="cafe.id">
          <img :src="cafe.image" alt="Cafe Image" class="cafe-image" />
          <h2 class="cafe-name">{{ cafe.name }}</h2>
          <div class="reviews">
            <div class="review" v-for="(review, index) in cafe.reviews" :key="index">
              <div class="rating-image">{{ review.ratingImage }}</div>
              <div class="review-text">{{ review.text }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        cafes: [
          {
            id: 1,
            name: 'aday in chiang mai coffee brew',
            image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/9h6mhqdj4p7f.jpg',
            reviews: [
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 1' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 2' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 3' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 4' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 5' },
            ],
          },
          {
            id: 2,
            name: 'YEllOO',
            image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/dlw2awazbkkr.jpg',
            reviews: [
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 1' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 2' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 3' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 4' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 5' },
            ],
          },
          {
            id: 3,
            name: 'EVERGREEN',
            image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/0wq31ij3a2u8.jpg',
            reviews: [
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 1' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 2' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 3' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 4' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 5' },
            ],
          },
          {
            id: 4,
            name: 'Undostudio',
            image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/yvp5j6hkerng.jpg',
            reviews: [
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 1' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 2' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 3' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 4' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 5' },
            ],
          },
          {
            id: 5,
            name: 'Karoon • กรุณ',
            image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/aogkfqrgigsf.jpg',
            reviews: [
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 1' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 2' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 3' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 4' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 5' },
            ],
          },
          {
            id: 6,
            name: 'Bar Cha - Matcha and Bakery バーチャ ',
            image: 'https://img.salehere.co.th/p/1200x0/2022/11/21/w3uh9bdry6hz.jpg',
            reviews: [
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 1' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 2' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 3' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 4' },
              { ratingImage: '⭐⭐⭐⭐⭐', text: 'ความคิดเห็นที่ 5' },
            ],
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .review-container {
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
  
  .reviews {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 10px;
  }
  
  .review {
    display: flex;
    align-items: center;
    margin: 5px 0;
  }
  
  .rating-image {
    font-size: 24px;
    margin-right: 5px;
  }
  
  .review-text {
    font-size: 16px;
  }
  </style>
  