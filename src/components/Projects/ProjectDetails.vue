<script setup>
import {ref} from 'vue'
import { projects } from '../../project';
import { useRoute } from 'vue-router';

const route=useRoute();
const projectId=route.params.id;
const project=ref(projects.find((p) => p.id === Number(projectId)))
</script>

<template>
     <!-- ======= Portfolio Details Section ======= -->
     <section id="portfolio-details" class="portfolio-details">
      <div class="container">

        <div class="row gy-4">
          <div class="d-flex justify-content-end">
            <a href="/" class="btn btn-primary"><i class="bi bi-arrow-left"></i> Back</a>
          </div>
          <div class="col-lg-8">
            <div class="portfolio-details-slider swiper">
              <div class="swiper-wrapper align-items-center">

                <div class="swiper-slide">
                  <img :src="project.image2" alt="">
                </div>

                <div class="swiper-slide">
                  <img :src="project.image3" alt="">
                </div>

                

              </div>
              <div class="swiper-pagination"></div>
            </div>
          </div>

          <div class="col-lg-4">
            <div class="portfolio-info">
              <h3>Project information</h3>
              <ul>
                <li><strong>Name</strong>: {{ project.name }}</li>
                <li><strong>Category</strong>: {{ project.category }}</li>
                <li><strong>Client</strong>: {{ project.client}} </li>
                <li><strong>Project URL</strong>: <a href="#">{{ project.link }}</a></li>
              </ul>
            </div>
            <div class="portfolio-description">
              <h2>{{ project.name }}</h2>
              <p>
                {{ project.description }}
              </p>
            </div>
          </div>

        </div>

      </div>
    </section><!-- End Portfolio Details Section -->
</template>