<template>
    <section class=" px-[6%] sm:px-[10%] lg:px-[20%] bg-gray-200 py-10 md:h-[80vh]">
        <h2 class="text-[#555] font-bold pb-[20px]">CONTACT ME</h2>
        <form ref="form" @submit.prevent="sendEmail" class="flex flex-col gap-2">
            <label class="text-[18px] lg:text-[20px]">Name:</label>
            <input type="text" name="user_name" placeholder="Enter Your Name" class="p-3 rounded-md  border border-gray-300" required>
            <label class="text-[18px] lg:text-[20px]">Email:</label>
            <input type="email" name="user_email" placeholder="Email" class="p-3 rounded-md " required>
            <label class="text-[18px] lg:text-[20px]">Message:</label>
            <textarea name="message" rows="4" class="rounded-md p-3 border border-gray-300" placeholder="Message"></textarea>
            <input type="submit" value="Send" class="bg-green-100 border rounded-xl border-gray-300 p-[15px] font-bold flex justify-center items-center text-center cursor-pointer">
        </form>
    </section>
    
</template>

<script>
import emailjs from '@emailjs/browser';
  export default {
    methods: {
      sendEmail() {
        emailjs.sendForm('contact_service', 'contact_form', this.$refs.form, 'bC5Pi2n9iozeJHTpp')
          .then((result) => {
              alert('SUCCESS!', result.text);
              result.text = ''
              result.email = ''
          }, (error) => {
              alert('FAILED...', error.text);
          });
      }
    }
  }
</script>
<style>

</style>
