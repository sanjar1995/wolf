<script setup>
import Typography from "@/components/UI/Typography.vue";
const resultItems = [ 
  {
    icon: "🏆",
    text: "Сформулируете лучшее предложение на вашем рынке",
  },
  {
    icon: "☑️",
    text: "Замотивируете менеджеров и научитесь правильно их контролировать",
  },
  {
    icon: "🎯",
    text: "Внедрите системный найм и обучение персонала",
  },
  {
    icon: "🎓",
    text: "Наймете и обучите мощного руководителя",
  },
  {
    icon: "💻",
    text: "ВнедритеCRM-систему",
  },
  {
    icon: "💯",
    text: "Научитесь искать ТОПовых продавцов на рынке",
  },
  {
    icon: "👨‍💻",
    text: "Внедрите скрипты и все передовые технологии продаж",
  },
  {
    icon: "💸",
    text: "Создадите конкурентную среду в отделе продаж. Замотивируете менеджеров развиваться и перевыполнять планы",
  },
];
</script>
<template>
  <section class="result-info">
    <div class="container">
      <Typography tagName="h2" class="result-info__title title">
        В результате обучения вы и ваша команда
      </Typography>
      <Typography tagName="p" class="result-info__txt">
        Это минимум внедрений, которые вы сделаете за время прохождения
        программы #реальныйотзыв
      </Typography>
      <div class="result-info__content">
        <div class="result-info__item" v-for="item in resultItems" :key="item">
          <span class="result-info__item-icon">{{ item.icon }}</span>
          <p class="result-info__item-txt ellipsis">
            {{ item.text }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
