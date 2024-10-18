<template>
  <div class="container testimonial-slider">
    <div class="slides text-white" :style="slideStyle">
      <div v-for="(testimonial, index) in infiniteTestimonials" :key="index" class="slide"
        :class="{ 'highlighted-slide': (index) === currentIndex }">
        <div class="slide-content">
          "{{ testimonial.text }}"
        </div>
        <div class="slide-author">
          <span class="author-name">{{ testimonial.author }}</span>
        </div>
      </div>
    </div>
    <span class="prev-btn" @click="prevSlide">
      <div class="span-slide">
        <span class="content-button" aria-hidden="true"><</span>
      </div>
    </span>
    <span class="next-btn" @click="nextSlide">
      <div class="span-slide">
        <span class="content-button" aria-hidden="true">></span>
      </div>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      slideWidth: 0,
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
      return [...this.testimonials];
    },
    slideStyle() {
      return {
        transform: `translateX(${(this.currentIndex - 1) * -594}px)`, // Adjust based on the current index
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
      if (this.currentIndex === this.infiniteTestimonials.length - 1) {
        this.currentIndex = 0;
      } else {
        this.currentIndex++;
      }
    },
    prevSlide() {
      if (this.currentIndex === 0) {
        this.currentIndex = 2;
      } else {
        this.currentIndex--;
      }
    },
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
  min-width: 524px;
  min-height: 390px;
  box-sizing: border-box;
  padding: 20px;
  text-align: center;
  padding: 40px;
  gap: 13px;
  border-radius: 30px;
  background:#FFFFFF0A !important;
  border: 1px solid #3F3F3F;
  backdrop-filter: blur(2px);
  transition: transform 0.5s ease;
}

.highlighted-slide {
  transform: scale(1.1);
  z-index: 1;
}

.slides {
  display: flex;
  justify-content: center;
  transform: translateX(50%);
}

.prev-btn,
.next-btn {
  position: absolute;
  top: 50%;
  width: 50px;
  height: 50px;
  background-color: #fbd016;
  border-radius: 40px;
  cursor: pointer;
  z-index: 10;
  transition: all 0.6s ease;
  border: none;
  transform: translateY(-50%);
  color: #000;
  align-items: center;
  justify-content: center;
  display: flex;
}

.prev-btn {
  left: 25%;
}

.next-btn {
  right: 25%;
}

.span-slide span {
  font-size: 2em;
  text-align: center;
}

.slide-content {
  font-family: Open Sans;
  font-size: 23.77px;
  font-style: italic;
  font-weight: 400;
  line-height: 30.9px;
  text-align: left;
  margin-bottom: 42px;
}
.slide-author {
  font-family: Open Sans;
  font-size: 23.77px;
  font-weight: 700;
  line-height: 30.9px;
  text-align: left;
}
</style>