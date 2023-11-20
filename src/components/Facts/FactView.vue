<script setup>
import { facts } from '../../facts';
</script>

<template>
   
    <!-- ======= Facts Section ======= -->
    <section id="facts" class="facts">
      <div class="container" data-aos="fade-up">

        <div class="section-title">
          <h2>Facts</h2>
          <p></p>
        </div>

        <div class="row">

          <div class="col-lg-3 col-md-6" v-for="(fact,index) in facts" :key="index.id">
            <div class="count-box">
              <i :class="fact.icon"></i>
              <span>{{ fact.count }}</span>
              <p>{{ fact.title }}</p>
            </div>
          </div>

        </div>

      </div>
    </section><!-- End Facts Section -->
</template>