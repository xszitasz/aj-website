<template>
    <section id="topbar" class="d-flex align-items-center">

    <div class="container d-flex justify-content-center justify-content-md-between">
      <div class="contact-info d-flex align-items-center">
        <i class="bi bi-envelope-fill"></i><a href="mailto:xszitasz@gmail.com">{{ email }}</a>
        <i class="bi bi-phone-fill phone-icon"></i> {{ phoneNumber}}
      </div>

      <div class="social-links d-none d-md-block">
        <a href="https://www.facebook.com/profile.php?id=100017322969115" class="facebook"><i class="bi bi-facebook"></i></a>
        <a href="#" class="instagram"><i class="bi bi-instagram"></i></a>
        <a href="#" class="linkedin"><i class="bi bi-linkedin"></i></a>
        <a @click="changeLanguage('SVK')">{{ language }}</a>
        <a @click="changeLanguage('HUN')">{{ language }}</a>
      </div>

    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
        return {
            email: 'xszitasz@gmail.com',
            language: 'SVK',
            phoneNumber: '+421 910 623 309'
        }
    },
    methods: {
        changeLanguage(language: string){
            if(language === 'HUN') {
                this.phoneNumber = '+421 910 623 309';
            } else {
                this.phoneNumber = '+36 910 623 309';
            }
        }
    }
})
</script>

<style scoped>
#topbar {
  background: #fbfbfb;
  font-size: 15px;
  height: 40px;
  padding: 0;
}

#topbar .contact-info a {
  line-height: 0;
  color: #444444;
  transition: 0.3s;
}

#topbar .contact-info a:hover {
  color: #5cb874;
}

#topbar .contact-info i {
  color: #5cb874;
  line-height: 0;
  margin-right: 5px;
}

#topbar .contact-info .phone-icon {
  margin-left: 15px;
}

#topbar .social-links a {
  color: #6f6f6f;
  padding: 4px 12px;
  display: inline-block;
  line-height: 1px;
  transition: 0.3s;
}

#topbar .social-links a:hover {
  color: #5cb874;
}
</style>
