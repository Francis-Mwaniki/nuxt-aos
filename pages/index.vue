<template>
    <div>


    <div>
    <!-- text-4xl bg-gradient-to-r from-green-300 via-blue-500 to-purple-600 bg-clip-text font-extrabold text-transparent tracking-tight sm:text-6xl -->
    <div class="bg-gray-900 text-white py-20 text-center">
      <h1 class="text-4xl bg-gradient-to-r from-green-300 via-blue-500 to-purple-600 bg-clip-text font-extrabold text-transparent tracking-tight sm:text-6xl uppercase" data-aos="zoom-out-up">Welcome to Our Website!</h1>
      <p class="text-lg mb-8" data-aos="zoom-out-up">Discover amazing things here.</p>
      <img src="https://images.pexels.com/photos/11001424/pexels-photo-11001424.jpeg" alt="Hero Image" class="mx-auto rounded-full w-48 h-48 object-cover shadow-lg mb-8" />
      <a href="#" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Get Started</a>
    </div>

    <!-- Card Section -->
    <div class="container mx-auto mt-12 flex flex-wrap justify-center">
      <div v-for="(card, index) in cardItems" :key="index" class="bg-white rounded-lg shadow-lg p-6 m-4 w-64" data-aos="zoom-out-up">
        <img :src="card.imageUrl" :alt="'Card Image ' + index" class="w-full h-32 object-cover mb-4" />
        <h2 class="text-xl font-bold mb-2">{{ card.title }}</h2>
        <p>{{ card.description }}</p>
      </div>
    </div>
    <div class="bg-gray-900 text-white py-20 text-center" data-aos="zoom-out-up">
      <h1 class="text-4xl font-bold mb-4" data-aos="zoom-out-up">Welcome to Our Website!</h1>
      <p class="text-lg mb-8" data-aos="zoom-out-up">Discover amazing things here.</p>
      <img src="https://images.pexels.com/photos/11001424/pexels-photo-11001424.jpeg" alt="Hero Image" class="mx-auto rounded-full w-48 h-48 object-cover shadow-lg mb-8" />
      <a href="#" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Get Started</a>
    </div>
  </div>
    </div>
</template>

<script >
import AOS from 'aos';
import 'aos/dist/aos.css'; 

export default {
  data() {
    return {
      cardItems: [
        {
          title: 'Card 1',
          description: 'Description for Card 1',
          imageUrl: 'https://images.pexels.com/photos/18254694/pexels-photo-18254694/free-photo-of-man-with-suitcase-in-front-of-modern-building-in-baku-in-black-and-white.jpeg'
        },
        {
          title: 'Card 2',
          description: 'Description for Card 2',
          imageUrl: 'https://images.pexels.com/photos/11001424/pexels-photo-11001424.jpeg'
        },
        {
          title: 'Card 3',
          description: 'Description for Card 3',
          imageUrl: 'https://images.pexels.com/photos/18357062/pexels-photo-18357062/free-photo-of-halves-of-figs.jpeg'
        },
        {
          title: 'Card 4',
          description: 'Description for Card 1',
          imageUrl: 'https://images.pexels.com/photos/18254694/pexels-photo-18254694/free-photo-of-man-with-suitcase-in-front-of-modern-building-in-baku-in-black-and-white.jpeg'
        },
        {
          title: 'Card 5',
          description: 'Description for Card 2',
          imageUrl: 'https://images.pexels.com/photos/11001424/pexels-photo-11001424.jpeg'
        },
        {
          title: 'Card 6',
          description: 'Description for Card 3',
          imageUrl: 'https://images.pexels.com/photos/18357062/pexels-photo-18357062/free-photo-of-halves-of-figs.jpeg'
        }
      ]
    };
  },
  beforeMount() {
    created: {
      AOS.init();
    }
  },
};

</script>

<style scoped>

</style>