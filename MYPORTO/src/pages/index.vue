<template>
    <navbar :socialLight=true />
    <!-- Start Hero -->
    <section class="relative pt-28 personal-wrapper overflow-hidden bg-amber-500/5" id="home" >
        <div class="absolute inset-0" id="overlay"></div>
        <div class="container">
            <div class="grid md:grid-cols-2 grid-cols-1 items-center gap-[30px]">
                <div>
                    <h4 class="font-bold lg:text-[32px] text-3xl lg:leading-normal leading-normal mb-4">Hey! I'm
                        <br>
                        <vue-typewriter-effect class="typewrite relative text-type-element  text-amber-500"
                            data-period="4000"
                            :strings='["Muhamad Ariel Dwi Prayoga", "Data Analyst", "Data Scientist", "Data Engineer", "ML Engineer"]' /><span
                            class="wrap"></span>
                    </h4>
                    <p class="text-slate-400 max-w-xl">Obviously I'm a Data Enthusiast. 
                    Experienced in Analytics, Engineering, Science, and Machine Learning.</p>

                <div class="mt-6 flex space-x-4">
                    <a href="https://drive.google.com/file/d/174FBOs3EBAT65KGwQqHy0cFgGSA6QLzo/view?usp=sharing"
                        target="_blank"
                        class="btn bg-amber-500/10 hover:bg-amber-500 border-amber-500/10 
                            hover:border-amber-500 text-amber-500 hover:text-white 
                            rounded-md">
                        CV
                    </a>

                    <a href="https://github.com/username" 
                        target="_blank"
                        class="btn bg-amber-500/10 hover:bg-amber-500 border-amber-500/10 
                            hover:border-amber-500 text-amber-500 hover:text-white 
                            rounded-md">
                        Github
                    </a>
                </div>

                </div>

                <div class="relative">
                    <img src="../assets/images/hero/2.svg" alt="">

                    <div
                        class="absolute lg:bottom-20 md:bottom-10 bottom-2 ltr:md:-left-5 ltr:left-2 rtl:md:-right-5 rtl:right-2 p-4 rounded-lg shadow-md dark:shadow-gray-800 bg-white dark:bg-slate-900 m-3 w-44 text-center">
                        <span class="text-3xl font-medium mb-0 flex justify-center"><count-up
                                class="counter-value font-bold" :start-val="1" :end-val="4"></count-up>+</span>
                        <h6 class="text-sm text-slate-400 mt-1">Project Completed</h6>
                    </div>

                    <div
                        class="absolute lg:top-80 md:top-56 top-48 ltr:md:-right-0 ltr:right-2 rtl:md:-left-0 rtl:left-2 p-4 rounded-lg shadow-md dark:shadow-gray-800 bg-white dark:bg-slate-900 m-3 w-44 text-center">
                        <h6 class="font-semibold">Data Enthusiast</h6>
                        <h6 class="text-sm text-slate-400 mt-1">1+ Years Experience</h6>
                    </div>
                </div>
            </div>
        </div><!--end container-->
    </section><!--end section-->
    <div class="relative">
        <div class="absolute block w-full h-auto bottom-[25px] z-1 left-0">
            <a href="#about"><i
                    class="mdi mdi-arrow-down absolute top-0 left-0 right-0 text-center inline-flex items-center justify-center rounded-full bg-white dark:bg-slate-900 h-12 w-12 mx-auto shadow-md dark:shadow-gray-800"></i></a>
        </div>
    </div>
    <!-- End Hero -->
    <about />
    <services />
    <experience />
    <education />
    <projects />
    <clients />
    <blog />
    <getintouch />
</template>

<script>
import navbar from '@/components/navbar/navbar.vue'
import VueTypewriterEffect from "vue-typewriter-effect";
import CountUp from 'vue-countup-v3';
import about from '@/components/about/about.vue';
import services from '@/components/services/services.vue';
import experience from '@/components/experience/experience.vue';
import education from '@/components/education/education.vue';
import projects from '@/components/project/projects.vue';
// import clients from '@/components/client/clients.vue';
// import blog from '@/components/blog/blog.vue';
import getintouch from '@/components/getInTouch/getInTouch.vue';

export default {
    name: 'indexOne',
    data() {
       
    },
    components: {
        navbar,
        VueTypewriterEffect,
        CountUp,
        about,
        services,
        experience,
        education,
        projects,
        getintouch,
    }
}
</script>

<style lang="scss" scoped></style>