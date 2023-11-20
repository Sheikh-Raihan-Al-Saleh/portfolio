<script setup>
import { ref, computed } from 'vue'; 

import { aboutData } from '../../about.js';

const currentDate = ref(new Date());

//Calculate Age by given birthdate. 
const calculatedAge = computed(() => {
  const birthDate = new Date(aboutData.birthdate);
  const timeDiff = Math.abs(currentDate.value.getTime() - birthDate.getTime());
  return Math.floor(timeDiff / (1000 * 3600 * 24 * 365.25));
});
</script>

<template>
     <!-- ======= About Section ======= -->
     <section id="about" class="about">
      <div class="container" data-aos="fade-up">

        <div class="section-title">
          <h2>About</h2>
          <p></p>
        </div>

        <div class="row">
          <div class="col-lg-4">
            <img :src="aboutData.profile" class="img-fluid" alt="">
          </div>
          <div class="col-lg-8 pt-4 pt-lg-0 content">
            <h3>{{ aboutData.designation }}</h3>
            <p class="fst-italic">
            </p>
            <div class="row">
              <div class="col-lg-6">
                <ul>
                  <li><i class="bi bi-chevron-right"></i> <strong>Name:</strong> <span>{{ aboutData.name }}</span></li>
                  <li><i class="bi bi-chevron-right"></i> <strong>Birthday:</strong> <span>{{ aboutData.birthdate }}</span></li>
                  <li><i class="bi bi-chevron-right"></i> <strong>Phone:</strong> <span>{{ aboutData.phone }}</span></li>
                  <li><i class="bi bi-chevron-right"></i> <strong>City:</strong> <span>{{ aboutData.city }}</span></li>
                </ul>
              </div>
              <div class="col-lg-6">
                <ul>
                  <li><i class="bi bi-chevron-right"></i> <strong>Age:</strong> <span>{{ calculatedAge }}</span></li>
                  <li><i class="bi bi-chevron-right"></i> <strong>Degree:</strong> <span></span>{{ aboutData.degree }}</li>
                  <li><i class="bi bi-chevron-right"></i> <strong>Email:</strong> <span>{{ aboutData.email }}</span></li>
                  
                </ul>
              </div>
            </div>
            <p>
              {{ aboutData.details }}
            </p>
          </div>
        </div>

      </div>
    </section><!-- End About Section -->
</template>