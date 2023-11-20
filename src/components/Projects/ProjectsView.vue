<script setup>
import { projects } from '../../project';
</script>

<template>

    <!-- ======= Portfolio Section ======= -->
    <section id="portfolio" class="portfolio section-bg">
      <div class="container" data-aos="fade-up">

        <div class="section-title">
          <h2>Portfolio</h2>
          <p></p>
        </div>

        <div class="row portfolio-container" data-aos="fade-up" data-aos-delay="200">

          <div class="col-lg-4 col-md-6 portfolio-item filter-app" v-for="project in projects" :key="project.id">
            <div class="portfolio-wrap">
              <img :src="project.image" class="img-fluid" alt="">
              <div class="portfolio-info">
                <h4>{{ project.name }}</h4>
                <p></p>
                <div class="portfolio-links">
                  <a :href="project.image" data-gallery="portfolioGallery" class="portfolio-lightbox" title="App 1"><i class="bx bx-plus"></i></a>
                  <a :href="project.link" class="portfolio-details-lightbox" data-glightbox="type: external" title="Portfolio Details"><i class="bx bx-link"></i></a>
                  
                  <router-link :to="'/project-details/' + project.id" class="portfolio-details-lightbox" data-glightbox="type: external" title="Portfolio Details"><i class="bx bx-info-circle"></i></router-link >
                </div>
              </div>
            </div>
          </div>

        </div>

      </div>
    </section><!-- End Portfolio Section -->
</template>