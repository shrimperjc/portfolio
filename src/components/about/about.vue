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
                        <img src="../../assets/images/meorange1.png"
                            class="rounded-full shadow-md shadow-gray-200 dark:shadow-gray-800" alt="">

                        <div
                            class="absolute lg:bottom-20 md:bottom-10 bottom-6 ltr:lg:-right-16 rtl:lg:-left-16 ltr:md:-right-8 rtl:md:-left-8 ltr:right-0 rtl:left-0 p-4 rounded-lg shadow-md dark:shadow-gray-800 bg-white dark:bg-slate-900 m-3 w-44 text-center">
                            <h6 class="font-semibold">Web Developer</h6>
                            <span class="text-2xl font-medium text-amber-500 mb-0 flex justify-center">
                                <count-up class="counter-value font-bold" :start-val="1"
                                    :end-val="13"></count-up>+<span class="text-sm text-slate-400 mt-3 ml-1"> Years</span></span>
                            <span class="text-sm text-slate-400">Experience</span>
                        </div>
                    </div>
                </div><!--end col-->

                <div class="lg:col-span-7">
                    <div class="lg:ms-5">
                        <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">I'm a
                            Passionate Front End Web Developer</h3>

                        <p class="text-slate-400 max-w-xl text-[15px]">I'm a highly motivated chap with almost two decades of experience in IT maintenance and web design.
                                I've historically worked with individuals, established smaller businesses as well as smaller start-ups to help them build an online presence with a bespoke web site tailored to their needs which as a result
                                generate more leads or sales</p>
                        <p class="text-slate-400 max-w-xl text-[15px] mt-6"></p>

                        <div class="mt-6">
                            <a href="#project"
                                class="btn bg-amber-500/10 hover:bg-amber-500 border-amber-500/10 hover:border-amber-500 text-amber-500 hover:text-white rounded-md me-2 mt-2">See
                                my Work</a>
                        </div>
                    </div>
                </div><!--end grid-->
            </div><!--end grid-->
        </div><!--end container-->

        <div class="container md:mt-24 mt-16">
            <div class="grid grid-cols-1 pb-8 text-center">
                <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">My History
                </h3>

                <p class="text-slate-400 max-w-xl mx-auto text-[15px]">
                    Programming has been in my blood since i was very small and while other kids were out enjoying themselves as teenagers, i was programming BASIC games on my BBC Micro and Atari ST. I've been coding since high school and i'm very lucky to be getting paid to do something i truly love.
                    <br><br>
                    Programming, and the internet in particular, has changed a lot since i first started coding back in the 1990's, and as a result, in this industry you need to keep on top of all new technologies.
                    Fortunately i love learning and task myself to learn something new every day.
                    What I really love is tackling something no one else knows how to do, or maybe no one has ever tried to do.
                    <br><br>
                    That's the most magical thing of all, figuring out how to write code to do something totally unique, or even seemingly impossible.
                    Even today, i still love the art of coding, especially figuring out problems with almost no information and learning a new way to achieve a result or overcome an obstacle.
                    <br><br>
                    I started off coding in BASIC back in the 1980's, then took a City and Guilds course in C++, which gave me an introduction to object oriented programming.
                    I've always been interested in how a whole website is constructed and how all the pieces of technology that make up a website work together and in conjunction to come together and produce
                    websites that we know today. As a result, my knowledge covers front-end design languages such as HTML and CSS, back-end languages such as PHP, behavioural languages such as Javascript and jQuery and
                    backend database languages such as T-SQL and mySQL.
                </p>
                <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold md:mt-24 mt-16">Hobbies & Expertise</h3>
                <p class="text-slate-400 max-w-xl mx-auto text-[15px]">
                    What floats my boat outside of coding...
                </p>
            </div><!--end grid-->

            <div class="grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 mt-8 gap-[30px]">
                <div v-for="item in hobbies" :key="item"
                    class="flex group shadow shadow-gray-200 dark:shadow-gray-800 dark:hover:shadow-gray-700 items-center p-3 rounded-lg bg-white dark:bg-slate-900">
                    <div
                        class="flex items-center justify-center h-[45px] min-w-[45px] -rotate-45 bg-amber-500/10 group-hover:bg-amber-500 text-amber-500 group-hover:text-white text-center rounded-xl me-5 transition-all duration-500">
                        <i :data-feather="item.icon" class="h-5 w-5 rotate-45"></i>
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
import feather from 'feather-icons'

export default {
    name: 'aboutCompo',
    data() {
        return {
            hobbies: [
                {
                    name: 'Live Music',
                    icon: 'music'
                },
                {
                    name: 'Coffee',
                    icon: 'coffee'
                },
                {
                    name: 'Reading',
                    icon: 'book-open'
                },
                {
                    name: 'Gaming',
                    icon: 'hard-drive'
                },
                {
                    name: 'Music',
                    icon: 'music'
                },
                {
                    name: 'Games',
                    icon: 'hard-drive'
                },
                {
                    name: 'Designing',
                    icon: 'figma'
                },
                {
                    name: 'Sports',
                    icon: 'target'
                },
            ]
        }
    },
    mounted() {
        feather.replace()
        
    },
    components: {
        CountUp,
    }
}
</script>

<style lang="scss" scoped></style>