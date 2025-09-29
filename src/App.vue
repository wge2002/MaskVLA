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
    <video autoplay playsinline loop controls disable-picture-in-picture="true">
      <source src="./assets/mp4/intro.mp4" type="video/mp4" />
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
      approach. Our project page is
      <a href="https://anonymous.4open.science/w/MaskVLA-D31F/" target="_blank"
        >https://anonymous.4open.science/w/MaskVLA-D31F/</a
      >.
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
    <div class="contentMainTitle">Introduction</div>
    <div class="contentImg mediumImg">
      <img src="./assets/pic/pic1.png" alt="image" />
      <div class="introText">
        <span class="bold">Fig. 1.</span> We propose
        <span class="black">MaskVLA</span>, an improved fine-tuning method for
        multiview VLA frameworks that significantly enhances model performance.
        By randomly masking the primary camera input, the method guides the
        model to learn robust multi-view visual features. In both RoboTwin2.0
        simulation environments and real-world experiments, it demonstrates
        substantial improvements over OpenVLA-OFT across multiple manipulation
        tasks.
      </div>
    </div>
  </div>
  <div class="articleMainBodyContainer contentContainer">
    <div class="contentMainTitle">Methodology</div>
    <div class="contentImg mediumImg">
      <img src="./assets/pic/pic2.png" alt="image" />
      <div class="introText">
        <span class="bold">Fig. 2.</span>
        <span class="black"> Grad-CAM Analysis:</span>
        Qualitative comparisons on two RoboTwin tasks.
        <span class="black">Row 1:</span> Input images.
        <span class="black">Row 2:</span> Baseline (OpenVLA-OFT) shows scattered
        attention on irrelevant areas. <span class="black">Row 3:</span> MaskVLA
        concentrates attention precisely on task-critical regions validating its
        superior visual grounding via masked training.
      </div>
    </div>
  </div>
  <div class="articleMainBodyContainer contentContainer">
    <div class="contentImg">
      <img src="./assets/pic/pic3.png" alt="image" />
      <div class="introText">
        <span class="bold">Fig. 3.</span>
        <span class="black"> Architecture of our MaskVLA.</span>
        During the fine-tuning stage, a small portion of the input from the
        primary camera (e.g., 10%) is masked out. During inference, the model
        receives complete multi-camera inputs. This masking strategy reduces the
        model’s dependency on the primary camera and guides more robust and
        generalized feature learning.
      </div>
    </div>
  </div>
  <div class="articleMainBodyContainer contentContainer">
    <div class="contentMainTitle">Simulation Experiment</div>
    <div class="contentImg">
      <img src="./assets/pic/pic4.png" alt="image" />
      <div class="introText">
        <span class="bold">Fig. 4.</span>
        <span class="black"> Simulation experimental task demonstration.</span>
        We selected 4 tasks from the 50 tasks provided by robotwin and tested
        both their easy and hard modes respectively. (a) "Adjust bottle" easy
        mode; (b) "Adjust bottle" hard mode; (c) "Open laptop" easy mode; (d)
        "Open laptop" hard mode; (e) "Put object cabinet" easy mode; (f) "Put
        object cabinet" hard mode; (g) "Stack bowls three" easy mode; (h) "Stack
        bowls three" hard mode.
      </div>
    </div>
  </div>
  <div class="articleMainBodyContainer contentContainer">
    <div class="contentImg mediumImg">
      <img src="./assets/pic/pic5.png" alt="image" />
      <div class="introText">
        <span class="bold">Fig. 5.</span>
        <span class="black"> Failure Analysis.</span>
        (a) represents grasping at empty space caused by overfit; (b) represents
        model decision failure caused by OOD, continuously outputting repetitive
        action chunks with robotic arms repeatedly retreating; (c) represents
        situations where manipulated objects are knocked away due to internal
        object collision code in RoboTwin2.0 (as highlighted by the red box in
        the figure); (d) represents cases where low-quality task completion is
        judged as failure by the evaluation program; (e) represents situations
        other than the main cases mentioned above. The two pie charts on the
        right represent the quantity and proportion of failure cases for
        baseline and MaskVLA in evaluation respectively.
      </div>
    </div>
  </div>

  <!-- Simulation Videos -->
  <div class="videoDisplayGroupContainer contentContainer simVideo">
    <div class="occupied"></div>
    <div class="resultType">Ours✅️</div>
    <div class="resultType">Baseline❌</div>
    <div class="occupied"></div>
    <div class="difficultyType">Easy</div>
    <div class="difficultyType">Hard</div>
    <div class="difficultyType">Easy</div>
    <div class="difficultyType">Hard</div>

    <div class="taskType">
      <div class="taskName">Adjust Bottle</div>
      <div class="taskName">Open Laptop</div>
      <div class="taskName">Put Object Cabinet</div>
      <div class="taskName">Stack Bowls Three</div>
    </div>
    <!-- Success Case -->
    <div class="successCaseContainer">
      <div class="coverVideo">
        <!-- <div class="introText">"Adjust bottle" Easy Mode Success Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_adjust_clean_success_5x.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Adjust bottle" Hard Mode Success Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_adjust_randomized_success_5x.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Open laptop" Easy Mode Success Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_openlaptop_clean_success.mp4"
            type="video/mp4"
          />
        </video>
      </div>

      <div class="coverVideo">
        <!-- <div class="introText">"Open laptop" Hard Mode Success Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_openlaptop_randomized_success.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Put object cabinet" Easy Mode Success Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_putobject_clean_success.mp4"
            type="video/mp4"
          />
        </video>
      </div>

      <div class="coverVideo">
        <!-- <div class="introText">"Put object cabinet" Hard Mode Success Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_putobject_randomized_success.mp4"
            type="video/mp4"
          />
        </video>
      </div>

      <div class="coverVideo">
        <!-- <div class="introText">"Stack bowls three" Easy Mode Success Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_stack_clean_success.mp4"
            type="video/mp4"
          />
        </video>
      </div>

      <div class="coverVideo">
        <!-- <div class="introText">"Stack bowls three" Hard Mode Success Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_stack_randomized_success.mp4"
            type="video/mp4"
          />
        </video>
      </div>
    </div>

    <!-- Failure Case -->
    <div class="failureCaseContainer">
      <div class="coverVideo">
        <!-- <div class="introText">"Adjust bottle" Easy Mode Failure Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_adjust_clean_failed_5x.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Adjust bottle" Hard Mode Failure Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_adjust_randomized_failed_5x.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Open laptop" Easy Mode Failure Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_openlaptop_clean_failed.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Open laptop" Hard Mode Failure Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_openlaptop_randomized_failed.mp4"
            type="video/mp4"
          />
        </video>
      </div>

      <div class="coverVideo">
        <!-- <div class="introText">"Put object cabinet" Easy Mode Failure Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_putobject_clean_failed.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Put object cabinet" Hard Mode Failure Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_putobject_randomized_failed.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Stack bowls three" Easy Mode Failure Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_stack_clean_failed.mp4"
            type="video/mp4"
          />
        </video>
      </div>
      <div class="coverVideo">
        <!-- <div class="introText">"Stack bowls three" Hard Mode Failure Case</div> -->
        <video
          autoplay
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source
            src="./assets/mp4/sim_stack_randomized_failed.mp4"
            type="video/mp4"
          />
        </video>
      </div>
    </div>
  </div>

  <div class="articleMainBodyContainer contentContainer">
    <div class="contentImg">
      <img src="./assets/pic/pic6.png" alt="image" />
      <div class="introText">
        <span class="bold">Fig. 6. </span>
        ALOHA robot experimental task demonstration. Four representative tasks
        test MaskVLA’s multi-view information integration capability: (a) "Feed
        carrot" - Place the carrot in the food plate; (b) "Adjust cups" -
        Straighten the cups and place them on the plate; (c) "Place orange" -
        Place the orange in the fruit dish; (d) "Stack bowls" - Stack the bowls
        in sequence.
      </div>
    </div>
  </div>

  <div class="articleMainBodyContainer contentContainer">
    <div class="contentImg mediumImg">
      <img src="./assets/pic/table2.png" alt="image" />
    </div>
  </div>
  <div class="articleMainBodyContainer contentContainer">
    <div class="contentMainTitle">Real World Experiment</div>
  </div>

  <!-- Real-world Videos -->
  <div class="videoDisplayGroupContainer contentContainer realWorldVideo">
    <div class="coverVideo">
      <div class="introText">Feed carrot</div>
      <video
        autoplay
        muted
        playsinline
        loop
        controls
        disable-picture-in-picture="true"
      >
        <source src="./assets/mp4/real_carrot_success.mp4" type="video/mp4" />
      </video>
    </div>
    <div class="coverVideo">
      <div class="introText">Adjust cups</div>
      <video
        autoplay
        muted
        playsinline
        loop
        controls
        disable-picture-in-picture="true"
      >
        <source
          src="./assets/mp4/real_adjust_cup_success.mp4"
          type="video/mp4"
        />
      </video>
    </div>
    <div class="coverVideo">
      <div class="introText">Place orange</div>
      <video
        autoplay
        muted
        playsinline
        loop
        controls
        disable-picture-in-picture="true"
      >
        <source src="./assets/mp4/real_orange_success.mp4" type="video/mp4" />
      </video>
    </div>

    <div class="coverVideo">
      <div class="introText">Stack bowls</div>
      <video
        autoplay
        muted
        playsinline
        loop
        controls
        disable-picture-in-picture="true"
      >
        <source
          src="./assets/mp4/real_stack_left_success.mp4"
          type="video/mp4"
        />
      </video>
    </div>
  </div>
  <!-- <div class="coverVideo">
      <div class="introText">"Stack bowls"with Right Arm</div>
      <video
        autoplay
        muted
        playsinline
        loop
        controls
        disable-picture-in-picture="true"
      >
        <source
          src="./assets/mp4/real_stack_right_success.mp4"
          type="video/mp4"
        />
      </video>
    </div> 
  </div>-->
  <div class="articleMainBodyContainer contentContainer">
    <div class="contentImg tinyImg">
      <img src="./assets/pic/pic7.png" alt="image" />
      <div class="introText">
        <span class="bold">Fig. 7. </span>
        Real-world multi-task results.
      </div>
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
/* * {
  word-break: normal;
  word-wrap: break-word;
} */
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

.black {
  font-family: "Product-sans-black";
}

.contentContainer {
  display: flex;
  flex-direction: column;
  position: relative;
  box-sizing: border-box;
  width: 100%;
  min-width: 960px;
  height: fit-content;
  padding: 5vmax 0 0;
  background-color: #ffffff;
}
.contentContainer:last-child {
  padding-bottom: 15vmax;
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
  padding: 4vmax 20%;
}
.simVideo {
  grid-template-rows: 2fr 1fr 16fr;
  grid-template-columns: 1fr repeat(4, 1.5fr);
}
.simVideo > *:nth-child(-n + 3) {
  border-bottom: #000000 solid 0.1vmax;
}
.simVideo > *:nth-child(n + 4):nth-child(-n + 8) {
  border-top: #000000 solid 0.1vmax;
}
.resultType {
  display: flex;
  width: 100%;
  height: 100%;
  font-family: "Product-sans-bold";
  box-sizing: border-box;
  font-size: 1.5vmax;
  color: #363636;
  justify-content: center;
  align-items: center;
}
.resultType:nth-child(2) {
  grid-column: 2/4;
  border-right: #000000 solid 0.1vmax;
}
.resultType:nth-child(3) {
  grid-column: 4/6;
  border-left: #000000 solid 0.1vmax;
}
.difficultyType {
  display: flex;
  font-family: "Product-sans-bold";
  box-sizing: border-box;
  font-size: 1.2vmax;
  color: #363636;
  justify-content: center;
  align-items: end;
  grid-row: 2/3;
}

.difficultyType:nth-child(5) {
  grid-column: 2/3;
}
.difficultyType:nth-child(6) {
  grid-column: 3/4;
  border-right: #000000 solid 0.1vmax;
}
.difficultyType:nth-child(7) {
  grid-column: 4/5;
  border-left: #000000 solid 0.1vmax;
}
.difficultyType:nth-child(8) {
  grid-column: 5/6;
}
.taskType {
  display: grid;
  grid-template-rows: repeat(4, 1fr);
  font-family: "Product-sans-bold";
  box-sizing: border-box;
  font-size: 1.2vmax;
  color: #363636;
  padding-bottom: 1vmax;
  padding-right: 1vmax;
  grid-column: 1/2;
  grid-row: 3/7;
}
.taskName {
  display: flex;
  margin: 1vmax 0;
  align-items: center;
  justify-content: center;
  text-align: center;
  line-height: 1.5;
}
.successCaseContainer,
.failureCaseContainer {
  display: grid;
  width: 100%;
  box-sizing: border-box;
  padding-bottom: 1vmax;
  grid-template-columns: repeat(2, 1fr);
}
.successCaseContainer {
  padding-right: 5%;
  border-right: #000000 solid 0.1vmax;
  grid-column: 2/4;
}
.failureCaseContainer {
  padding-left: 5%;
  border-left: #000000 solid 0.1vmax;
  grid-column: 4/6;
  padding-right: 1vmax;
}
.videoDisplayGroupContainer .coverVideo video {
  width: 95%;
  margin: 0 2.5%;
}
.coverVideo {
  display: flex;
  width: 100%;
  box-sizing: border-box;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 1vmax;
}
.realWorldVideo.videoDisplayGroupContainer {
  padding: 0 25%;
  grid-template-columns: repeat(2, 1fr);
}
.realWorldVideo .coverVideo {
  margin-top: 0;
  margin-bottom: 2vmax;
}
.coverVideo video {
  width: 50%;
  aspect-ratio: 16/9;
  border: #d0d0d0 solid 0.1vmax;
  /* border-radius: 1vmax; */
}

.articleMainBodyContainer {
  display: flex;
  width: 100%;
  box-sizing: border-box;
  padding: 4vmax 25% 0;
}
.contentMainTitle {
  font-family: "Product-sans-black";
  font-size: 2vmax;
  color: #363636;
  margin: 0 0 1vmax;
  text-align: center;
  padding-bottom: 1vmax;
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
.mediumImg img {
  width: 75%;
}
.tinyImg img {
  width: 50%;
}
.contentImg .introText,
.coverVideo .introText {
  font-family: "Product-sans-regular";
  font-size: 0.95vmax;
  color: #363636;
  line-height: 1.5;
  text-align: justify;
  padding: 0 7.5%;
  margin: 0.5vmax 0 1.5vmax;
}

.realWorldVideo .coverVideo .introText {
  font-family: "Product-sans-bold";
  font-size: 1.25vmax;
  margin: 0.5vmax 0;
}
.coverVideo .introText {
  font-family: "Product-sans-medium";
  margin: 2.5vmax 0 0.5vmax;
  font-size: 1vmax;
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
