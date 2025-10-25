<template>
   <!-- Start -->
   <section class="relative md:py-24 py-16 bg-gray-50 dark:bg-slate-800" id="contact">
            <div class="container">
                <div class="grid grid-cols-1 pb-8 text-center wow animate__animated animate__fadeInUp" data-wow-delay=".1s">
                    <h3 class="mb-6 md:text-2xl text-xl md:leading-normal leading-normal font-semibold">Contact Me</h3>

                    <p class="text-slate-400 max-w-xl mx-auto text-[15px]">I am available to discuss collaborations, freelance opportunities, and professional inquiries.</p>
                </div><!--end grid-->

                <div class="grid grid-cols-1 lg:grid-cols-12 md:grid-cols-2 mt-8 items-center gap-[30px] " >
                    <div class="lg:col-span-8">
                        <div class="p-6 rounded-md shadow bg-white dark:bg-slate-900 wow animate__animated animate__fadeInUp" data-wow-delay=".3s">
                            <form method="post" name="myForm" id="myForm" onsubmit="return validateForm()">
                                <p class="mb-0 text-red-500" id="error-msg"></p>
                                <div id="simple-msg" class="text-green-500"></div>
                                <div class="grid lg:grid-cols-12 lg:gap-5">
                                    <div class="lg:col-span-6 mb-5">
                                        <input name="name" id="name" type="text" class="form-input w-full py-2 px-3 border border-inherit dark:border-gray-800 dark:bg-slate-900 dark:text-slate-200 rounded h-10 outline-none bg-transparent focus:border-amber-500/50 dark:focus:border-amber-500/50 focus:shadow-none focus:ring-0 text-[15px]" placeholder="Name :">
                                    </div>
    
                                    <div class="lg:col-span-6 mb-5">
                                        <input name="email" id="email" type="email" class="form-input w-full py-2 px-3 border border-inherit dark:border-gray-800 dark:bg-slate-900 dark:text-slate-200 rounded h-10 outline-none bg-transparent focus:border-amber-500/50 dark:focus:border-amber-500/50 focus:shadow-none focus:ring-0 text-[15px]" placeholder="Email :">
                                    </div><!--end col-->
                                </div>

                                <div class="grid grid-cols-1">
                                    <div class="mb-5">
                                        <input name="subject" id="subject" class="form-input w-full py-2 px-3 border border-inherit dark:border-gray-800 dark:bg-slate-900 dark:text-slate-200 rounded h-10 outline-none bg-transparent focus:border-amber-500/50 dark:focus:border-amber-500/50 focus:shadow-none focus:ring-0 text-[15px]" placeholder="Subject :">
                                    </div>

                                    <div class="mb-5">
                                        <textarea name="comments" id="comments" class="form-input w-full py-2 px-3 border border-inherit dark:border-gray-800 dark:bg-slate-900 dark:text-slate-200 rounded h-28 outline-none bg-transparent focus:border-amber-500/50 dark:focus:border-amber-500/50 focus:shadow-none focus:ring-0 text-[15px]" placeholder="Message :"></textarea>
                                    </div>
                                </div>
                                <button type="submit" id="submit" name="send" class="btn bg-amber-500 hover:bg-amber-600 border-amber-500 hover:border-amber-600 text-white rounded-md h-11 justify-center flex items-center">Send Message</button>
                            </form>
                        </div>
                    </div>

                    <div class="lg:col-span-4">
                        <div class="lg:ms-8">
                            <!-- info contact tetap -->
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
    name: 'getInTOuch',
    mounted() {
        // fungsi global sesuai onsubmit di form
        window.validateForm = () => {
            const name = document.getElementById("name").value;
            const email = document.getElementById("email").value;
            const subject = document.getElementById("subject").value;
            const message = document.getElementById("comments").value;

            if (!name || !email || !subject || !message) {
                document.getElementById("error-msg").innerText = "❌ Please fill all fields!";
                return false;
            }

            emailjs.send(
                "service_kcc2cze",     // ✅ Service ID
                "template_41rhgh9",   // ✅ Template ID
                {
                    name: name,
                    email: email,
                    subject: subject,
                    message: message,
                    time: new Date().toLocaleString() // ✅ tambahan waktu
                },
                "lTf5gjxPIdkt7feh1"    // ✅ Public Key
            ).then(() => {
                document.getElementById("simple-msg").innerText = "✅ Message sent successfully!";
                document.getElementById("error-msg").innerText = "";
                document.getElementById("myForm").reset();
            }).catch((err) => {
                console.error("EmailJS Error:", err);
                document.getElementById("error-msg").innerText = "❌ Failed to send message!";
                document.getElementById("simple-msg").innerText = "";
            });

            return false; // biar ga reload halaman
        }
    }
}
</script>

<style lang="scss" scoped>
</style>
