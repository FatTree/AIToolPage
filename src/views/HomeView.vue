<script setup>
import Menu from '../components/Manu.vue'

const intros = [
  {
    icon: "flash_on",
    title: "快速",
    content: "我們先進的推理基礎設施提供了極短的響應時間，讓你的產品服務不間斷。"
  },
  {
    icon: "auto_awesome",
    title: "靈活",
    content: "我們的服務可以根據您的需求進行靈活調整，同時還可以滿足不同項目和預算的需求。"
  },
  {
    icon: "library_add",
    title: "擴充",
    content: "我們的服務支持多種擴充選項，可以滿足您的不斷增長的 AI 需求。"
  }
];

const recomands = [
  {
    content: "非常喜歡 AI工具王 提供的 AI 模型租賃服務，使用起來非常方便，而且效果非常好。對於我們公司的業務來說，這個服務非常重要，因為我們需要大量的數據進行分析和預測，AI工具王 提供的 AI 模型能夠幫助我們節省大量時間和成本，實在是太棒了！",
    imgUrl: "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/avatar3.png?raw=true",
    name: "陳小姐",
    company: "ABC科技有限公司"
  },
  {
    content: "作為一家醫療器材公司，我們非常關注人工智能技術的應用，而 AI工具王 提供的 AI 模型租賃服務為我們帶來了很大的幫助。我們使用 AI工具王 的模型進行醫學影像分析和預測，這些模型非常精確，能夠幫助我們更好地診斷病情，提高治療效果。感謝 AI工具王 團隊的辛勤工作！",
    imgUrl: "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/avatar1.png?raw=true",
    name: "劉小姐",
    company: "XYZ 醫療器材有限公司"
  }
  ,
  {
    content: "我們銀行一直在尋找能夠幫助我們提高風險控制和客戶服務的解決方案，而 AI工具王 提供的 AI 模型租賃服務正好滿足了我們的需求。我們使用 AI工具王 的模型進行客戶信用評估和詐騙檢測等任務，這些模型非常準確，能夠幫助我們更好地控制風險，提高客戶滿意度。非常感謝 AI工具王 團隊的支持！",
    imgUrl: "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/avatar2.png?raw=true",
    name: "黃先生",
    company: "EFG 銀行"
  }
];

</script>

<template>
  <main>
    <div class="MaxW">
      <h1 class="TC-Display02 TC-Blob">透過<br>AI 工具王的<br>強大模型<br>讓您的業務更聰明</h1>
      <div class="TC-Heading06 TC-Blob TC-Btn">開始使用</div>
      <div class="decoBox d-flex">
        <img class="deco" src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/deco.png?raw=true" alt="">
        <img class="deco" src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/deco.png?raw=true" alt="">
        <img class="deco" src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/deco.png?raw=true" alt="">
      </div>
      <div class="service">
        <div class="d-flex">
          <h3 class="service__title1 TC-Heading03 TC-Blob">我們的服務</h3>
          <h3 class="service__title2 TC-Heading01 TC-Blob">我們相信透過 AI 技術，<br>包括圖像識別、自然語言處理和機器翻譯等，讓您更快、更準確地做出決策。</h3>
        </div>
        <div class="d-flex TC-Box">
          <div v-for="(item, key) in intros" class="intro" :key="key">
            <span class="material-icons intro__icon">
              <span class="material-symbols-outlined">
                {{item.icon}}
              </span>
            </span>
            <h4 class="intro__title TC-Heading03 TC-Blob">{{ item.title }}</h4>
            <p class="intro__content TC-Body TC-Regular">{{ item.content }}</p>
          </div>
        </div>
      </div>
      <div class="sponsor">
        <h3 class="TC-Heading03 TC-Blob">來自合作夥伴</h3>
        <div class="sponsor__logos">
          <div class="mask"></div>
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise1.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise2.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise3.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise4.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise5.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise6.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise7.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise8.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise9.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise6.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise11.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise12.png?raw=true" alt="">
          <img src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/enterprise7.png?raw=true" alt="">
        </div>
      </div>
      <div class="d-flex">
        <div v-for="(item, key) in recomands" class="recomand" :key="key">
          <div class="recomand__top">
            <div class="recomand__top__starts material-icons">
              <span class="material-symbols-outlined">star</span>
            </div>
            <div class="recomand__top__starts material-icons">
              <span class="material-symbols-outlined">star</span>
            </div>
            <div class="recomand__top__starts material-icons">
              <span class="material-symbols-outlined">star</span>
            </div>
            <div class="recomand__top__starts material-icons">
              <span class="material-symbols-outlined">star</span>
            </div>
            <div class="recomand__top__starts material-icons">
              <span class="material-symbols-outlined">star</span>
            </div>
            <div class="TC-Body TC-Regular">
              {{ item.content }}
            </div>
          </div>
          <div class="recomand__head">
            <img :src=item.imgUrl alt="avd">
            <div>
              <p class="TC-Body TC-Blob">{{ item.name }}</p>
              <p class="TC-Small TC-Regular">{{ item.company }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="manu">
      <Menu />
    </div>
    <div class="bottomBox MaxW">
      <div class="bottomBox__top">
        <h3 class="TC-Heading01 TC-Blob">現在就來建立屬於你的服務吧</h3>
        <div class="TC-Heading06 TC-Blob TC-Btn">
          開始使用
          <span class="material-icons intro__icon">
            <span class="material-symbols-outlined">call_made</span>
          </span>
        </div>
      </div>
      <div class="bottomBox__btm">
        <h3 class="TC-Display03 TC-Blob">首頁<br>定價</h3>
        <img class="logo" src="https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/logo.png?raw=true" alt="">
      </div>
    </div>
  </main>
</template>
<style lang="scss" scoped>
@import '../assets/main.module.scss';

.TC-Btn {
  margin-top: 40px;
  border: 1px solid $Black0;
  cursor: pointer;
}

.decoBox {
  justify-content: end;
  padding-bottom: 160px;
  > .deco {
    width: 180px;
    height: 180px;
  }
}

.service {
  &__title1 {
    width: 414px;
  }

  &__title2 {
   width: 856px; 
  }

  
  .intro {
    border: 1px solid $Black80;
    border-radius: 16px;
    width: 416px;
    height: 366px;
    padding: 80px 40px;
    margin-top: 80px;
    margin-bottom: 160px;
  
    &:not(:first-child) {
      margin-left: 24px;
    }
  
    &__icon {
      font-size: 80px;
      
    }
  
    &__title {
      padding: 20px 0;
    }
  
    &__content {
  
    }
  }
}

.sponsor {

  &__logos {
    margin-bottom: 160px;
    position: relative;
    text-align: center;
    padding-top: 80px;

    .mask {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(to right, black, transparent 30%, transparent 70%, black);
    }

    img {
      height: 40px;
      margin: 20px 20px 0 0;
    }
  }
}

.recomand {
  border-radius: 16px;
  width: 416px;
  height: 400px;
  padding: 40px;
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
  margin-bottom: 160px;
  background: rgba(255, 255, 255, 0.08);

  &:not(:first-child) {
    margin-left: 24px;
  }

  &__top {
    &__starts {
      font-size: 16px;
      padding: 0 7px 22px 0;
    }
  }

  &__head {
    display: flex;

    img {
      display: inline-block;
      width: 48px;
      height: 48px;
      border-radius: 50%;
      margin-right: 16px;
    }
  }
}

.bottomBox {
  
  &__top {
    text-align: center;
    padding: 158px 0;
    border-bottom: 1px solid $Black0;
  }

  &__btm {
    padding: 100px 0;
    border-bottom: 1px solid $Black0;
    display: flex;
    justify-content: space-between;

    > .logo {
      width: 245px;
      height: 40px;
    }
  }
}

@media screen and (max-width: 767px) {
  .service {
    .TC-Box {
      display: block;

      .intro {
        width: 100%;
        
        &:not(:first-child) {
          margin-left: 0px;
        }
      }
    }

      
  }
}
</style>