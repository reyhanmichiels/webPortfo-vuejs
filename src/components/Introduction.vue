<script setup>
import { reactive } from "vue";

const card = reactive({
  title: "Hello again!",
  body: "My name is reyhan, i'm Technology Information student at Brawijaya University. I'm interested in becoming a backend developer.  Now I have experience with php and laravel, and am learning the GO language. In the future I'm interested in learning about springboot, docker, and a little bit about devops",
  button: "See portfolio",
});
</script>

<template>
  <div
    id="introduction"
    class="w-screen h-screen flex justify-center items-center"
  >
    <div class="w-1/2 h-1/2">
      <div class="card lg:card-side bg-base-100 shadow-xl">
        <figure>
          <img src="../assets/profile.jpeg" alt="Album" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">{{ card.title }}</h2>
          <p>{{ card.body }}</p>
          <div class="card-actions justify-end">
            <a href="#portfolio">
              <button class="btn btn-primary">{{ card.button }}</button>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
