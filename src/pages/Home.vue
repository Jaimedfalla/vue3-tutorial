<script setup>
    import courses from '../courses';
    import CourseSummary from '../components/CourseSummary.vue';
</script>

<template>
    <div class="Home page">
        <header>
            <h1>Vue Online Course Site</h1>
        </header>
        <course-summary 
            v-for="course in courses"
            :key="course.id"
            :course="course">
        </course-summary>
    </div>
</template>