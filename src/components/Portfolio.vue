<script setup>
import { ref } from "vue";

const portfolio = ref([
  {
    id: "slide1",
    next: "#slide2",
    prev: "#slide2",
    title: "ScholarWithUs",
    body: "ScholarWithUs is an application that provides information and preparation for taking scholarships to study abroad",
    link: "https://github.com/reyhanmichiels/ScholarWithUs",
  },
  {
    id: "slide2",
    next: "#slide1",
    prev: "#slide1",
    title: "SI-OBE",
    body: "si-OBE is a web-based application for the management of student grades based on the OBE (Outcome Based Education) system.",
    link: "https://github.com/andrisan/si-obe",
  },
]);
</script>

<template>
  <div
    id="portfolio"
    class="w-screen h-screen flex justify-center items-center"
  >
    <div class="h-1/4 w-1/3">
      <div class="carousel w-full">
        <div
          v-for="port in portfolio"
          :key="port.id"
          :id="port.id"
          class="carousel-item relative w-full flex justify-center items-center"
        >
          <div class="card w-96 bg-base-100 shadow-xl">
            <div class="card-body">
              <h2 class="card-title">{{ port.title }}</h2>
              <p>{{ port.body }}</p>
              <div class="card-actions justify-end">
                <a :href="port.link">
                  <button class="btn btn-primary">Github</button>
                </a>
              </div>
            </div>
          </div>
          <div
            class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
          >
            <a :href="port.next" class="btn btn-circle">❮</a>
            <a :href="port.prev" class="btn btn-circle">❯</a>
          </div>
        </div>

        <!-- <div
          id="slide2"
          class="carousel-item relative w-full flex justify-center items-center"
        >
          <div class="card w-96 bg-base-100 shadow-xl">
            <div class="card-body">
              <h2 class="card-title">Card title!</h2>
              <p>If a dog chews shoes whose shoes does he choose?</p>
              <div class="card-actions justify-end">
                <button class="btn btn-primary">Buy Now</button>
              </div>
            </div>
          </div>
          <div
            class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
          >
            <a href="#slide1" class="btn btn-circle">❮</a>
            <a href="#slide1" class="btn btn-circle">❯</a>
          </div>
        </div> -->
      </div>
    </div>
  </div>
</template>
