<template>
  <div class="container testimonial-slider">
    <div class="slides text-white" :style="slideStyle">
      <div v-for="(testimonial, index) in infiniteTestimonials" :key="index" class="slide" :class="{ 'highlighted-slide': index === currentIndex }">
        <div class="slide-content">
          {{ testimonial.text }}
        </div>
        <div class="slide-author">
          <span class="author-name">{{ testimonial.author }}</span>
        </div>
      </div>
    </div>
    <span class="prev-btn" @click="prevSlide" :disabled="currentIndex === infiniteTestimonials.length - 1">
      <div class="span-slide">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      </div>
    </span>
    <span class="next-btn" @click="nextSlide" :disabled="currentIndex === infiniteTestimonials.length + 1">
      <div class="span-slide">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
      </div>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      testimonials: [
        {
          text: "Estamos muito entusiasmados com o potencial da plataforma da Freedom. Embora ainda estejamos na fase inicial de testes, já percebemos como ela pode ser um divisor de águas para nossa operação. A centralização de múltiplas IAs em uma interface simples e acessível é algo realmente inovador. A facilidade de integração e a forma como ela torna acessível a criação de conteúdo e automação de processos nos dá uma visão clara de como isso pode ser amplamente implementado na nossa empresa no futuro.",
          author: "Juliano Trisca, Regional VP slack sales",
        },
        {
          text: "Testar a plataforma da Freedom nos abriu os olhos para o que pode ser o futuro das nossas operações. Ainda estamos avaliando como implementar isso a longo prazo, mas já conseguimos ver o quão inovadora é a proposta. A Freedom simplifica o uso das tecnologias mais recentes e oferece um ambiente intuitivo para qualquer pessoa, independentemente do nível técnico, criar conteúdo de alta qualidade. É definitivamente uma solução que estamos considerando para o próximo passo em nossa empresa.",
          author: "Mike Allan, Co-founder, Atar b2b adquirida pela Porto Seguro",
        },
        {
          text: "Estamos muito entusiasmados com o potencial da plataforma da Freedom. Embora ainda estejamos na fase inicial de testes, já percebemos como ela pode ser um divisor de águas para nossa operação. A centralização de múltiplas IAs em uma interface simples e acessível é algo realmente inovador. A facilidade de integração e a forma como ela torna acessível a criação de conteúdo e automação de processos nos dá uma visão clara de como isso pode ser amplamente implementado na nossa empresa no futuro.",
          author: "Juliano Trisca, Regional VP slack sales",
        }
      ]
    };
  },
  computed: {
    infiniteTestimonials() {
      return [...this.testimonials,...this.testimonials,...this.testimonials]; // Duplicate the testimonials array
    },
    slideStyle() {
      return {
        transform: `translateX(${this.slideWidth}%)`,
        transition: 'transform 0.5s ease-in-out'
      };
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.slideWidth = document.querySelector('.slide').offsetWidth;
    });
    this.nextSlide();
  },
  methods: {
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % (this.infiniteTestimonials.length);
    },
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1) % (this.infiniteTestimonials.length);
    }
  }
};
</script>

<style scoped>
.testimonial-slider {
  position: relative;
  margin: auto;
  overflow: hidden;
  margin: 140px 0px;
}

.slides {
  display: flex;
  justify-content: center;
}

.slide {
  margin: 35px;
  min-width: 40%;
  box-sizing: border-box;
  padding: 20px;
  text-align: center;
  padding: 40px;
  gap: 10px;
  border-radius: 30px;
  border: 1px solid #3F3F3F;
  backdrop-filter: blur(2px);
  transform: scale(1);
  transition: transform 0.5s ease;
}

.highlighted-slide {
  transform: scale(1.1);
  z-index: 1;
}

.slide-content {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 10px;
}

.slide-author {
  font-size: 14px;
  color: #666;
}

.author-name {
  font-weight: bold;
}

.author-title {
  font-size: 12px;
  color: #999;
}

.prev-btn, .next-btn {
  position: absolute;
  top: 45%;
  background-color: #fbd016;
  border-radius: 40px;
  cursor: pointer;
  z-index: 10;
  transition: all 0.6s ease;
  border: none;
}
.span-slide{
  width: 44px;
  height: 44px;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.prev-btn:hover , .next-btn:hover {
  transform: scale(1.2);
}

.prev-btn {
  left: 26%;
}

.next-btn {
  right: 26%;
}
</style>