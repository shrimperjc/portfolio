<template>
    <!-- Start -->
    <section class="relative md:py-24 py-16" id="project">
            <div class="container">
                <div class="grid grid-cols-1 pb-8 text-center">
                    <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">My Work & Projects</h3>

                    <p class="text-slate-400 max-w-xl mx-auto text-[15px]">Here is a short list of some of the companies I have helped with web development in the past</p>
                </div><!--end grid-->

                <div class="grid lg:grid-cols-4 md:grid-cols-3 grid-cols-1 mt-8 gap-[30px]">
                    <div v-for="item in projects" :key="item" class="relative group overflow-hidden rounded-lg shadow shadow-slate-200 dark:shadow-gray-800">
                        <img :src="item.image" alt="">
                        <div class="absolute inset-0 opacity-0 group-hover:opacity-100 bg-gradient-to-b to-slate-900 from-transparent transition-all duration-500"></div>
                        <div class="absolute bottom-0 opacity-0 group-hover:opacity-100 m-6 transition-all duration-500">
                            <a :href="item.link" class="text-white hover:text-amber-500 font-semibold transition-all duration-500">{{item.name}}</a>
                            <span class="block text-sm text-slate-400">{{ item.languag }}</span>
                            <span></span>
                            <span class="block text-sm text-green-400">{{ item.tech }}</span>
                        </div>

                        <div class="absolute z-10 opacity-0 group-hover:opacity-100 top-1/2 -translate-y-1/2 right-0 left-0 mx-auto text-center transition-all duration-500">
                            <!-- <a @click="showMultiple" class="btn bg-amber-500 hover:bg-amber-600 border-amber-500 hover:border-amber-600 text-white btn-icon rounded-full lightbox">
                                <i class="uil uil-camera"></i>
                            </a> -->
                        </div>
                    </div><!--end content-->
                    
                   
                </div><!--end grid-->
            </div><!--end container-->
        </section><!--end section-->
        <!-- End -->
        <vue-easy-lightbox :visible="visibleRef" :imgs="imgsRef" :index="indexRef" @hide="onHide"></vue-easy-lightbox>

</template>

<script>
import VueEasyLightbox from 'vue-easy-lightbox';
import { ref } from 'vue'

    export default {
        name: 'projectComp',
        data() {
            return {
                projects:[
                    {
                        image: require('../../assets/images/works/colzoologo.png'),
                        name: 'Colchester Zoo',
                        languag: 'Website Joomla build and code work',
                        link: 'https://www.colchester-zoo.com/',
                        tech: 'Joomla, HTML, CSS'
                    },
                    {
                        image: require('../../assets/images/works/stjlogo.png'),
                        name: 'St. James Auctions, Piccadilly',
                        languag: 'Full custom Wordpress website design and build',
                        link: 'https://stjauctions.com/',
                        tech: 'Wordpress, PHP'
                    },
                    
                    {
                        image: require('../../assets/images/works/lselogo.jpeg'),
                        name: 'London South East',
                        languag: 'Website Amendments and Updates',
                        link: 'https://www.lse.co.uk/',
                        tech: 'Classic ASP, GraphQL'
                    },
                    
                    {
                        image: require('../../assets/images/works/syngentalogo.png'),
                        name: 'Syngenta UK',
                        languag: 'Web Site amendments / content creation and update',
                        link: 'https://www.syngenta.co.uk/',
                        tech: 'In house software'
                    },
                    
                    {
                        image: require('../../assets/images/works/bplogo.jpeg'),
                        name: 'Babyprints',
                        languag: 'Full E-Commerce website design and build',
                        link: 'https://babyprints.co.uk/',
                        tech: 'Wordpress, PHP'
                    },
                    
                    {
                        image: require('../../assets/images/works/wblogo.jpeg'),
                        name: 'West Bromwich Building Society',
                        languag: 'Front end website build, and backend user admin configuration',
                        link: 'https://quote.insurance-westbrom.com/',
                        tech: 'HTML, CSS, VueJS'
                    },
                    
                    {
                        image: require('../../assets/images/works/biolinelogo.png'),
                        name: 'Bioline',
                        languag: 'Mobile App Development',
                        link: 'https://www.biolineagrosciences.com/?products=bioline-app',
                        tech: 'In house software'
                    },
                    
                    {
                        image: require('../../assets/images/works/amblogo.jpeg'),
                        name: 'Onboard Air Ambulance',
                        languag: 'Charity Wordpress website build',
                        link: 'https://theairambulanceservice.org.uk/our-helicopters/',
                        tech: 'Wordpress, PHP'
                    },
                    
                ]
                
            }
        },
        components: {
        VueEasyLightbox,
    },
    setup() {
        const visibleRef = ref(false)
        const indexRef = ref(0)
        const imgsRef = ref([])


        const onShow = () => {
            visibleRef.value = true
        }
        const showMultiple = () => {
            imgsRef.value = [
            require('../../assets/images/works/colzoonew.jpg'),
            require('../../assets/images/works/stjnew.jpg'),
            require('../../assets/images/works/webdesignnew.jpg'),
            require('../../assets/images/works/webdesignnew.jpg'),
            require('../../assets/images/works/babypnew.jpg'),
            require('../../assets/images/works/webdesignnew.jpg'),
            require('../../assets/images/works/webdesignnew.jpg'),
            require('../../assets/images/works/webdesignnew.jpg'),

            ]
            console.log(showMultiple.value, 'rrr');

            indexRef.value = 0
            onShow()
        }
        const onHide = () => (visibleRef.value = false)

        return {
            visibleRef,
            indexRef,
            imgsRef,
            showMultiple,
            onHide
        }
    }
        
    }
</script>

<style lang="scss" scoped>

</style>