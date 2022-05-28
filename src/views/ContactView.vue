<template>
    <div class="container">
        <form ref="form" @submit.prevent="sendEmail">
          <label>Name</label>
          <input 
            type="text" 
            v-model="from_name"
            name="from_name"
            placeholder="Your Name"
            required
          >
          <label>Email</label>
          <input 
            type="email" 
            v-model="email"
            name="email"
            placeholder="Your Email"
            required
            >
          <label>Message</label>
          <textarea 
            name="message"
            v-model="message"
            cols="30" rows="5"
            placeholder="Message"
            required>
            
          </textarea>
          
          <input type="submit" value="Send">
        </form>
    </div>
</template>

<script> 
import emailjs from 'emailjs-com';

export default {
    data() {
        return {
            from_name: '',
            email: '',
            message: '',
        }
    },
    methods: {
    sendEmail() {
      emailjs.sendForm("service_a7noxxa", "template_hdh1hwd", this.$refs.form, "J0OqH6uG8nV2RSJsj")
        .then((result) => {
            console.log('SUCCESS!', result.text);
        }, (error) => {
            console.log('FAILED...', error.text);
        });
        this.from_name = ''
        this.email = ''
        this.message= ''
    }

    
  }
}
</script>

<style scoped>
* {
    box-sizing: border-box;
    font-weight: bold;
}

.container {
  display: block;
  margin:auto;
  text-align: center;
  border-radius: 5px;
  padding: 20px;
  width: 50%;
  box-shadow: 0px 0px 20px rgb(5,206,233);
}

label {
  float: left;
}

input[type=text], [type=email], textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

input[type=submit] {
  background-color: rgb(5,206,233);
  color: black;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: rgb(5, 100, 112);
}
</style>