<template>
  <section class="relative w-full" data-aos="zoom-in-up">
    <div class="absolute top-0 inset-x-0 h-64 flex items-start">
      <div class="h-24 w-2/3 bg-gradient-to-br from-[#570cac] blur-2xl invisible opacity-40"></div>
      <div class="h-20 w-3/5 bg-gradient-to-r from-[#670ccf] opacity-40 blur-2xl"></div>
    </div>
    <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-screen-lg lg:max-w-screen-xl mx-auto relative">
      <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 relative pt-24 lg:max-w-none max-w-2xl md:max-w-3xl mx-auto">
        <div class="lg:py-6">
          <div class="text-center lg:text-left">
              <h1 class=" text-white font-bold text-4xl md:text-5xl lg:text-6xl">
                  Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#cbe7e3] to-[#05999e] typing-effect">
                  Duc Le
                          </span>
              </h1>
          </div>
          <p class="text-[#a5d8f1] pt-8 text-2xl lg:text-left mx-auto max-w-xl" data-aos="fade-right" data-aos-delay="200">
            With a passion for developing web applications and a spirit of learning new knowledge. I am always looking for new challenges and opportunities to improve my skills.
          </p>
          <div class="flex items-center gap-3 pt-9 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0">
            
            <button class="border border-primary px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center">
              <div class="hover:scale-105 transition-all ease-in-out flex justify-center items-center relative">
                <div class="svg-container">
                  <svg class="download-icon" width="18" height="22" viewBox="0 0 18 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path class="download-arrow" d="M13 9L9 13M9 13L5 9M9 13V1" stroke="#b0fde0"
                    stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                    />
                    <path d="M1 17V18C1 18.7956 1.31607 19.5587 1.87868 20.1213C2.44129
                    20.6839 3.20435 21 4 21H14C14.7956 21 15.5587 20.6839 16.1213
                    20.1213C16.6839 19.5587 17 18.7956 17 18V17"
                    stroke="#b0fde0" stroke-width="2" stroke-linecap="round" />
                  </svg>
                  <div class="download-loader text-[#a5d8f1] hidden"></div>
                </div>
                <a href="/public/Le Minh Duc - Intern_Fresher Developer - CV.pdf" download="Le Minh Duc - Intern_Fresher Developer - Resume.pdf" class="pl-2 text-[#b0fde0]"> Download resume</a>
              </div>
            </button>
          </div>
        </div>
        <div class="lg:h-full md:flex">
          <div class="flex w-full h-96 min-h-[24rem] lg:min-h-[none] lg:w-full lg:h-full items-center relative">
            <div class="absolute z-0 top-1/2 -translate-y-1/2 w-5/6 right-0 h-[calc(80%+20px)] bg-gradient-to-tr opacity-25 from-[#570cac] to-primary blur-2xl"></div>
            <div class="absolute h-full z-10 p-2 -translate-y-1/2 top-1/2 lg:right-3 md:right-40 sm:right-16 rounded-full shadow-lg border border-primary neon-effect">
              <img src="@/assets/top_picture.jpg" alt="Hero pic" width="500" height="auto" loading="lazy"
              class="w-full h-full rounded-full object-cover animate-float scale-80"
              data-aos="fade-left" data-aos-delay="300"
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import AOS from 'aos';
import 'aos/dist/aos.css';
AOS.init();
</script>

<style>
.rounded-image {
  width: 200px;  /* Điều chỉnh kích thước theo yêu cầu */
  height: 200px; /* Điều chỉnh kích thước theo yêu cầu */
  border-radius: 50%;
  object-fit: cover;  /* Đảm bảo hình ảnh không bị biến dạng */
}
@keyframes float {
0% {
  transform: translateY(0);
}
50% {
  transform: translateY(-10px);
}
100% {
  transform: translateY(0);
}
}

.animate-float {
animation: float 4s ease-in-out infinite; /* 4s là thời gian một chu kỳ */
}

/* Hiệu ứng neon - Phiên bản tối ưu */
.neon-effect {
  position: relative;
  z-index: 1;
}

.neon-effect::before {
  content: '';
  position: absolute;
  top: -5px;
  left: -5px;
  right: -5px;
  bottom: -5px;
  border-radius: 50%;
  background: radial-gradient(
    circle, 
    rgba(96, 234, 224, 0.6) 0%,  /* #60eae0 - Cyan nhạt */
    rgba(87, 12, 172, 0.2) 70%   /* #570cac - Tím */
  );
  filter: blur(15px);
  z-index: -1;
  animation: neon-glow 3s ease-in-out infinite alternate;
}

.neon-effect::after {
  content: '';
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  border-radius: 50%;
  border: 2px solid rgba(96, 234, 224, 0.5);  /* Viền cyan */
  box-shadow: 
    0 0 15px rgba(96, 234, 224, 0.8),  /* Lớp trong */
    0 0 30px rgba(5, 153, 158, 0.6),   /* #05999e - Cyan đậm */
    0 0 45px rgba(87, 12, 172, 0.4);   /* #570cac - Tím */
  z-index: -1;
  animation: neon-border 3s ease-in-out infinite alternate;
}

@keyframes neon-glow {
  0% {
    opacity: 0.7;
    transform: scale(0.95);
  }
  100% {
    opacity: 1;
    transform: scale(1.1);
  }
}

@keyframes neon-border {
  0% {
    box-shadow: 
      0 0 15px rgba(96, 234, 224, 0.8),
      0 0 30px rgba(5, 153, 158, 0.6),
      0 0 45px rgba(87, 12, 172, 0.4);
  }
  100% {
    box-shadow: 
      0 0 25px rgba(96, 234, 224, 1),
      0 0 50px rgba(5, 153, 158, 0.8),
      0 0 75px rgba(103, 12, 207, 0.6);  /* #670ccf - Tím sáng */
  }
}
</style>