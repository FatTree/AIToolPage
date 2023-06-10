<script setup>

const cardArr = [
  {
    imgUrl:
      "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/tool1.png?raw=true",
    imgAlt: "AI工具一",
    titleName: "Chatbot Builder",
    description:
      "建立智能化的聊天機器人，解答常見問題、提供客戶支援、收集反饋等。",
    modelName: "卡卡",
    hashTag: "#聊天"
  },
  {
    imgUrl:
      "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/tool2.png?raw=true",
    imgAlt: "AI工具",
    titleName: "Image Recognition Platform",
    description: "專業的圖像識別平台，識別圖像、分類、標記等。",
    modelName: "杰杰",
    hashTag: "#影像辨識"
  },
  {
    imgUrl:
      "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/tool3.png?raw=true",
    imgAlt: "Language Translation API",
    titleName: "Language Translation API",
    description: "專業的語言翻譯 API，實現文本翻譯功能，支援多種格式的文本。",
    modelName: "琪琪",
    hashTag: "#翻譯"
  },
  {
    imgUrl:
      "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/tool4.png?raw=true",
    imgAlt: "Sentiment Analysis API",
    titleName: "Sentiment Analysis API",
    description: "自動識別文本中的情感傾向，包括正向、負向和中性等。",
    modelName: "昊昊",
    hashTag: "#行銷"
  },
  {
    imgUrl:
      "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/tool5.png?raw=true",
    imgAlt: "Fraud Detection Platform",
    titleName: "Fraud Detection Platform",
    description: "預防詐騙活動，適用於銀行、金融、電商等。",
    modelName: "卡卡",
    hashTag: "#客服"
  },
  {
    imgUrl:
      "https://github.com/hexschool/2022-web-layout-training/blob/main/2023web-camp/tool6.png?raw=true",
    imgAlt: "Voice Assistant SDK",
    titleName: "Voice Assistant SDK",
    description:
      "通過語音控制應用程式、設備，實現多種功能，例如播放音樂、查詢天氣、發送信息等。",
    modelName: "杰杰",
    hashTag: "#生產力"
  }
];
</script>

<template>
  <div class="manu">
    <div class="MaxW">
      <h1 class="TC-Display03 TC-Blob menuTitle">這些超酷的應用，都來自 AI工具王</h1>
      <div class="search">
        <div class="material-icons search__icon">search</div>
        <input type="text" placeholder="輸入關鍵字搜尋" class="search__input">
      </div>
      <div class="filterBox">
        <button class="filter">
          篩選
          <span class="material-icons">filter_alt</span>
        </button>
        <div class="filterBox__center">
          <div class="filterBtn filterBtn--selected">全部</div>
          <div class="filterBtn">聊天</div>
          <div class="filterBtn">影像辨識</div>
          <div class="filterBtn">翻譯</div>
          <div class="filterBtn">行銷</div>
          <div class="filterBtn">客服</div>
          <div class="filterBtn">生產力</div>
        </div>
        <button class="filter">
          由新到舊
          <span class="material-icons">expand_more</span>
        </button>
      </div>
      <ul id="cardListUl" class="cardList"> 
        <li v-for="(item, key) in cardArr" :key="key" class="card">
          <div class="card__pic">
            <img :src=item.imgUrl :alt=item.imgAlt class="img">
          </div>
          <div class="card__content">
            <h4 class="card__content__title">{{item.titleName}}</h4>
            <p class="card__content__description">
              {{item.description}}
            </p>
          </div>
          <div class="card__box">
            <span class="TCBodyBlob">AI 模型</span>
            <span class="TCBodyRagular">{{item.modelName}}</span>
          </div>
          <div class="card__box">
            <span class="TCBodyRagular">{{item.hashTag}}</span>
            <span class="material-icons share">share</span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../assets/main.module.scss';

.manu {
  background-color: #fff;
  border-radius: 160px;
  color: $Black100;
  padding: 160px 90px;
  max-width: 1920px;
  margin: 0 auto;
}

.menuTitle {
  margin-bottom: 80px;
  text-align: center;
}

.search {
  position: relative;

  &__icon {
    position: absolute;   
    top: 17px;
    left: 43px; 
    font-size: 21px;
    color: $Black60;
  }

  &__input {
    border-radius: 16px;
    border: none;
    width: 100%;
    padding: 20px 76px;
    background-color: $Black20;
    margin-bottom: 24px;

    &::placeholder {
      color: $Black60;
      font-weight: $Reg-FW;
      @include TC-Font(16px, 1.5, $Black);
    }

    &:focus {
      outline: none;
    }
    
  }
}

@mixin filterHover {
  background-color: $Black20;
  color: $Black100;
  font-weight: $Blob-FW;
}

.filterBox {
  display: flex;
  justify-content: space-between;
  align-items: center;

  .filter {
    @include TC-Font(16px, 1.5, $Black);
    color: $Black100;
    background-color: $Black0;
    border: 1px solid $Black20;
    border-radius: 16px;
    cursor: pointer;
    padding: 20px 40px;

    .material-icons {
      font-size: 17px;
      margin-left: 14px;
    }
  }

  &__center {
    display: flex;
    width: 100%;
    overflow: hidden;
    .filterBtn {
      @include TC-Font(16px, 1.5, $Black);
      font-weight: $Reg-FW;
      padding: 8px 16px;
      background-color: $Black0;
      border-radius: 16px;
      color: $Black60;
      cursor: pointer;
      margin-right: 10px;

      &--selected, &:hover {
        @include filterHover;
      }
    }

  }
}
.cardList {
  // width: 1350px;
  display: flex;
  flex-wrap: wrap;
  margin: 0 auto;
  justify-content: space-between;

  .card {
    border: 1px solid $Black20;
    width: 416px;
    border-radius: 16px;
    overflow: hidden;
    margin-top: 24px;
    &:hover {
      cursor: pointer;
    }

    &__pic {
      width: 416px;
      height: 312px;
      overflow: hidden;
      > img {
        display: block;
        &:hover {
          transform: scale(1.2);
          transition: 1s;
        }
      }
    }

    &__content {
      padding: 20px 32px;
      height: 78px;

      &__title {
        @include TC-Heading06-Blob();
        margin: 0 0 12px;
        flex-grow: 1;
      }
      &__description {
        @include TC-Small-Regular();
        // height: 42px;
        margin: 0;
      }
    }

    &__box {
      border-top: 1px solid $Black20;
      padding: 20px 32px;
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;

      > .TCBodyBlob {
        @include TC-Body-Blod;
      }

      > .TCBodyRagular {
        @include TC-Body-Regular;
      }

      > .share {
        @include icon24;
      }
    }
  }
}

</style>
