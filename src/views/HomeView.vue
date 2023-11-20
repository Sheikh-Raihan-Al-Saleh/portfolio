<script setup>
import LayoutView from '../components/LayoutView.vue';
import AboutView from '../components/About/AboutView.vue';
import FactView from '../components/Facts/FactView.vue';
import ProjectsView from '../components/Projects/ProjectsView.vue';
import ContactView from '../components/Contact/ContactView.vue';
import SkillsView from '../components/Skills/SkillsView.vue';



</script>

<template>
  <LayoutView>
    <AboutView></AboutView>
    <SkillsView></SkillsView>
    <FactView></FactView>
    <ProjectsView></ProjectsView>
    <ContactView></ContactView>
  </LayoutView>

</template>
