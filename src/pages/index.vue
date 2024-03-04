<script setup>
  const pageTitle = 'Home';
  useHead({
    title: pageTitle,
  });
</script>

<template>
  <div class="app home">
    <Navbar />
    <Header />
    <Section anchor="logo-nazwa">
      <div class="logo-nazwa">
        <NuxtImg src="/images/logo/logo.png" /><span>Przyjazny Powiat</span>
      </div>
    </Section>
    <Section anchor="About" title="O nas" grid="2">
      <div class="about__content">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus consequuntur, quos commodi quasi doloremque 
          cupiditate repellendus illum? Aliquam deserunt, debitis blanditiis, dolores porro veniam rem minima ea beatae, repudiandae maiores.
        </p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus consequuntur, quos commodi quasi doloremque 
          cupiditate repellendus illum? Aliquam deserunt, debitis blanditiis, dolores porro veniam rem minima ea beatae, repudiandae maiores.
        </p>
      </div>
      <div class="about__content">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus consequuntur, quos commodi quasi doloremque 
          cupiditate repellendus illum? Aliquam deserunt, debitis blanditiis, dolores porro veniam rem minima ea beatae, repudiandae maiores.
        </p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus consequuntur, quos commodi quasi doloremque 
          cupiditate repellendus illum? Aliquam deserunt, debitis blanditiis, dolores porro veniam rem minima ea beatae, repudiandae maiores.
        </p>
      </div>
    </Section>
    <Section anchor="kandydaci" title="Kandydaci" grid="4">
      <div class="kandydaci-top">
        <span></span>
        <h3>Okręg I - Brodnica</h3>
      </div>
      <a v-for="item in kandydaci" :key="item.title" class="kandydaci__card" :href="`#${item.photo}`">
        <div class="kandydaci__card--photo">
          <NuxtImg :src="`/images/photos/${item.photo}.png`"></NuxtImg>
        </div>
        <div class="kandydaci__card--name">
          <p>{{ item.name }}</p>
        </div>
        <div class="kandydaci__card--surname">
          <p>{{ item.surname }}</p>
        </div>
      </a>
    </Section>
    <Section v-for="item in kandydaci" :anchor="item.photo" :key="item.title" class="kandydaci__opis" grid="2">
      <div class="lewo">
      <div class="kandydaci__opis--photo">
          <NuxtImg :src="`/images/photos/${item.photo}.png`"></NuxtImg>
        </div>
        <div class="kandydaci__opis--name">
          <p>{{ item.name + " " + item.surname}} </p>
        </div>
        <div class="contact">
          <div class="kandydaci__opis--phone">
            <p>{{ item.phone }}</p>
          </div>
          <div class="kandydaci__opis--mail">
            <p>{{ item.mail }}</p>
          </div>
      </div>
      </div>
      <div class="prawo">
        <div class="kandydaci__opis--description">
          <p>{{ item.description }}</p>
        </div>
      
      </div>
    </Section>
  </div>
</template>

<script>
  export default {
    name: 'home',
    data() {
      return {
        kandydaci: [
          {
            photo: 'pawelszramka',
            name: 'Paweł',
            surname: 'Szramka',
            description:'Chcę, wspólnie z Wami, zmieniać nasze otoczenie na lepsze. Możemy sprawić, że powiat brodnicki będzie wspaniałym miejscem do życia. Warto wykorzystać atuty naszych okolic, pokazywać mocne strony i pracować nad wszystkimi elementami, które hamują nasz rozwój. Możemy zrobić to skutecznie, stawiając na współpracę, otwarcie na nowe pomysły i wspólną wizję przyszłości. Brodniczanin, szczęśliwy mąż, poseł na Sejm RP VIII i IX kadencji, logistyk z wykształcenia, były żołnierz',
            phone:'111 111 111',
            mail: 'pawełszramka@gmail.com',
          },
          {
            photo: 'pawelszramka',
            name: 'Paweł',
            surname: 'Szramka',
            description:'Chcę, wspólnie z Wami, zmieniać nasze otoczenie na lepsze. Możemy sprawić, że powiat brodnicki będzie wspaniałym miejscem do życia. Warto wykorzystać atuty naszych okolic, pokazywać mocne strony i pracować nad wszystkimi elementami, które hamują nasz rozwój. Możemy zrobić to skutecznie, stawiając na współpracę, otwarcie na nowe pomysły i wspólną wizję przyszłości. Brodniczanin, szczęśliwy mąż, poseł na Sejm RP VIII i IX kadencji, logistyk z wykształcenia, były żołnierz',
            phone:'111 111 111',
            mail: 'pawełszramka@gmail.com',
          },
          {
            photo: 'pawelszramka',
            name: 'Paweł',
            surname: 'Szramka',
            description:'Chcę, wspólnie z Wami, zmieniać nasze otoczenie na lepsze. Możemy sprawić, że powiat brodnicki będzie wspaniałym miejscem do życia. Warto wykorzystać atuty naszych okolic, pokazywać mocne strony i pracować nad wszystkimi elementami, które hamują nasz rozwój. Możemy zrobić to skutecznie, stawiając na współpracę, otwarcie na nowe pomysły i wspólną wizję przyszłości. Brodniczanin, szczęśliwy mąż, poseł na Sejm RP VIII i IX kadencji, logistyk z wykształcenia, były żołnierz',
            phone:'111 111 111',
            mail: 'pawełszramka@gmail.com',
          },
          {
            photo: 'pawelszramka',
            name: 'Paweł',
            surname: 'Szramka',
            description:'Chcę, wspólnie z Wami, zmieniać nasze otoczenie na lepsze. Możemy sprawić, że powiat brodnicki będzie wspaniałym miejscem do życia. Warto wykorzystać atuty naszych okolic, pokazywać mocne strony i pracować nad wszystkimi elementami, które hamują nasz rozwój. Możemy zrobić to skutecznie, stawiając na współpracę, otwarcie na nowe pomysły i wspólną wizję przyszłości. Brodniczanin, szczęśliwy mąż, poseł na Sejm RP VIII i IX kadencji, logistyk z wykształcenia, były żołnierz',
            phone:'111 111 111',
            mail: 'pawełszramka@gmail.com',
          },
          {
            photo: 'pawelszramka',
            name: 'Paweł',
            surname: 'Szramka',
            description:'Chcę, wspólnie z Wami, zmieniać nasze otoczenie na lepsze. Możemy sprawić, że powiat brodnicki będzie wspaniałym miejscem do życia. Warto wykorzystać atuty naszych okolic, pokazywać mocne strony i pracować nad wszystkimi elementami, które hamują nasz rozwój. Możemy zrobić to skutecznie, stawiając na współpracę, otwarcie na nowe pomysły i wspólną wizję przyszłości. Brodniczanin, szczęśliwy mąż, poseł na Sejm RP VIII i IX kadencji, logistyk z wykształcenia, były żołnierz',
            phone:'111 111 111',
            mail: 'pawełszramka@gmail.com',
          },
          {
            photo: 'pawelszramka',
            name: 'Paweł',
            surname: 'Szramka',
            description:'Chcę, wspólnie z Wami, zmieniać nasze otoczenie na lepsze. Możemy sprawić, że powiat brodnicki będzie wspaniałym miejscem do życia. Warto wykorzystać atuty naszych okolic, pokazywać mocne strony i pracować nad wszystkimi elementami, które hamują nasz rozwój. Możemy zrobić to skutecznie, stawiając na współpracę, otwarcie na nowe pomysły i wspólną wizję przyszłości. Brodniczanin, szczęśliwy mąż, poseł na Sejm RP VIII i IX kadencji, logistyk z wykształcenia, były żołnierz',
            phone:'111 111 111',
            mail: 'pawełszramka@gmail.com',
          },
          {
            photo: 'pawelszramka',
            name: 'Paweł',
            surname: 'Szramka',
            description:'Chcę, wspólnie z Wami, zmieniać nasze otoczenie na lepsze. Możemy sprawić, że powiat brodnicki będzie wspaniałym miejscem do życia. Warto wykorzystać atuty naszych okolic, pokazywać mocne strony i pracować nad wszystkimi elementami, które hamują nasz rozwój. Możemy zrobić to skutecznie, stawiając na współpracę, otwarcie na nowe pomysły i wspólną wizję przyszłości. Brodniczanin, szczęśliwy mąż, poseł na Sejm RP VIII i IX kadencji, logistyk z wykształcenia, były żołnierz',
            phone:'111 111 111',
            mail: 'pawełszramka@gmail.com',
          },
          {
            photo: 'pawelszramka',
            name: 'Paweł',
            surname: 'Szramka',
            description:'Chcę, wspólnie z Wami, zmieniać nasze otoczenie na lepsze. Możemy sprawić, że powiat brodnicki będzie wspaniałym miejscem do życia. Warto wykorzystać atuty naszych okolic, pokazywać mocne strony i pracować nad wszystkimi elementami, które hamują nasz rozwój. Możemy zrobić to skutecznie, stawiając na współpracę, otwarcie na nowe pomysły i wspólną wizję przyszłości. Brodniczanin, szczęśliwy mąż, poseł na Sejm RP VIII i IX kadencji, logistyk z wykształcenia, były żołnierz',
            phone:'111 111 111',
            mail: 'pawełszramka@gmail.com',
          },
          
        ],
        
      }
    },
  }
</script>