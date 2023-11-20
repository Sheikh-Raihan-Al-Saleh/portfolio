<script setup>
    import { skills } from '../../skill';
</script>

<template>
  <!-- ======= Skills Section ======= -->
  <section id="skills" class="skills section-bg">
    <div class="container" data-aos="fade-up">
      <div class="section-title">
        <h2>Skills</h2>
        <p></p>
      </div>

      <div class="row skills-content">
        <div class="col-lg-6" v-for="(skill, index) in skills" :key="index.id">
          <div class="progress">
            <span class="skill">
              <i class="num mx-2">{{ index + 1 }}</i> {{ skill.name }} <i class="val">{{ skill.level }}%</i>
            </span>
            <div class="progress-bar-wrap">
              <div
                class="progress-bar"
                role="progressbar"
                :style="{ width: skill.level + '%' }"
                :aria-valuenow="skill.level"
                aria-valuemin="0"
                aria-valuemax="100"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section><!-- End Skills Section -->
  
</template>



<style scoped>
.progress-bar {
  height: 10px;
  background-color: rgb(1, 152, 16);
  color: white;
  text-align: center;
  line-height: 20px;
}
</style>
