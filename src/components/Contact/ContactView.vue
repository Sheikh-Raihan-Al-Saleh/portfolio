<script setup>
import { aboutData } from '../../about.js';
</script>

<template>
    <!-- ======= Contact Section ======= -->
    <section id="contact" class="contact">
        <div class="container" data-aos="fade-up">
            <div class="section-title">
                <h2>Contact</h2>
            </div>

            <div class="row col-md-12"> 
                <div class="col-md-4">
                    <div class="address">
                        <i class="bi bi-geo-alt"></i>
                        <h4>Location:</h4>
                        <p>{{ aboutData.location }}</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="email">
                        <i class="bi bi-envelope"></i>
                        <h4>Email:</h4>
                        <p>{{ aboutData.email }}</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="phone">
                        <i class="bi bi-phone"></i>
                        <h4>Call:</h4>
                        <p>{{ aboutData.phone }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section><!-- End Contact Section -->
</template>