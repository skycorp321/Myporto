<template>
    <!-- Start -->
    <section class="relative md:py-24 py-16" id="project">
        <div class="container">
            <!-- Header -->
            <div class="grid grid-cols-1 pb-8 text-center wow animate__animated animate__fadeInUp" data-wow-delay=".1s">
                <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">
                    My Work & Projects
                </h3>

                <p class="text-slate-400 max-w-xl mx-auto text-[15px]">
                    Showcasing end to end data projects, including pipeline development, analytical insights,
                    predictive modeling, and data-driven solutions in Data Engineering, Analysis, Machine Learning,
                    and Data Science.
                </p>
            </div>

            <!-- Project Grid -->
            <div class="grid lg:grid-cols-4 md:grid-cols-3 grid-cols-1 mt-8 gap-[30px]">
                <div 
                    v-for="(item, index) in projects" 
                    :key="index"
                    class="relative group overflow-hidden rounded-lg shadow shadow-slate-200 dark:shadow-gray-800 wow animate__animated animate__fadeInUp"
                    data-wow-delay=".3s"
                >
                    <!-- Klik gambar langsung buka link -->
                    <a :href="item.link" target="_blank" rel="noopener noreferrer">
                        <!-- ✅ Perbaikan agar gambar tidak terpotong -->
                        <img 
                            :src="item.image" 
                            alt="" 
                            class="w-full h-60 object-cover object-center rounded-t-lg"
                        >
                        
                        <!-- Overlay efek hover -->
                        <div 
                            class="absolute inset-0 opacity-0 group-hover:opacity-100 bg-gradient-to-b to-slate-900 from-transparent transition-all duration-500">
                        </div>
                        
                        <!-- Info Project -->
                        <div 
                            class="absolute bottom-0 opacity-0 group-hover:opacity-100 m-6 transition-all duration-500">
                            <span 
                                class="text-white hover:text-amber-500 font-semibold transition-all duration-500">
                                {{ item.name }}
                            </span>
                            <span class="block text-sm text-slate-400">{{ item.languag }}</span>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </section>
    <!-- End -->
</template>

<script>
export default {
    name: 'projectComp',
    data() {
        return {
            projects: [
                {
                    image: require('../../assets/images/works/1.png'),
                    name: 'Vegetables Classification Using CNN',
                    languag: 'Machine Learning',
                    link: 'https://builtbyariel.site/login'
                },
                {
                    image: require('../../assets/images/works/2.png'),
                    name: 'Revou Capstone Project',
                    languag: 'Power BI',
                    link: 'https://drive.google.com/file/d/1oWFS8BCOxGkkPaoOw2Gx3Eybkzaw3_Cy/view?usp=sharing'
                },
                {
                    image: require('../../assets/images/works/3.jpg'),
                    name: 'Valexy Theme',
                    languag: 'Landing',
                    link: 'https://github.com/yourusername/valexy'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped></style>
