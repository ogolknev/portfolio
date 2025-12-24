<script setup lang="ts">
import ProjectCard from "@/components/ProjectCard.vue";
import ServiceCard from "@/components/ServiceCard.vue";

const services = [
  {
    title: "Веб-приложения и сайты",
    description:
      "Создание и полный дэплой сайтов и веб-приложений. От лэндингов до сложных SPA с базами данных.",
    stack: [
      "Vue",
      "TailwindCSS",
      "Node.js/Bun",
      "FastAPI",
      "PostgreSQL",
      "Docker",
    ],
    minPrice: 10000,
  },
  {
    title: "Telegram-боты",
    description:
      "Автоматизация, парсинг, интеграции с API. Боты для продаж, аналитики, автоматизации задач.",
    stack: ["grammY", "aiogram", "Docker"],
    minPrice: 3000,
  },
  {
    title: "Автоматизации и ИИ интеграции",
    description:
      "Автоматизация рутинных процессов. Интеграция нейросетей и ИИ-моделей. Системы для обработки данных и работы с внешними API.",
    stack: ["Python", "OpenAI", "LangChain"],
    minPrice: 5000,
  },
];

const projects = [
  {
    title: "Онлайн школа",
    description:
      "Платформа для онлайн-курсов с управлением контентом. Полнофункциональное веб-приложение для обучения.",
    stack: ["Vue", "Strapi CMS", "PostgreSQL"],
    link: "https://github.com/ogolknev/online-school",
  },
  {
    title: "Мессенджер Phialka",
    description:
      "Мессенджер для самохостинга. Открытый исходный код. Веб-клиент с функционалом реального времени.",
    stack: ["Vue", "WebSocket", "FastAPI", "PostgreSQL"],
    link: "https://github.com/ogolknev/phialka-messenger-web",
  },
  {
    title: "Лэндинг Taskflow",
    description:
      "Показательный лэндинг с высокой конверсией. Оптимизированный UI/UX и быстрая загрузка.",
    stack: ["Vue", "NuxtUI"],
    link: "https://github.com/ogolknev/taskflow-landing",
  },
  {
    title: "Автоматизация нарезки клипов",
    description:
      "Telegram-бот для автонарезки клипов из видео. Автоматическое создание контента для TikTok, Reels, Shorts.",
    stack: ["Python", "ffmpeg", "grammY", "Docker", "n8n", "Groq"],
  },
  {
    title: "A1-to-indexes",
    description:
      "Вспомогательный инструмент для разработчиков работающих с таблицами.",
    stack: ["Native JS"],
    link: "https://github.com/ogolknev/a1-to-indexes",
  },
];
</script>

<template>
  <div class="space-y-16">
    <section id="hero" class="py-16 space-y-6">
      <div>
        <h1 class="text-3xl font-normal">[-.-] Никита Оголкнев</h1>
        <h2 class="text-xl text-neutral-500 font-mono">Fullstack Developer</h2>
      </div>

      <p class="font-mono text-lg">
        <span class="text-neutral-500 text-lg font-sans">></span> Создаю
        масштабируемые веб-приложения, Telegram-боты и системы автоматизации.
        Пишу код как книгу — чтобы его мог понять и поддерживать каждый.
      </p>

      <div>
        <a href="#projects">
          <button class="mr-5" type="button"># Смотреть проекты</button>
        </a>
        <a href="#contact">
          <button type="button"># Написать мне</button>
        </a>
      </div>

      <p class="font-mono">
        <span class="text-neutral-500 text-lg font-sans">Стек: </span
        >JavaScript/TypeScript, Vue, Python, FastAPI, Bun + Hono, PostgreSQL
      </p>
    </section>

    <section id="about" class="space-y-6">
      <h2 class="text-3xl font-normal">[o.o] Обо мне</h2>

      <p class="font-mono text-lg">Привет, я Никита!</p>

      <p class="font-mono text-neutral-400">
        За 2 года я помог десяткам клиентов превратить идеи в рабочие продукты.
        Я люблю решать сложные задачи, учиться новому и делать всё основательно.
      </p>

      <p class="font-mono text-neutral-400">
        Для меня главное в коде — эстетика и эффективность. Я обожу писать код
        как книгу, чтобы потом его мог кто угодно читать и всё понимать. И люблю
        оптимизации.
      </p>

      <p class="font-mono text-neutral-400">
        Каждый проект — это не просто набор строк кода, а продуманная
        архитектура, которая будет работать быстро и легко расширяться в
        будущем.
      </p>
    </section>

    <section id="services">
      <h2 class="text-3xl font-normal mb-10">[~.~] Услуги</h2>

      <div class="space-y-8 mb-8">
        <ServiceCard
          v-for="service in services"
          :key="service.title"
          :title="service.title"
          :description="service.description"
          :stack="service.stack"
          :minPrice="service.minPrice" />
      </div>

      <p>Готов обсудить ваш проект и найти оптимальное решение.</p>
    </section>

    <section id="projects">
      <h2 class="text-3xl font-normal mb-10">[+.+] Проекты</h2>

      <div class="space-y-8 mb-8">
        <ProjectCard
          v-for="project in projects"
          :key="project.title"
          :title="project.title"
          :description="project.description"
          :stack="project.stack"
          :link="project.link" />
      </div>
    </section>

    <section id="contact">
      <h2 class="text-3xl font-normal mb-10">[x.x] Контакты</h2>

      <p class="font-mono">
        <span class="text-neutral-500">Email:</span>
        <a href="mailto:ogolknevnv@gmail.com">ogolknevnv@gmail.com</a>
      </p>
      <p class="font-mono">
        <span class="text-neutral-500">Telegram:</span>
        <a href="https://t.me/ogolknev">@ogolknev</a>
      </p>
      <p class="font-mono">
        <span class="text-neutral-500">GitHub:</span>
        <a href="https://github.com/ogolknev">ogolknev</a>
      </p>
      <p class="font-mono mt-8 text-lg">
        Напишите мне, если у вас есть проект или вопросы. Готов обсудить детали
        и найти лучшее решение.
      </p>
    </section>
  </div>
</template>
