<template>
  <!-- <div class="sign contentContainer">
    <div class="">This page is working in progress.</div>
    <div class="">Please wait for a while.</div>
    <div class="inProgress"></div>
  </div> -->
  <div class="articleTitleContainer contentContainer">
    <div class="articleTitle">MaskVLA:</div>
    <div class="articleTitle">
      Visual Masking Against Trajectory Overfitting of Vision-Language-Action
      Model
    </div>

    <div class="arthorNameLine">
      <div class="arthorNameContainer">
        <span class="arthorName">anonymous author 1</span
        ><span class="sup">1</span><span class="arthorName">， </span>
      </div>
      <div class="arthorNameContainer">
        <span class="arthorName">anonymous author 2</span
        ><span class="sup">1</span><span class="arthorName">， </span>
      </div>
      <div class="arthorNameContainer">
        <span class="arthorName">anonymous author N</span
        ><span class="sup">N</span><span class="arthorName">， </span>
      </div>
    </div>
    <div class="expression">
      <div class="expressionItem">
        <span class="sup"> * </span
        ><span class="expressionText">Equal Contribution</span>
      </div>
    </div>

    <div class="university">
      <div class="universityContainer">
        <span class="sup"> 1 </span
        ><span class="universityName">anonymous organization </span>
      </div>
    </div>
    <div class="buttonGroup">
      <button class="button" onclick="window.open('/')" type="button">
        <div class="buttonIcon arxivIcon"></div>
        Paper
      </button>
      <button class="button" onclick="window.open('/')" type="button">
        <div class="buttonIcon gitHubIcon"></div>
        Code
      </button>
      <!-- <button
        class="button unfinished"
        onclick="window.alert('Code will be released soon!')"
        type="button"
      >
        <div class="gitHubIcon"></div>
        Code
      </button> -->
      <button class="button" onclick="window.open('/')" type="button">
        <div class="buttonIcon huggingFaceIcon"></div>
        Model
      </button>
    </div>
  </div>
  <div class="videoDisplayContainer contentContainer coverVideo">
    <video muted playsinline loop controls disable-picture-in-picture="true">
      <source src="./assets/mp4/video1.mp4" type="video/mp4" />
    </video>
  </div>
  <div class="articleMainBodyContainer contentContainer">
    <div class="contentMainTitle">Abstract</div>
    <div class="content">
      Vision-Language-Action (VLA) models integrate vision-language
      understanding with executable robot actions, enabling end-to-end learning
      for robot control. However, our empirical analysis reveals that existing
      models exhibit severe trajectory memorization and overfitting when
      finetuned on limited datasets. To guide the model in effectively utilizing
      wrist camera information, we propose MaskVLA, a masking-based fine-tuning
      strategy. By randomly masking a small portion of the main camera’s visual
      information, the model is guided to autonomously learn more fine-grained,
      task-relevant, and effective visual features. This process leads to the
      emergence of robust policies, thereby enhancing the model’s capability to
      tackle complex manipulation tasks and improving its generalization
      performance. Our method has been comprehensively evaluated on RoboTwin
      2.0, achieving an average success rate improvement of 22.9% and 16.5%
      compared to π0 and OpenVLA-OFT, respectively. Furthermore, experiments on
      real-world ALOHA robots also demonstrate the effectiveness of our
      approach. Our project page is https://anonymous.4open.science/w/
      MaskVLA-D31F/.
    </div>

    <!-- <div class="codeSpace">
      <pre>
        
        <code>
@article{ xxxxxxxxxxx, 
  title={titleCodeMode},
  author={ {authore} name list of all authors}, 
  journal = {arXiv preprint arXiv:arxivCODE}, year={2025}, 
}
        </code>
      </pre>
    </div> -->
  </div>
  <div class="articleMainBodyContainer contentContainer">
    <div class="contentImg contentImg1">
      <img src="./assets/pic/pic1.png" alt="image" />
      <div class="introText">
        <span class="bold">Fig. 1.</span> We propose MaskVLA, an improved
        fine-tuning method for multiview VLA frameworks that significantly
        enhances model performance. By randomly masking the primary camera
        input, the method guides the model to learn robust multi-view visual
        features. In both RoboTwin2.0 [5] simulation environments and real-world
        experiments, it demonstrates substantial improvements over OpenVLA-OFT
        [2] across multiple manipulation tasks.
      </div>
    </div>
  </div>
  <div class="videoDisplayGroupContainer contentContainer">
    <div class="coverVideo">
      <video muted playsinline loop controls disable-picture-in-picture="true">
        <source src="./assets/mp4/video1.mp4" type="video/mp4" />
      </video>
    </div>
    <div class="coverVideo">
      <video muted playsinline loop controls disable-picture-in-picture="true">
        <source src="./assets/mp4/video2.mp4" type="video/mp4" />
      </video>
    </div>
  </div>

  <!-- <div class="articleMainBodyContainer contentContainer">
    <div class="contentImg contentImg">
      <img src="./assets/pic/fig2.png" alt="image" />
      <div class="introText">
        <span class="bold">Figure 2:</span> RoboMemory architecture with working
        pipeline and memory mechanisms. (a) Left: The agent’s pipeline. Parallel
        Step Summarizer and Query Generator in Information Processor (1)
        generate updates/queries for Lifelong Embodied Memory (2). These
        memories enable Closed-Loop Planning (3) for tasks like “slice and pick
        up the apple”—the Planner generates plans, while the Critic and memories
        adjust decisions via feedback from visual inputs/results (4). (b) Right:
        Spatial and Semantic memories operate in parallel with isomorphic
        updates. Internally, Spatial memory maintains a
        relevance/similarity-updated KG, and Semantic memory manages a Vector DB
        with analogous logic.
      </div>
    </div>
  </div> -->
  <!-- <div class="forecast contentContainer">
    The rest of paper is comming soon...
  </div> -->
</template>

<script setup lang="ts"></script>

<style scoped>
body {
  /* word setting */
  font-family: "Alibaba-puhui-regular";
}
* {
  /* word-break: normal;
  word-wrap: break-word; */
}
/* font */
@font-face {
  font-family: "Product-sans-black";
  font-display: swap;
  src: url("@/assets/font/ProductSans-Black.ttf") format("truetype");
}
@font-face {
  font-family: "Product-sans-bold";
  font-display: swap;
  src: url("@/assets/font/ProductSans-Bold.ttf") format("truetype");
}
@font-face {
  font-family: "Product-sans-medium";
  font-display: swap;
  src: url("@/assets/font/ProductSans-Medium.ttf") format("truetype");
}
@font-face {
  font-family: "Product-sans-regular";
  font-display: swap;
  src: url("@/assets/font/ProductSans-Regular.ttf") format("truetype");
}
@font-face {
  font-family: "Product-sans-light";
  font-display: swap;
  src: url("@/assets/font/ProductSans-Light.ttf") format("truetype");
}
@font-face {
  font-family: "Product-sans-thin";
  font-display: swap;
  src: url("@/assets/font/ProductSans-Thin.ttf") format("truetype");
}
@font-face {
  font-family: "Alibaba-puhui-regular";
  font-display: swap;
  src: url("@/assets/font/Alibaba-PuHuiTi-Regular.ttf") format("truetype");
}
@font-face {
  font-family: "Alibaba-puhui-medium";
  font-display: swap;
  src: url("@/assets/font/Alibaba-PuHuiTi-Medium.ttf") format("truetype");
}

@font-face {
  font-family: "Alibaba-puhui-heavy";
  font-display: swap;
  src: url("@/assets/font/Alibaba-PuHuiTi-Heavy.ttf") format("truetype");
}
@font-face {
  font-family: "Alibaba-puhui-bold";
  font-display: swap;
  src: url("@/assets/font/Alibaba-PuHuiTi-Bold.ttf") format("truetype");
}
a,
a:active,
a:hover,
a:focus,
a:visited {
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}

.bold {
  font-family: "Product-sans-bold";
}

.contentContainer {
  display: flex;
  flex-direction: column;
  position: relative;
  box-sizing: border-box;
  width: 100%;
  min-width: 960px;
  height: fit-content;
  padding: 5vmax 0;
  background-color: #ffffff;
}
/* .contentContainer:nth-child(even) {
  background-color: #f0f0f0;
}
.contentContainer:nth-child(odd) {
  background-color: #ffffff;
} */

.forecast {
  display: flex;
  height: 50vmax;
  font-family: "Product-sans-bold";
  font-size: 3vmax;
  justify-content: center;
  align-items: center;
  line-height: 1.5;
}
.inProgress {
  display: flex;
  width: 15vmax;
  height: 15vmax;
  background-image: url("@/assets/icon/component/road.png");
  background-size: contain;
  margin-left: 1vmax;
}

.articleTitleContainer {
  padding-top: 5vmax;
}
.articleTitle {
  /* display: flex; */
  /* flex-direction: column; */
  box-sizing: border-box;
  font-family: "Product-sans-bold";
  font-size: 3vmax;
  color: #363636;
  justify-content: center;
  line-height: 1.25;
  text-align: center;
  padding: 0 17.5%;
}

.colorStress {
  display: inline;
  color: #209cee;
}

.arthorNameLine {
  display: flex;
  width: 100%;
  font-family: "Product-sans-regular";
  box-sizing: border-box;
  flex-wrap: wrap;
  padding: 0 20%;
  margin: 2.5vmax 0 0;
  line-height: 1.5;
  font-size: 1.25vmax;
  justify-content: center;
}
.arthorNameContainer {
  display: flex;
  box-sizing: border-box;
  flex-shrink: 0;
  margin-right: 0.5vmax;
}
.arthorName {
  color: #209cee;
}
.sup {
  display: flex;
  vertical-align: top;
  flex-shrink: 0;
  font-size: 60%;
  margin: 0 0.125vmax;
  font-family: "Product-sans-regular";
}
.expression {
  display: flex;
  margin: 0.75vmax 0 0;
  justify-content: center;
}
.expressionItem {
  display: flex;
  box-sizing: border-box;
  flex-shrink: 0;
  margin: 0 0.25vmax;
}
.expressionText {
  font-size: 1vmax;
  font-family: "Product-sans-regular";
}
.university {
  display: flex;
  width: 100%;
  font-family: "Product-sans-regular";
  box-sizing: border-box;
  flex-wrap: wrap;
  padding: 0 25%;
  margin: 0.75vmax 0 0;
  line-height: 1.5;
  font-size: 1.2vmax;
  justify-content: center;
}
.universityContainer {
  display: flex;
  box-sizing: border-box;
  flex-shrink: 0;
  margin-right: 1vmax;
}
.universityName {
  font-family: "Product-sans-regular";
  color: #535353;
}
.buttonGroup {
  display: flex;
  justify-content: center;
  margin: 0.75vmax 0;
}
.button {
  display: flex;
  height: 2vmax;
  justify-content: center;
  align-items: center;
  font-family: "Product-sans-regular";
  border-radius: 1.5vmax;
  border: #363636 solid 0px;
  background-color: #363636;
  color: #ffffff;
  padding: 1.5vmax;
  margin: 0.5vmax;
  font-size: 1vmax;
  cursor: pointer;
}
.button:hover {
  background-color: #474747;
}
.button.unfinished {
  background-color: #707070;
}
.button.unfinished:hover {
  background-color: #808080;
}
.buttonIcon {
  width: 1.5vmax;
  height: 1.5vmax;
  background-size: contain;
  background-repeat: no-repeat;
  margin-right: 0.75vmax;
}
.arxivIcon {
  background-image: url("@/assets/icon/component/arxiv.png");
}
.gitHubIcon {
  background-image: url("@/assets/icon/component/github.png");
}
.huggingFaceIcon {
  background-image: url("@/assets/icon/component/huggingface.png");
}
.videoDisplayGroupContainer {
  display: grid;
  width: 100%;
  box-sizing: border-box;
  padding: 4vmax 25%;
  grid-template-columns: repeat(2, 1fr);
}
.videoDisplayGroupContainer .coverVideo video {
  width: 95%;
  margin: 0 2.5%;
}
.coverVideo {
  display: flex;
  width: 100%;
  box-sizing: border-box;
  flex-direction: row;
  justify-content: center;
}
.coverVideo video {
  width: 50%;
  aspect-ratio: 16/9;
  /* border-radius: 1vmax; */
}

.articleMainBodyContainer {
  display: flex;
  width: 100%;
  box-sizing: border-box;
  padding: 4vmax 25%;
}
.contentMainTitle {
  font-family: "Product-sans-black";
  font-size: 2vmax;
  color: #363636;
  margin: 0 0 1vmax;
  text-align: center;
}
.contentSubTitle {
  font-family: "Product-sans-black";
  font-size: 1.25vmax;
  color: #363636;
  margin: 0 0 1.5vmax;
}
.content {
  /* display: flex; */
  width: 100%;
  font-family: "Product-sans-regular";
  font-size: 1vmax;
  color: #363636;
  line-height: 1.5;
  margin: 0 0 1vmax;

  /* word-wrap: normal;
  word-break: normal; */
  text-align: justify;
}
.content a {
  color: #209cee;
}
.content a:hover {
  color: #1978b8;
}

.contentImg {
  display: flex;
  flex-direction: column;
  width: 100%;
  box-sizing: border-box;
  justify-content: center;
  align-items: center;
}
.contentImg img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  margin-bottom: 1.5vmax;
}
.contentImg .introText {
  font-family: "Product-sans-regular";
  font-size: 0.95vmax;
  color: #363636;
  line-height: 1.5;
  text-align: justify;
  padding: 0 7.5%;
  margin-bottom: 1.5vmax;
}

.contentImg2 {
  /* flex-direction: row; */
}
.contentImg2 img {
  width: 60%;
}

/* .contentImg2 .introText {
  text-align: justify;
  padding: 0 4vmax;
} */

.codeSpace {
  display: flex;
  width: 100%;
  /* justify-content: center; */
  overflow-x: scroll;
}
pre {
  display: flex;
  width: 100%;
  box-sizing: border-box;
  background-color: #d6d6d6;
  padding: 1vmax 0;
}
code {
  display: flex;
  width: 100%;
  font-family: NSimSun;
  font-size: 0.8vmax;
  color: #363636;
  line-height: 1.5;
  padding: 0.5vmax 3vmax;
}
</style>
