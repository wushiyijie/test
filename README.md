<!DOCTYPE html>
<html lang="zh-Hans">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>curriculum vitae</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap"
      rel="stylesheet"
    />
    <style>
      :root {
        --bg: #111;
        --text: #eee;
        --table-bg: #222;
        --table-border: #444;
        --table-th-bg: #333;
        --header-bg: #333;
        --header-text: #fff;
      }
      .light-mode {
        --bg: #fff;
        --text: #333;
        --table-bg: #f9f9f9;
        --table-border: #ccc;
        --table-th-bg: #e0e0e0;
        --header-bg: #ddd;
        --header-text: #333;
      }
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      body {
        font-family: "Roboto", sans-serif;
        background: var(--bg);
        color: var(--text);
        padding: 20px;
        position: relative;
        overflow-x: hidden;
        transition: background 0.5s, color 0.5s;
      }
      h1.ct.tt {
        font-size: 2em;
        text-align: center;
        margin-top: 40px;
        text-transform: uppercase;
        border-bottom: 3px solid #aaa;
        display: inline-block;
        animation: fadeInDown 2s ease-out;
      }
      hr {
        margin: 20px 0;
      }
      h2 {
        font-size: 1.5em;
        margin: 20px 0 20px;
        padding: 10px;
        background: var(--header-bg);
        color: var(--header-text);
        cursor: pointer;
        transition: background 0.3s, box-shadow 0.3s;
        animation: fadeInLeft 1.8s forwards;
        border-radius: 5px;
      }
      h2:hover {
        background: #444;
        box-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
      }
      ol.pp {
        margin-left: 10px;
        margin-bottom: 30px;
        max-height: 1000px;
        opacity: 1;
        transform: scaleY(1);
        transition: max-height 0.6s ease, opacity 0.6s ease, transform 0.6s ease;
        overflow: hidden;
      }
      ol.pp.hidden {
        max-height: 0;
        opacity: 0;
        transform: scaleY(0.95);
      }
      .circle-btn {
        position: fixed;
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background: #d2f0f4;
        color: #fff;
        border: none;
        cursor: pointer;
        font-size: 1.5em;
        box-shadow: 0 0 8px #a1afc9;
        transition: background 0.3s, transform 0.3s, box-shadow 0.3s;
        display: flex;
        align-items: center;
        justify-content: center;
        z-index: 1001;
      }
      .circle-btn:hover {
        background: #424c50;
        transform: scale(1.1);
        box-shadow: 0 0 12px #a1afc9;
      }
      #scrollToTopBtn {
        bottom: 20px;
        right: 20px;
      }
      #toggleAllBtn {
        bottom: 90px;
        right: 20px;
      }
      #themeToggleBtn {
        top: 20px;
        right: 20px;
      }
      @keyframes fadeIn {
        from {
          opacity: 0;
          transform: translateY(20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
      @keyframes fadeInDown {
        from {
          opacity: 0;
          transform: translateY(-20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
      @keyframes fadeInLeft {
        from {
          opacity: 0;
          transform: translateX(-20px);
        }
        to {
          opacity: 1;
          transform: translateX(0);
        }
      }
      .highlight {
        text-shadow: 0 0 5px rgba(255, 215, 0, 0.8);
        background-color: rgba(255, 215, 0, 0.15);
        transition: text-shadow 0.3s;
      }
      .cursor-trail {
        position: absolute;
        width: 8px;
        height: 8px;
        border-radius: 50%;
        background: var(--header-text);
        pointer-events: none;
        animation: trailFade 0.5s forwards;
        box-shadow: 0 0 10px var(--header-text);
      }
      @keyframes trailFade {
        0% {
          opacity: 1;
          transform: scale(1);
        }
        100% {
          opacity: 0;
          transform: scale(0.5);
        }
      }
      .bubble {
        position: fixed;
        border-radius: 50%;
        background: linear-gradient(
          45deg,
          rgba(255, 0, 0, 0.3),
          rgba(255, 127, 0, 0.3),
          rgba(255, 255, 0, 0.3),
          rgba(0, 255, 0, 0.3),
          rgba(0, 0, 255, 0.3),
          rgba(75, 0, 130, 0.3),
          rgba(148, 0, 211, 0.3)
        );
        color: #808080;
        width: 70px;
        height: 70px;
        line-height: 70px;
        text-align: center;
        font-weight: bold;
        z-index: 1000;
        pointer-events: auto;
        user-select: none;
        animation: float 4s ease-in-out infinite;
        transition: box-shadow 0.3s;
      }
      .bubble:hover {
        box-shadow: 0 0 15px #000000;
      }
      @keyframes float {
        0% {
          transform: translate(0, 0);
        }
        50% {
          transform: translate(30px, -30px);
        }
        100% {
          transform: translate(0, 0);
        }
      }
      lg {
        color: #90ee90;
        font-weight: bold;
      }
      .lollipop-effect {
        position: absolute;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background: conic-gradient(
          rgba(255, 0, 0, 0.5),
          rgba(255, 127, 0, 0.5),
          rgba(255, 255, 0, 0.5),
          rgba(0, 255, 0, 0.5),
          rgba(0, 0, 255, 0.5),
          rgba(75, 0, 130, 0.5),
          rgba(148, 0, 211, 0.5),
          rgba(255, 0, 0, 0.5)
        );
        animation: spin 1s linear infinite, fadeOut 1s forwards;
        pointer-events: none;
        box-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
      }

      @keyframes spin {
        from {
          transform: rotate(0deg);
        }
        to {
          transform: rotate(360deg);
        }
      }

      @keyframes fadeOut {
        0% {
          opacity: 1;
          transform: scale(1);
        }
        100% {
          opacity: 0;
          transform: scale(0.5);
        }
      }

      #cvHeading {
        font-size: 2em;
        margin-top: 20px;
        margin-bottom: 20px;
        padding: 15px;
        background: var(--header-bg);
        color: var(--header-text);
        border-radius: 10px;
        text-align: center;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      }

      #cvContent {
        font-size: 1em;
        line-height: 1.8;
        margin-bottom: 30px;
        padding: 20px;
        background: var(--table-bg);
        border: 1px solid var(--table-border);
        border-radius: 10px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        color: var(--text);
      }

      .tag {
        display: inline-block;
        border-radius: 10px;
        padding: 2px 8px;
        margin-left: 5px;
        font-size: 0.9em;
      }
      .tag-red {
        border: 1px solid #ff9999;
        background: rgba(255, 153, 153, 0.2);
        color: #ff6666;
      }
      .tag-orange {
        border: 1px solid #ffcc99;
        background: rgba(255, 204, 153, 0.2);
        color: #ff9966; 
      }
      .tag-blue {
        border: 1px solid #99ccff;
        background: rgba(153, 204, 255, 0.2);
        color: #6699ff;
      }
      .tag-green {
        border: 1px solid #99e699;
        background: rgba(153, 230, 153, 0.2);
        color: #66cc66;
      }
    </style>
  </head>
  <body>
    <h2 id="cvHeading">   ˼   </h2>
    <p id="cvContent"></p>
    <h2>    ԭ  </h2>
    <ol class="pp">
      
        <b>1.  ѧУ    ֪:</b><br>
        <b>(1)ѧ        רҵʵ           </b><br>
        <p>   ȴ ѧӵ и   ʡ ص ʵ   ң  硰      Ϣ                ʵ   ҡ                о    ĵȿ   ƽ̨    
           󡰲 ѧ  һ 廯      ģʽ    У       Ŀ    ҵ  ʦ ƣ        ҿ  ٳɳ Ϊ   ѧ       빤  ʵ   ĸ      ˲š </p><br>
        <b>(2)   ʻ   Ұ   ѧ   ںϵĹ   ƽ̨</b><br>
        <p>  Ϊ         ѧ              רҵ   С   У+  У  ս ԣ 
         ṩ  3+1    ˶          Ŀ       ¼  ¹     ѧ  Ӣ          ѧ ĺ              ޼ƻ        ҶԺ   ѧ            
           󡰼    +   ˫ѧλ    ģʽ   Լ      Ľ       ɫ  Դ          δ   ڹ  ʻ      Ŷ  з          á </p><br>
        <b>2.    Ը  </b><br>
        <p>ѡ   ȴ ѧ     רҵ       ǶԼ   ǰ ص ׷ 󣬸  Ƕԡ  ô   ı    硱    ļ  С 
           ڴ  ڻ      ܼ   ʵ   ҡ   ̽  AI ߽磬 ڡ У       Ŀ   л   ʵս   飬 ڡ    ʻ          ؿ      Ұ  
           ճɳ Ϊ  ߡ       ȡ  롰   Ĺػ       ʱ      ʦ  </p><br>
      
    </ol>
    
    <h2>      Ϣ</h2>
    <ol class="pp">
      
        <b>    ԺУ     ȴ ѧ<br>
         <b>רҵ         ѧ 뼼  <br><br>
        <p>   壺    </p><br> 
        <p> ־ӣ     Ȫ  </p><br>
        <p> 绰  17759019791</p><br>
        <p>   ᣺    </p><br>
        <p>   䣺1625138673@qq.com</p>
   
    </ol>

    <h2>        </h2>
    <ol class="pp">
        <p>2016.09    2019.06</p><br>
        <p>ԺУ   ƣ Ȫ ݵ     ѧ</p><br>
        <p>2019.09    2022.06</p><br>
        <p>ԺУ   ƣ Ȫ  ʵ    ѧ</p><br>
        <p>2022.09    2026.06</p><br>
        <p>ԺУ   ƣ        ĿƼ ѧԺ</p><br>
        <p>רҵ         ѧ 뼼  רҵ</p><br>
        <b>   ޿γ̣     ϵͳ     ݽṹ     ݿ⡢     ھ </b><br><br>
        <b> ɼ        꼶    ǰ20%<br><br>
        <p>         ֤ 飺</p>
        <b>1. ļ ֤  </b><br>
        <b>2.2023       е ʮһ   ѧ        ƴ      Ƚ </b><br>
        <b>3.У     б      㽱</b><br>
        <b>4.ӭ ± У                   </b><br>
        <b>5.     д ѧ   ׽  У   ཻ          </b><br>
        <b>6.2023  ϴ   Χ          </b><br>
        <b>7.2024  ϴ   Χ          </b><br>
        <b>8.ӵ  C1  ʻ֤</b><br>
        <b>9.ӵ  Χ  2  ֤  </b><br>
      
    </ol>
    
    <h2>  Ŀ    </h2>
    <ol class="pp">
      <li>
        <b>2024.02~2024.3 </b><b>  ѧ    ҵ  Ŀ     </b><b>  ĿС 鸺    </b><br>
        <b>  Ŀ   ⣺       塱ɽ  - ǻ ũ 帳 ܡ </b><br>
        <b>   ˽ ɫ    Ŀ    ĸ    ˣ ͳ  8 ˿ ѧ   Ŷӡ </b><br>
        <b>  Ҫְ  </b><br>
        <p>(1)ͨ    ȹ ͨ ھ  Աר     ƶ    Ի  ֹ       </p><br>
        <p>(2)Э    Դ ƽ   Ŀִ У ȷ   ׶   Ŀ   ɣ </p><br>
        <p>(3)      ֯ ŶӸ  ̣  Ż Э     ̡ </p><br>
        <b>ʵ   ջ </b><br>
        <p>(1)   򾭼ö  죺           ũ   г                ǻ ũҵ     ý ϵ Ǳ ڻ  ᣻</p><br>
        <p>(2) Ŷӹ     ԣ  ܽ      ̬ ֹ +Ŀ 굼 򡱵 Э  ģʽ       Ŷ ִ      </p><br>
        <p>(3)  ҵ  ֪            ߵ      г      ƽ  㣬Ϊ      ҵʵ      ʵս   顣</p><br>
      </li>
      <li>
       <b>2024.02~2024.3 </b><b>  ѧ    ҵ  Ŀ     </b><b>  ĿС   Ա</b><br>
       <b>  Ŀ   ⣺      δ    </b><br>
       <b>  Ҫְ  </b><br>
       <p>(1)ȫ ̽        Ŀ     ˣ   Чִ   Ŷӷֹ       Ŀ ߻                  صȻ    з  ӹؼ    ã </p><br>
       <p>(2)         Ŀ ؼ ģ  Ŀ       ֤  ͨ    ѧ  Э     ں     ѧ     ݷ       ҵ   ԣ    ƶ   Ŀ     ۿ       ز Ʒת    </p><br>
       <b>ʵ   ջ </b><br>
       <p>(1)ϵͳ       ֲ ҵȫ  ·         ۣ          ݴ      ַ        û   Ӫ    ҵ     ֵ Эͬ ߼   </p><br>
       <p>(2)        Python ȹ           г    ݽ ģ    ӻ                   ҵ ο   ֵ   û   ΪԤ  ģ ͣ </p><br>
       <p>(3)ǿ   ˿      Ŷ Э   븴            </u><br>
      </li>
      <li>
       <b>2024.02~2024.3 </b><b>  ѧ    ҵ  Ŀ     </b><b>  ĿС   Ա</b><br>
       <b>  Ŀ   ⣺      Χ       Ŀ       л       </b><br>
       <b>  Ҫְ  </b><br>
       <p>(1)ȫ    Ȳ     Ŀȫ   ڹ      ׼ ԽӸ     ս Բ       Ŀ ߻                      صȹؼ      ге    Ľ ɫ  </p><br>
       <p>(2)      Ŀ ɹ  Ķ   չʾ  · ݣ ͨ    ׼    Χ   Ļ  ں     ҵ  ֵ       Ŷ  ڴ ҵ      ն  Ѽ   </p><br>
       <b>ʵ   ջ </b><br>
       <p>(1) Ļ   ֪   ϵͳ    Χ      Ļ    磬       Ϊ л        ŵĵ       ·    ǿ   Ļ          θУ </p><br>
       <p>(2) г                Ļ   ҵ г          ۣ     Χ        Ĵ     Ʒ  ϸ             ȷ    ְҵ        ҵ  ϵ㣻</p><br>
       <p>(3)ս  ˼ά      ͨ    Ŀ  0  1     ʵ           Ļ   ֵ ھ   ҵ   ֵ ȫ  ·˼ά  ǿ   Ŷ Э      Դ          </p><br>
      </li>
    </ol>

    <h2>У԰    </h2>
    <ol class="pp">
      <li>
       <b>2022.09~2025.04</b> <b>        </b><b>ʵѵ        </b><br>
        <p>(1)         滮  ͳ  10+  У           £      Ŷ   ɴӴ   ߻    ֳ ִ еıջ                ۼƳ 500 ˴Σ </p><br>
        <p>(2) ۼ             10+       ж     Ա ں        л񽱣 </p><br>
        <p>(3)  β   У              ȡ   ˼Ѽ </p><br>
      </li>
      <li>
       <b>2022.09~2025.04</b> <b>Ժ   ۶ </b><b>  Ա</b><br>
       <p>(1)         30+      ģ    ۣ ͨ          ⡪     ع        Ż    ջ ѵ    ϵ  ʵ   ߼   ܴ   ٳ Ӧ 估 ۵    ͻ ƣ </p><br>
       <p>(2)       Ա   Ժ   ֽ    д裬     ڶԿ  гɳ </p><br>
       <p>(3)     Ϊ       ִ   ѧԺ  սУ        </p><br>
      </li>
      <li>
       <b>2022.09~2025.04</b> <b>Ժ     </b><b>  Ա</b><br>
       <p>(1)        У        </p><br>
       <p>(2)           ѵ  </p><br>
      </li>
    </ol>

    

    <button id="themeToggleBtn" class="circle-btn"> 9 8</button>
    <button id="toggleAllBtn" class="circle-btn"> 9 0</button>
    <button id="scrollToTopBtn" class="circle-btn"> 9 9</button>


    <script>
        
      const bubbleCount = 2;
      for (let i = 0; i < bubbleCount; i++) {
        const bubble = document.createElement("div");
        bubble.classList.add("bubble");
        bubble.innerText = "H.H.";
        bubble.style.left = Math.random() * 100 + "vw";
        bubble.style.top = Math.random() * 100 + "vh";
        let duration = Math.random() * 3 + 4;
        bubble.style.animationDuration = duration + "s";
        bubble.addEventListener("mouseenter", () => {
          bubble.innerText = "Honghui";
          bubble.style.animationPlayState = "paused";
        });
        bubble.addEventListener("mouseleave", () => {
          bubble.innerText = "H.H.";
          bubble.style.animationPlayState = "running";
        });
        document.body.appendChild(bubble);
      }

      document.querySelectorAll("h2").forEach((heading) => {
        heading.addEventListener("click", () => {
          const siblingOL = heading.nextElementSibling;
          if (siblingOL && siblingOL.tagName === "OL") {
            siblingOL.classList.toggle("hidden");
          }
        });
      });

      let allCollapsed = false;
      const toggleAllBtn = document.getElementById("toggleAllBtn");
      toggleAllBtn.addEventListener("click", () => {
        toggleAllBtn.style.transition = "transform 0.3s";
        toggleAllBtn.style.transform = "translateY(-10px)";
        setTimeout(() => {
          toggleAllBtn.style.transform = "translateY(0)";
          document.querySelectorAll("ol.pp").forEach((list) => {
            if (!allCollapsed) {
              list.classList.add("hidden");
            } else {
              list.classList.remove("hidden");
            }
          });
          allCollapsed = !allCollapsed;
          toggleAllBtn.innerText = allCollapsed ? " 9 1" : " 9 0";
        }, 300);
      });

      const scrollBtn = document.getElementById("scrollToTopBtn");
      scrollBtn.style.display = "none";
      
      document.body.classList.add("light-mode");
      
      window.addEventListener("scroll", () => {
        if (document.documentElement.scrollTop > 200) {
          scrollBtn.style.display = "flex";
        } else {
          scrollBtn.style.display = "none";
        }
      });

      scrollBtn.addEventListener("click", () => {
        window.scrollTo({ top: 0, behavior: "smooth" });
      });

      const themeToggleBtn = document.getElementById("themeToggleBtn");
      themeToggleBtn.addEventListener("click", () => {
        let flashCount = 0;
        const flashInterval = setInterval(() => {
          themeToggleBtn.style.background = flashCount % 2 === 0 ? "#000" : "#fff";
          flashCount++;
          if (flashCount === 6) {
            clearInterval(flashInterval);
            document.body.classList.toggle("light-mode");
            themeToggleBtn.style.background = "";
            themeToggleBtn.innerText = document.body.classList.contains("light-mode") ? " 9 6" : " 9 8";
          }
        }, 150);
      });

      
      const cvTranslations = {
        en: "I'm Zeng honghui, I am currently pursuing a bachelor's degree at Chongqing University of Humanities, Science and Technology.",
        "zh-Hans": "         ԣ Ŀǰ           ĿƼ ѧԺ        ѧλ  ",  
      };
      const initialCVContent = "         ԣ Ŀǰ           ĿƼ ѧԺ        ѧλ  ";
      document.getElementById("cvContent").textContent = initialCVContent;
      

      const cvHeadingTranslations = {
        "zh-Hans": "   ˼   ",
        en: "Curriculum Vitae"
      };

      const headings = [
        { en: "Curriculum Vitae", "zh-Hans": "   ˼   " },
        { en: "Reason for application", "zh-Hans": "    ԭ  "},
        { en: "Application Information", "zh-Hans": "      Ϣ" },
        { en: "Educational experience", "zh-Hans": "        "},
        { en: "Project experience", "zh-Hans": "  Ŀ    "},
        { en: "Campus experience", "zh-Hans": "У԰    "},
      ];

      document.getElementById("cvHeading").textContent = cvHeadingTranslations["zh-Hans"];

      const languageToggleBtn = document.createElement("button");
      languageToggleBtn.id = "languageToggleBtn";
      languageToggleBtn.className = "circle-btn";
      languageToggleBtn.style.top = "20px";
      languageToggleBtn.style.left = "auto";
      languageToggleBtn.style.right = "80px";
      languageToggleBtn.textContent = " 9 4";
      document.body.appendChild(languageToggleBtn);

      const languages = ["en", "zh-Hans"];
      let currentLanguageIndex = 1;

      languageToggleBtn.addEventListener("click", () => {
        languageToggleBtn.style.transition = "transform 0.5s";
        languageToggleBtn.style.transform = "rotate(540deg)";
        setTimeout(() => {
          languageToggleBtn.style.transform = "rotate(0deg)";
          currentLanguageIndex = (currentLanguageIndex + 1) % languages.length;
          const selectedLanguage = languages[currentLanguageIndex];
          document.querySelectorAll("h2").forEach((heading, index) => {
            heading.textContent = headings[index][selectedLanguage];
          });
          document.getElementById("cvHeading").textContent = cvHeadingTranslations[selectedLanguage];
          document.getElementById("cvContent").textContent = cvTranslations[selectedLanguage];
        }, 500);
      });

      const languageSelector = document.getElementById("languageSelector");
      if (languageSelector) {
        languageSelector.remove();
      }

      document.querySelectorAll("ol.pp").forEach((list) => {
        list.querySelectorAll("li").forEach((item, index) => {
          const originalHTML = item.innerHTML;
          item.innerHTML = `${index + 1}. ${originalHTML}`;
        });
      });

      document.addEventListener("mousemove", (event) => {
        const cursorTrail = document.createElement("div");
        cursorTrail.classList.add("cursor-trail");
        cursorTrail.style.left = `${event.pageX}px`;
        cursorTrail.style.top = `${event.pageY}px`;
        document.body.appendChild(cursorTrail);

        setTimeout(() => {
          cursorTrail.remove();
        }, 500);
      });

      function wrapTextNodes(node) {
        if (node.nodeType === 3) {
          const re = /Honghui Zeng/g;
          if (node.data.match(re)) {
            const frag = document
              .createRange()
              .createContextualFragment(
                node.data.replace(
                  re,
                  '<span class="highlight">Honghui Zeng</span>'
                )
              );
            node.parentNode.replaceChild(frag, node);
          }
        } else if (
          node.nodeType === 1 &&
          node.childNodes &&
          !/(script|style|button)/i.test(node.tagName)
        ) {
          for (let i = 0; i < node.childNodes.length; i++) {
            wrapTextNodes(node.childNodes[i]);
          }
        }
      }
      document.addEventListener("DOMContentLoaded", () => {
        wrapTextNodes(document.body);
      });
    </script>
  </body>
</html>
