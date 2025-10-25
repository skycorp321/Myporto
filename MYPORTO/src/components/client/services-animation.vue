<template>
    <!-- Start -->
    <section class="relative md:py-24 py-16 bg-gray-50 dark:bg-slate-800" id="service">
        <div class="container">
            <div class="grid grid-cols-1 pb-8 text-center wow animate__animated animate__fadeInUp" data-wow-delay=".1s">
                <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">My Expertise</h3>

                <p class="text-slate-400 max-w-xl mx-auto text-[15px]">End to end data solutions from engineering to insights.</p>
            </div><!--end grid-->

            <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 mt-8 gap-[30px]">
                <!-- Content -->
                <div 
                    v-for="item in services" 
                    :key="item.name" 
                    class="px-6 py-10 shadow shadow-gray-200 hover:shadow-md dark:shadow-gray-800 dark:hover:shadow-gray-700 transition duration-500 rounded-2xl bg-white dark:bg-slate-900 wow animate__animated animate__fadeInUp" 
                    data-wow-delay=".3s"
                >
                    <!-- Feather diganti img -->
                    <img :src="item.icon" alt="icon" class="h-12 w-12 object-contain" />

                    <div class="content mt-7">
                        <a href="" class="title h5 text-[17px] font-medium hover:text-amber-500">{{ item.name }}</a>
                        <p class="text-slate-400 mt-3 text-[15px] text-justify">{{ item.desc }}</p>
                    </div>
                </div>
                <!-- Content -->
            </div>
        </div><!--end container-->
    </section><!--end section-->
    <!-- End -->

    <!-- Start -->
    <section class="py-20 w-full table relative bg-[url('../../assets/images/bg/bg4.svg')] bg-no-repeat bg-center bg-cover" id="service">
        <div class="absolute inset-0 bg-slate-900/70"></div>
        <div class="container relative">
            <div class="grid grid-cols-1 pb-8 text-center wow animate__animated animate__fadeInUp" data-wow-delay=".1s">
                <h3 class="mb-4 md:text-2xl text-xl text-white font-semibold">I Am Available For Opportunities</h3>

                <p class="text-white/80 max-w-xl mx-auto text-[15px]">
                    Obviously, I'm a Data Enthusiast with over 1 years of experience. Experienced in all stages of data projects.
                </p>
            </div><!--end grid-->
        </div><!--end container-->
    </section><!--end section-->
    <!-- End -->
</template>

<script>
export default {
    data() {
        return {
            services: [
                {
                        icon: ('/Logo4/DataScientist.svg'),
                        name: 'Data Scientist',
                        desc: 'Transforming complex data into meaningful insights that drive innovation, smarter decisions, and sustainable growth.'
                    },
                    {
                        icon: ('/Logo4/Dataengineer.svg'),
                        name: 'Data Engineer',
                        desc: 'Building reliable data systems and pipelines that make information accessible, accurate, and ready for analysis.'
                    },
                    {
                        icon: ('/Logo4/MLEngineer.svg'),
                        name: 'ML Engineer',
                        desc: 'Developing intelligent solutions powered by machine learning to improve efficiency and create business value.'
                    },
                    {
                        icon: ('/Logo4/Dataanlayst.svg'),
                        name: 'Data Analyst',
                        desc: 'Turning complex data into clear, actionable insights that support strategy and drive better outcomes.'
                    },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>

</style>
<template>
    <!-- Start -->
    <section class="relative md:py-24 py-16 bg-gray-50 dark:bg-slate-800" id="service">
        <div class="container">
            <div class="grid grid-cols-1 pb-8 text-center wow animate__animated animate__fadeInUp" data-wow-delay=".1s">
                <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">My Expertise</h3>

                <p class="text-slate-400 max-w-xl mx-auto text-[15px]">End to end data solutions from engineering to insights.</p>
            </div><!--end grid-->

            <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 mt-8 gap-[30px]">
                <!-- Content -->
                <div 
                    v-for="item in services" 
                    :key="item.name" 
                    class="px-6 py-10 shadow shadow-gray-200 hover:shadow-md dark:shadow-gray-800 dark:hover:shadow-gray-700 transition duration-500 rounded-2xl bg-white dark:bg-slate-900 wow animate__animated animate__fadeInUp" 
                    data-wow-delay=".3s"
                >
                    <!-- Feather diganti img -->
                    <img :src="item.icon" alt="icon" class="h-12 w-12 object-contain" />

                    <div class="content mt-7">
                        <a href="" class="title h5 text-[17px] font-medium hover:text-amber-500">{{ item.name }}</a>
                        <p class="text-slate-400 mt-3 text-[15px] text-justify">{{ item.desc }}</p>
                    </div>
                </div>
                <!-- Content -->
            </div>
        </div><!--end container-->
    </section><!--end section-->
    <!-- End -->

    <!-- Start -->
    <section class="py-20 w-full table relative bg-[url('../../assets/images/bg/bg4.svg')] bg-no-repeat bg-center bg-cover" id="service">
        <div class="absolute inset-0 bg-slate-900/70"></div>
        <div class="container relative">
            <div class="grid grid-cols-1 pb-8 text-center wow animate__animated animate__fadeInUp" data-wow-delay=".1s">
                <h3 class="mb-4 md:text-2xl text-xl text-white font-semibold">I Am Available For Freelance Opportunities</h3>

                <p class="text-white/80 max-w-xl mx-auto text-[15px]">
                    Obviously, I'm a Data Enthusiast with over 1 years of experience. Experienced in all stages of data projects.
                </p>
            </div><!--end grid-->
        </div><!--end container-->
    </section><!--end section-->
    <!-- End -->
</template>

<script>
export default {
    data() {
        return {
            services: [
                    {
                        icon: ('/Logo4/DataScientist.svg'),
                        name: 'Data Scientist',
                        desc: 'Transforming complex data into meaningful insights that drive innovation, smarter decisions, and sustainable growth.'
                    },
                    {
                        icon: ('/Logo4/Dataengineer.svg'),
                        name: 'Data Engineer',
                        desc: 'Building reliable data systems and pipelines that make information accessible, accurate, and ready for analysis'
                    },
                    {
                        icon: ('/Logo4/MLEngineer.svg'),
                        name: 'ML Engineer',
                        desc: 'Developing intelligent solutions powered by machine learning to improve efficiency and create business value.'
                    },
                    {
                        icon: ('/Logo4/Dataanlayst.svg'),
                        name: 'Data Analyst',
                        desc: 'Turning complex data into clear, actionable insights that support strategy and drive better outcomes.'
                    },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>

</style>
