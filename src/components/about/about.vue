<template>
    <!-- Start -->
    <section class="relative md:py-24 py-16" id="about">
        <div class="container">
            <div class="grid lg:grid-cols-12 md:grid-cols-2 grid-cols-1 items-center gap-[30px]">
                <div class="lg:col-span-5 lg:px-8">
                    <div class="relative">
                        <div
                            class="absolute inset-0 border dark:border-gray-800 rounded-full -mt-[10px] -ms-3 h-[100%] w-[100%] -z-1">
                        </div>
                        <img src="../../assets/images/ab2.png"
                            class="rounded-full shadow-md shadow-gray-200 dark:shadow-gray-800" alt="">

                        <!-- ✅ Bagian ini diperbaiki -->
                        <div
                            class="absolute lg:bottom-20 md:bottom-10 bottom-6 ltr:lg:-right-16 rtl:lg:-left-16 ltr:md:-right-8 rtl:md:-left-8 ltr:right-0 rtl:left-0 p-4 rounded-lg shadow-md dark:shadow-gray-800 bg-white dark:bg-slate-900 m-3 w-44 text-center">
                            <h6 class="font-semibold">Data Enthusiast</h6>
                            <span class="text-2xl font-medium text-amber-500 mb-0 flex justify-center">
                                <count-up 
                                    class="counter-value font-bold" 
                                    :start-val="0"
                                    :end-val="1">
                                </count-up>
                                + <span class="text-sm text-slate-400 mt-3 ml-1">Years</span>
                            </span>
                            <span class="text-sm text-slate-400">Experience</span>
                        </div>
                        <!-- ✅ End perbaikan -->
                    </div>
                </div><!--end col-->

                <div class="lg:col-span-7">
                    <div class="lg:ms-5">
                        <h3
                            class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">
                            I'm a Passionate Data Enthusiast</h3>

                        <p class="text-slate-400 max-w-xl text-[15px] text-justify">I am a fresh graduate in
                            Informatics with expertise in Data Analytics, Data Science, 
                            and Machine Learning, skilled in Python, R, SQL, Tableau, Power BI, and Excel. 
                            I have experience as an ICT Infrastructure Research Analyst at the Ministry of Defense and Investment Data & Research Analyst 
                            at the Indonesia Stock Exchange Investment Gallery, delivering data-driven insights and impactful solutions. 
                            With strengths in data engineering, problem-solving, and cross-functional collaboration, I am eager to grow as a Data Analyst, 
                            Data Scientist, Data Engineer, or Machine Learning Engineer.</p>
                        <p class="text-slate-400 max-w-xl text-[15px] mt-6"></p>

                        <div class="mt-6">
                            <a href="#project"
                                class="btn bg-amber-500/10 hover:bg-amber-500 border-amber-500/10 hover:border-amber-500 text-amber-500 hover:text-white rounded-md me-2 mt-2">See
                                Work</a>
                        </div>
                    </div>
                </div><!--end grid-->
            </div><!--end grid-->
        </div><!--end container-->

        <!-- My Skills -->
        <div class="container md:mt-24 mt-16">
            <div class="grid grid-cols-1 pb-8 text-center">
                <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">Programming Languages & Software Skills</h3>
                <p class="text-slate-400 max-w-xl mx-auto text-[15px]">
                    Proficient in essential programming languages and data tools, enabling efficient data analysis, visualization, and machine learning implementation.
                </p>
            </div><!--end grid-->

            <div class="grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 mt-8 gap-[30px]">
                <div v-for="item in hobbies" :key="item.name"
                    class="flex group shadow shadow-gray-200 dark:shadow-gray-800 dark:hover:shadow-gray-700 items-center p-3 rounded-lg bg-white dark:bg-slate-900">
                    <div
                        class="flex items-center justify-center h-[45px] min-w-[45px] -rotate-45 bg-amber-500/10 group-hover:bg-amber-500 text-amber-500 group-hover:text-white text-center rounded-xl me-5 transition-all duration-500">
                        <img :src="item.icon" :alt="item.name" class="h-5 w-5 rotate-45 object-contain">
                    </div>
                    <div class="flex-1">
                        <h4 class="mb-0 text-[17px] font-medium">{{ item.name }}</h4>
                    </div>
                </div><!--end content-->
            </div><!--end grid-->
        </div><!--end container-->

        <!-- Other Skills -->
        <div class="container md:mt-24 mt-16">
            <div class="grid grid-cols-1 pb-8 text-center">
                <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">Soft Skills</h3>
                <p class="text-slate-400 max-w-xl mx-auto text-[15px]">
                    Key interpersonal and professional skills that enhance my performance as a Data Analyst, Data Scientist, Machine Learning Engineer, Data Engineer, and Business Analyst.
                </p>
            </div><!--end grid-->

            <div class="grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 mt-8 gap-[30px]">
                <div v-for="item in otherSkills" :key="item.name"
                    class="flex group shadow shadow-gray-200 dark:shadow-gray-800 dark:hover:shadow-gray-700 items-center p-3 rounded-lg bg-white dark:bg-slate-900">
                    <div
                        class="flex items-center justify-center h-[45px] min-w-[45px] -rotate-45 bg-amber-500/10 group-hover:bg-amber-500 text-amber-500 group-hover:text-white text-center rounded-xl me-5 transition-all duration-500">
                        <img :src="item.icon" :alt="item.name" class="h-5 w-5 rotate-45 object-contain">
                    </div>
                    <div class="flex-1">
                        <h4 class="mb-0 text-[17px] font-medium">{{ item.name }}</h4>
                    </div>
                </div><!--end content-->
            </div><!--end grid-->
        </div><!--end container-->

        <!-- Language Skills -->
        <div class="container md:mt-24 mt-16">
            <div class="grid grid-cols-1 pb-8 text-center">
                <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">Language Skills</h3>
                <p class="text-slate-400 max-w-xl mx-auto text-[15px]">
                    Languages I use for communication and collaboration.
                </p>
            </div><!--end grid-->

            <div class="grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 mt-8 gap-[30px]">
                <div v-for="item in languages" :key="item.name"
                    class="flex group shadow shadow-gray-200 dark:shadow-gray-800 dark:hover:shadow-gray-700 items-center p-3 rounded-lg bg-white dark:bg-slate-900">
                    <div
                        class="flex items-center justify-center h-[45px] min-w-[45px] -rotate-45 bg-amber-500/10 group-hover:bg-amber-500 text-amber-500 group-hover:text-white text-center rounded-xl me-5 transition-all duration-500">
                        <img :src="item.icon" :alt="item.name" class="h-5 w-5 rotate-45 object-contain">
                    </div>
                    <div class="flex-1">
                        <h4 class="mb-0 text-[17px] font-medium">{{ item.name }}</h4>
                    </div>
                </div><!--end content-->
            </div><!--end grid-->
        </div><!--end container-->
    </section><!--end section-->
    <!-- End -->
</template>

<script>
import CountUp from 'vue-countup-v3';

export default {
    name: 'aboutCompo',
    data() {
        return {
            hobbies: [
                { name: 'Excel', icon: '/Logo1/excel.svg' },
                { name: 'Google Sheets', icon: '/Logo1/Googleslide.svg' },
                { name: 'SQL', icon: '/Logo1/sql.svg' },
                { name: 'Power BI', icon: '/Logo1/powerbi.svg' },
                { name: 'Looker Studio', icon: '/Logo1/google.svg' },
                { name: 'Tableau', icon: '/Logo1/tableu.svg' },
                { name: 'R Studio', icon: '/Logo1/rstudio.svg' },
                { name: 'Python', icon: '/Logo1/Python-logo.svg' },
                { name: 'Jupyter Notebook', icon: '/Logo1/Jupyter.svg' },
                { name: 'Google Colab', icon: '/Logo1/collab.svg' },
                { name: 'Python ML Frameworks', icon: '/Logo1/Python-logo.svg' },
                { name: 'Model Deployment', icon: '/Logo1/Python-logo.svg' },
                { name: 'GitHub', icon: '/Logo1/github.svg' },
            ],
            otherSkills: [
                { name: 'Analytical Thinking & Problem-Solving', icon: '/Logo2/Analytical-Thinking&Problem-Solving.svg' },
                { name: 'Critical Thinking', icon: '/Logo2/CriticalThinking.svg' },
                { name: 'Attention to Detail', icon: '/Logo2/AttentiontoDetail.svg' },
                { name: 'Adaptability & Continuous Learning', icon: '/Logo2/Adaptability&Continuous Learning.svg' },
                { name: 'Time Management & Prioritization', icon: '/Logo2/TimeManagement&Prioritization.svg' },
                { name: 'Data Storytelling & Visualization', icon: '/Logo2/Data Storytelling&Visualization.svg' },
                { name: 'Effective Communication', icon: '/Logo2/EffectiveCommunication.svg' },
                { name: 'Cross functional Collaboration', icon: '/Logo2/CrossfunctionalCollaboration.svg' },
                { name: 'Negotiation & Stakeholder Management', icon: '/Logo2/Negotiation&StakeholderManagement.svg' },
                { name: 'Business Acumen', icon: '/Logo2/BusinessAcumen.svg' },
                { name: 'Decision Making', icon: '/Logo2/DecisionMaking.svg' },
                { name: 'Creativity & Innovation', icon: '/Logo2/Creativity&Innovation.svg' },
                { name: 'Leadership & Mentorship', icon: '/Logo2/Leadership&Mentorship.svg' },
            ],
            languages: [
                { name: 'English', icon: '/Logo3/england.svg'},
                { name: 'Indonesian', icon: '/Logo3/indonesia.svg' },
            ]
        }
    },
    components: {
        CountUp,
    }
}
</script>

<style lang="scss" scoped></style>
