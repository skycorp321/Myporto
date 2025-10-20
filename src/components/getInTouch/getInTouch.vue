<template>
     <!-- Start -->
     <section class="relative md:py-24 py-16 bg-gray-50 dark:bg-slate-800" id="contact">
            <div class="container">
                <div class="grid grid-cols-1 pb-8 text-center">
                    <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">Contact Me</h3>

                    <p class="text-slate-400 max-w-xl mx-auto text-[15px]">I am available to discuss collaborations, freelance opportunities, and professional inquiries.</p>
                </div><!--end grid-->

                <div class="grid grid-cols-1 lg:grid-cols-12 md:grid-cols-2 mt-8 items-center gap-[30px]">
                    <div class="lg:col-span-8">
                        <div class="p-6 rounded-md shadow bg-white dark:bg-slate-900">
                            <!-- tambahin @submit.prevent -->
                            <form @submit.prevent="sendEmail">
                                <div class="grid lg:grid-cols-12 lg:gap-5">
                                    <div class="lg:col-span-6 mb-5">
                                        <input v-model="form.name" name="name" id="name" type="text" 
                                               class="form-input w-full py-2 px-3 border border-inherit dark:border-gray-800 dark:bg-slate-900 dark:text-slate-200 rounded h-10 outline-none bg-transparent focus:border-amber-500/50 dark:focus:border-amber-500/50 focus:shadow-none focus:ring-0 text-[15px]" 
                                               placeholder="Name :">
                                    </div>
    
                                    <div class="lg:col-span-6 mb-5">
                                        <input v-model="form.email" name="email" id="email" type="email" 
                                               class="form-input w-full py-2 px-3 border border-inherit dark:border-gray-800 dark:bg-slate-900 dark:text-slate-200 rounded h-10 outline-none bg-transparent focus:border-amber-500/50 dark:focus:border-amber-500/50 focus:shadow-none focus:ring-0 text-[15px]" 
                                               placeholder="Email :">
                                    </div><!--end col-->
                                </div>

                                <div class="grid grid-cols-1">
                                    <div class="mb-5">
                                        <input v-model="form.subject" name="subject" id="subject" 
                                               class="form-input w-full py-2 px-3 border border-inherit dark:border-gray-800 dark:bg-slate-900 dark:text-slate-200 rounded h-10 outline-none bg-transparent focus:border-amber-500/50 dark:focus:border-amber-500/50 focus:shadow-none focus:ring-0 text-[15px]" 
                                               placeholder="Subject :">
                                    </div>

                                    <div class="mb-5">
                                        <textarea v-model="form.message" name="comments" id="comments" 
                                                  class="form-input w-full py-2 px-3 border border-inherit dark:border-gray-800 dark:bg-slate-900 dark:text-slate-200 rounded h-28 outline-none bg-transparent focus:border-amber-500/50 dark:focus:border-amber-500/50 focus:shadow-none focus:ring-0 text-[15px]" 
                                                  placeholder="Message :"></textarea>
                                    </div>
                                </div>
                                <button type="submit" id="submit" name="send" 
                                        class="btn bg-amber-500 hover:bg-amber-600 border-amber-500 hover:border-amber-600 text-white rounded-md h-11 justify-center flex items-center">
                                        Send Message
                                </button>
                            </form>
                            <!-- Tambahin feedback -->
                            <p v-if="successMsg" class="text-green-500 mt-3">{{ successMsg }}</p>
                            <p v-if="errorMsg" class="text-red-500 mt-3">{{ errorMsg }}</p>
                        </div>
                    </div>

                    <div class="lg:col-span-4">
                        <div class="lg:ms-8">
                            <div class="flex">
                                <div class="icons text-center mx-auto">
                                    <i class="uil uil-phone block rounded text-2xl dark:text-white mb-0"></i>
                                </div>
    
                                <div class="flex-1 ms-6">
                                    <h5 class="text-[17px] dark:text-white mb-2 font-medium">Phone</h5>
                                    <a href="tel:+62 851-1732-7071" class="text-slate-400 text-[15px]">+62 851-1732-7071</a>
                                </div>
                            </div>
    
                            <div class="flex mt-4">
                                <div class="icons text-center mx-auto">
                                    <i class="uil uil-envelope block rounded text-2xl dark:text-white mb-0"></i>
                                </div>
    
                                <div class="flex-1 ms-6">
                                    <h5 class="text-[17px] dark:text-white mb-2 font-medium">Email</h5>
                                    <a href="mailto:muhamadariel45@gmail.com" class="text-slate-400 text-[15px]">muhamadariel45@gmail.com</a>
                                </div>
                            </div>
    
                            <div class="flex mt-4">
                                <div class="icons text-center mx-auto">
                                    <i class="uil uil-map-marker block rounded text-2xl dark:text-white mb-0"></i>
                                </div>
    
                                <div class="flex-1 ms-6">
                                    <h5 class="text-[17px] dark:text-white mb-2 font-medium">Location</h5>
                                    <p class="text-slate-400 text-[15px] mb-2">Bekasi, Indonesia</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div><!--end grid-->
            </div><!--end container-->
        </section><!--end section-->
        <!-- End -->
</template>

<script>
import emailjs from "emailjs-com";

export default {
    name: 'getInTouch',
    data() {
        return {
            form: {
                name: "",
                email: "",
                subject: "",
                message: ""
            },
            successMsg: "",
            errorMsg: ""
        }
    },
    methods: {
        sendEmail() {
            emailjs.send(
                "service_kcc2cze",    // Service ID kamu
                "template_41rhgh9",   // Template ID kamu
                {
                  name: this.form.name,
                  email: this.form.email,
                  subject: this.form.subject,
                  message: this.form.message,
                  time: new Date().toLocaleString() // tambahan waktu
                },
                "lTf5gjxPIdkt7feh1"   // Public Key kamu
            ).then(() => {
                this.successMsg = "✅ Message sent successfully!";
                this.errorMsg = "";
                this.form = { name: "", email: "", subject: "", message: "" };
            }).catch((err) => {
                console.error("EmailJS Error:", err);
                this.errorMsg = "❌ Failed to send message. Please try again.";
                this.successMsg = "";
            });
        }
    }
}
</script>


<style lang="scss" scoped>
</style>
