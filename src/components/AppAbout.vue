<template>
  <div id="about">
    <a id="down" href="#about-me">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
        <path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z" />
      </svg>
    </a>
    <div id="about-me">
      <h1>About Me</h1>
      <div id="about-p">
        <p>
          My name is Anton Shevchuk and I'm a web developer from
          <a href="https://en.wikipedia.org/wiki/Ukraine" target="_blank"
            >Ukraine</a
          >, currently working at the Hanover Medical School in
          <a href="https://goo.gl/maps/Fy9jpgmdEPoKWERv5" target="_blank"
            >Hanover, Lower Saxony, Germany</a
          >.
        </p>
        <p>
          I started learning programming when I was 15 years old. I was studying
          Front-End development at the
          <a href="https://ucode.world/en/" target="”_blank”"
            >ucode IT Academy</a
          >
          in
          <a href="https://goo.gl/maps/FpxYVbHm6HkBFvyP7" target="_blank"
            >Kyiv, Ukraine</a
          >, from I bear most of my knowledge.
        </p>
        <p>
          But my progress didn't stop there, as I continued to expand my
          knowledge and learned Vue, a reactive JavaScript framework, on which
          this whole website is running, by the way.
        </p>
      </div>
      <h2></h2>
      <h1 id="skills">Skill Set</h1>

      <h2>Languages</h2>
      <div id="language-flex">
        <div id="language-box">
          <div class="language">
            <img src="../assets/ukflag.png" alt="Flag of The UK" />
            <span>English &#8212; Fluent</span>
          </div>
          <div class="language">
            <img src="../assets/ukraineflag.png" alt="Flag of Ukraine" />
            <span>Ukrainian &#8212; Native</span>
          </div>
          <div class="language">
            <img src="../assets/germanyflag.png" alt="Flag of Germany" />
            <span>German &#8212; Intermediate</span>
          </div>
          <div class="language">
            <img src="../assets/polandflag.png" alt="Flag of Poland" />
            <span>Polish &#8212; Intermediate</span>
          </div>
          <div class="language">
            <img src="../assets/russiaflag.png" alt="Flag of Russia" />
            <span>Russian &#8212; Fluent</span>
          </div>
        </div>
        <div id="language-desc">
          <p>
            I grew up speaking Ukrainian, and learned Russian along the way because of the cultural influence. Learning English I started from an early age of just 4 years old, and I have been learning it ever since. Now I consider myself fluent in English, and use it to work now, while mastering my German. I started learning Polish as a hobby, to expand my knowledge and to improve my communication skills. I want to be considered a polyglot one day.
          </p>
          <p>
            I started learning German in middle school, but continued after I relocated to Germany, to be able to communicate with people and especially my coworkers, those who aren't as good with English.
          </p>
        </div>
      </div>

      <h2>Front-End</h2>
      <div class="icon-box">
        <a
          href="https://developer.mozilla.org/en-US/docs/Web/HTML"
          target="_blank"
        >
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M12,17.56L16.07,16.43L16.62,10.33H9.38L9.2,8.3H16.8L17,6.31H7L7.56,12.32H14.45L14.22,14.9L12,15.5L9.78,14.9L9.64,13.24H7.64L7.93,16.43L12,17.56M4.07,3H19.93L18.5,19.2L12,21L5.5,19.2L4.07,3Z"
            />
          </svg>
          <span>HTML5</span>
        </a>
        <a
          href="https://developer.mozilla.org/en-US/docs/Web/CSS"
          target="_blank"
        >
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M5,3L4.35,6.34H17.94L17.5,8.5H3.92L3.26,11.83H16.85L16.09,15.64L10.61,17.45L5.86,15.64L6.19,14H2.85L2.06,18L9.91,21L18.96,18L20.16,11.97L20.4,10.76L21.94,3H5Z"
            />
          </svg>
          <span>CSS3</span>
        </a>
        <a
          href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"
          target="_blank"
        >
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M3,3H21V21H3V3M7.73,18.04C8.13,18.89 8.92,19.59 10.27,19.59C11.77,19.59 12.8,18.79 12.8,17.04V11.26H11.1V17C11.1,17.86 10.75,18.08 10.2,18.08C9.62,18.08 9.38,17.68 9.11,17.21L7.73,18.04M13.71,17.86C14.21,18.84 15.22,19.59 16.8,19.59C18.4,19.59 19.6,18.76 19.6,17.23C19.6,15.82 18.79,15.19 17.35,14.57L16.93,14.39C16.2,14.08 15.89,13.87 15.89,13.37C15.89,12.96 16.2,12.64 16.7,12.64C17.18,12.64 17.5,12.85 17.79,13.37L19.1,12.5C18.55,11.54 17.77,11.17 16.7,11.17C15.19,11.17 14.22,12.13 14.22,13.4C14.22,14.78 15.03,15.43 16.25,15.95L16.67,16.13C17.45,16.47 17.91,16.68 17.91,17.26C17.91,17.74 17.46,18.09 16.76,18.09C15.93,18.09 15.45,17.66 15.09,17.06L13.71,17.86Z"
            />
          </svg>
          <span>JavaScript</span>
        </a>
        <a href="https://vuejs.org/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M2,3H5.5L12,15L18.5,3H22L12,21L2,3M6.5,3H9.5L12,7.58L14.5,3H17.5L12,13.08L6.5,3Z"
            />
          </svg>
          <span>Vue.js</span>
        </a>
        <a href="https://sass-lang.com/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M10,15.33C10.16,15.87 10.14,16.37 10,16.83C10,16.88 9.96,16.93 9.94,17C9.92,17 9.9,17.07 9.87,17.12C9.76,17.36 9.6,17.59 9.41,17.79C8.83,18.43 8,18.67 7.67,18.47C7.29,18.25 7.5,17.35 8.16,16.64C8.88,15.88 9.92,15.38 9.92,15.38V15.38L10,15.33M18.27,6.28C17.82,4.5 14.87,3.92 12.09,4.91C10.43,5.5 8.63,6.42 7.34,7.63C5.81,9.07 5.56,10.32 5.66,10.84C6,12.68 8.54,13.89 9.58,14.78V14.79C9.28,14.94 7.04,16.07 6.5,17.23C5.96,18.45 6.6,19.33 7,19.45C8.34,19.81 9.69,19.16 10.41,18.07C11.11,17.03 11.06,15.68 10.75,15C11.17,14.9 11.66,14.85 12.28,14.92C14.04,15.13 14.38,16.22 14.31,16.68C14.25,17.14 13.88,17.39 13.76,17.47C13.64,17.54 13.6,17.57 13.61,17.63C13.62,17.71 13.68,17.71 13.78,17.69C13.93,17.66 14.71,17.32 14.74,16.47C14.78,15.39 13.75,14.19 11.93,14.22C11.18,14.24 10.71,14.31 10.37,14.44L10.29,14.35C9.16,13.15 7.08,12.3 7.17,10.68C7.2,10.09 7.4,8.55 11.17,6.67C14.25,5.13 16.72,5.55 17.15,6.5C17.76,7.83 15.83,10.32 12.63,10.68C11.41,10.82 10.76,10.34 10.6,10.17C10.43,10 10.41,9.97 10.35,10C10.24,10.07 10.31,10.23 10.35,10.33C10.44,10.58 10.84,11 11.5,11.24C12.09,11.43 13.53,11.54 15.26,10.87C17.2,10.12 18.72,8.03 18.27,6.28Z"
            />
          </svg>
          <span>Sass</span>
        </a>
      </div>

      <h2>Software</h2>
      <div class="icon-box">
        <a href="https://code.visualstudio.com/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M17,16.47V7.39L11,11.93M2.22,9.19C1.92,8.87 1.91,8.37 2.2,8.04L3.4,6.93C3.6,6.75 4.09,6.67 4.45,6.93L7.87,9.54L15.8,2.29C16.12,1.97 16.67,1.84 17.3,2.17L21.3,4.08C21.66,4.29 22,4.62 22,5.23V18.73C22,19.13 21.71,19.56 21.4,19.73L17,21.83C16.68,21.96 16.08,21.84 15.87,21.63L7.85,14.33L4.45,16.93C4.07,17.19 3.6,17.12 3.4,16.93L2.2,15.83C1.88,15.5 1.92,14.96 2.25,14.63L5.25,11.93"
            />
          </svg>
          <span>Visual Studio Code</span>
        </a>
        <a href="https://www.microsoft.com/en/microsoft-365" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M19.94 5.59V18.39Q19.94 19.06 19.55 19.59 19.16 20.11 18.5 20.29L12.77 21.94Q12.65 21.97 12.5 22H12.28Q11.95 22 11.68 21.91 11.41 21.82 11.13 21.67L7.38 19.55Q7.17 19.43 7.05 19.24 6.93 19.05 6.93 18.81 6.93 18.45 7.19 18.2 7.44 17.95 7.8 17.95H12.66V6.14L9 7.44Q8.57 7.6 8.3 8 8.03 8.38 8.03 8.85V15.58Q8.03 16 7.82 16.34 7.62 16.68 7.25 16.88L5.53 17.82Q5.29 17.95 5.05 17.95 4.64 17.95 4.35 17.66 4.06 17.37 4.06 16.95V7.47Q4.06 6.95 4.33 6.5 4.61 6 5.06 5.74L11.22 2.24Q11.43 2.12 11.67 2.06 11.91 2 12.15 2 12.32 2 12.46 2.03 12.6 2.05 12.77 2.1L18.5 3.69Q18.83 3.78 19.09 3.96 19.35 4.14 19.54 4.39 19.74 4.65 19.84 4.95 19.94 5.26 19.94 5.59M18.62 18.39V5.59Q18.62 5.36 18.5 5.19 18.35 5 18.13 4.96L15.31 4.18Q15 4.09 14.65 4 14.32 3.89 14 3.81V20.21L18.13 19Q18.35 18.96 18.5 18.79 18.62 18.62 18.62 18.39Z"
            />
          </svg>
          <span>Microsoft Office</span>
        </a>
        <a href="https://www.npmjs.com/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M4,10V14H6V11H7V14H8V10H4M9,10V15H11V14H13V10H9M12,11V13H11V11H12M14,10V14H16V11H17V14H18V11H19V14H20V10H14M3,9H21V15H12V16H8V15H3V9Z"
            />
          </svg>
          <span>npm</span>
        </a>
        <a href="https://www.sap.com/" target="_blank">
          <svg
            fill="#000000"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            width="96px"
            height="96px"
          >
            <path
              d="M 0 6 L 0 18 L 13 18 L 24 6 Z M 4.199219 9 C 5.898438 9 6.449219 9.398438 6.449219 9.398438 C 6.449219 9.398438 6.148438 10.152344 6 10.550781 C 5.5 10.351563 3.5 10 3.5 10.75 C 3.5 11.050781 3.601563 11.25 5.101563 11.597656 C 5.699219 11.75 6.601563 12.050781 6.800781 12.949219 L 8.351563 9 L 10.097656 9 L 12 13.75 L 12 9 L 14.25 9 C 15.5 9 16.5 10 16.5 11.25 C 16.5 12.5 15.5 13.5 14.25 13.5 L 13.5 13.5 L 13.5 15 L 10.75 15 L 10.449219 14.097656 C 10.097656 14.25 9.699219 14.347656 9.25 14.347656 C 8.800781 14.347656 8.402344 14.25 8.050781 14.097656 L 7.75 15 L 6 15 L 6.25 14.402344 C 5.800781 14.75 5.097656 15 4.199219 15 C 2.550781 15 2 14.550781 2 14.550781 L 2.398438 13.25 C 3.351563 13.851563 5.050781 13.75 5.050781 13.25 C 5.050781 12.75 4.300781 12.699219 3.300781 12.402344 C 2.351563 12.101563 2 11.347656 2 10.699219 C 2 10.050781 2.5 9 4.199219 9 Z M 13.5 10.5 L 13.5 12 L 14.25 12 C 14.648438 12 15 11.648438 15 11.25 C 15 10.851563 14.648438 10.5 14.25 10.5 Z M 9.25 10.699219 L 8.5 12.847656 C 8.699219 13 8.949219 13.050781 9.25 13.050781 C 9.550781 13.050781 9.800781 13 10 12.847656 Z"
            />
          </svg>
          <span>SAP</span>
        </a>
        <a href="https://www.adobe.com/products/photoshop.html" target="_blank">
          <svg
            fill="#000000"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            width="96px"
            height="96px"
          >
            <path
              d="M 5 3 C 3.9 3 3 3.9 3 5 L 3 19 C 3 20.1 3.9 21 5 21 L 19 21 C 20.1 21 21 20.1 21 19 L 21 5 C 21 3.9 20.1 3 19 3 L 5 3 z M 6.890625 8 L 9.5898438 8 C 11.915844 8 12.193359 10.140469 12.193359 10.605469 C 12.192359 12.465469 10.891641 13.115234 9.6816406 13.115234 L 8.5644531 13.115234 L 8.5644531 15.90625 L 6.890625 15.90625 L 6.890625 8 z M 8.5644531 9.3027344 L 8.5644531 11.814453 L 9.6816406 11.814453 C 10.425641 11.814453 10.611328 11.256469 10.611328 10.605469 C 10.612328 9.9534687 10.333641 9.3027344 9.6816406 9.3027344 L 8.5644531 9.3027344 z M 15.169922 9.953125 C 16.564922 9.953125 17.308594 10.791453 17.308594 11.814453 L 15.728516 11.814453 C 15.728516 11.349453 15.541922 11.070312 15.169922 11.070312 C 14.890922 11.070312 14.611328 11.256906 14.611328 11.628906 C 14.611328 12.558906 17.310547 12.279172 17.310547 14.326172 C 17.309547 15.721172 15.913922 16 15.169922 16 C 13.681922 16 12.9375 14.976875 12.9375 14.046875 L 14.425781 14.046875 C 14.425781 14.790875 14.983922 14.884766 15.169922 14.884766 C 15.541922 14.884766 15.820313 14.698172 15.820312 14.326172 C 15.820312 13.489172 13.121094 13.581703 13.121094 11.720703 C 13.121094 10.325703 14.424922 9.953125 15.169922 9.953125 z"
            />
          </svg>
          <span>Adobe Photoshop</span>
        </a>
        <a href="https://www.vegascreativesoftware.com/us/" target="_blank">
          <svg
            fill="#000000"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            width="96px"
            height="96px"
          >
            <path
              d="M 4.085938 1 C 2.921875 1.015625 1.984375 2 2 3.15625 L 2 20.867188 C 2 21.234375 2.09375 21.59375 2.269531 21.910156 C 2.269531 21.914063 2.269531 21.914063 2.269531 21.914063 C 2.832031 22.925781 4.148438 23.296875 5.15625 22.71875 L 21.03125 13.683594 C 21.035156 13.679688 21.039063 13.679688 21.042969 13.675781 C 21.335938 13.503906 21.578125 13.257813 21.75 12.953125 C 22.265625 12.035156 21.949219 10.847656 21.035156 10.320313 C 21.035156 10.320313 21.03125 10.316406 21.03125 10.316406 L 5.15625 1.28125 C 4.828125 1.09375 4.457031 0.996094 4.085938 1 Z M 4.109375 3 C 4.128906 3 4.144531 3.003906 4.160156 3.015625 C 4.160156 3.015625 4.164063 3.015625 4.164063 3.015625 L 19.941406 12 L 7 19.371094 L 7 16.671875 L 11 14.390625 L 11 12.074219 L 7 14.34375 L 7 9.132813 C 7 9.0625 7.046875 9.003906 7.152344 9.007813 L 11 11.269531 L 11 9.351563 C 11 9.222656 11.035156 9.105469 11.066406 8.988281 L 8.15625 7.28125 C 7.832031 7.09375 7.492188 7.015625 7.085938 7 C 5.921875 7.015625 4.984375 7.980469 5 9.140625 L 5 15.480469 L 4.085938 15.996094 L 4 15.875 L 4 3.140625 C 4 3.136719 4 3.132813 4 3.128906 C 4 3.042969 4.046875 3 4.109375 3 Z M 12.304688 9 C 12.132813 9.003906 11.996094 9.15625 12 9.34375 L 12 14.65625 C 12 14.71875 12.011719 14.777344 12.042969 14.832031 C 12.125 14.992188 12.3125 15.046875 12.460938 14.953125 L 16.871094 12.242188 C 16.910156 12.21875 16.945313 12.183594 16.96875 12.140625 C 17.039063 12.003906 16.992188 11.835938 16.871094 11.757813 L 12.460938 9.046875 C 12.414063 9.015625 12.359375 9 12.304688 9 Z M 5 17.785156 L 5 20.507813 L 4.164063 20.984375 C 4.164063 20.984375 4.160156 20.984375 4.160156 20.984375 C 4.097656 21.023438 4.058594 21.011719 4.015625 20.9375 C 4.003906 20.917969 4 20.894531 4 20.875 C 4 20.871094 4 20.871094 4 20.867188 L 4 17.984375 C 4.039063 17.988281 4.078125 18 4.117188 18 C 4.421875 18 4.71875 17.917969 5 17.785156 Z"
            />
          </svg>
          <span>Sony Vegas</span>
        </a>
        <a href="https://www.blender.org/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M12.58,3.12V3.13C12.27,3.13 11.96,3.22 11.71,3.39C11.21,3.74 11.15,4.32 11.6,4.69L14.46,7L5.73,7.03H5.72C5,7.03 4.3,7.5 4.16,8.1C4,8.71 4.5,9.22 5.26,9.22L9.69,9.21L1.76,15.3C1,15.87 0.77,16.82 1.24,17.42C1.72,18.03 2.73,18.03 3.5,17.42L7.8,13.89C7.8,13.89 7.73,14.37 7.74,14.65C7.74,14.94 7.84,15.5 7.97,15.93C8.26,16.86 8.75,17.71 9.43,18.46C10.13,19.23 11,19.85 12,20.29C13.03,20.76 14.17,21 15.34,21C16.5,21 17.65,20.75 18.69,20.28C19.69,19.84 20.55,19.21 21.25,18.44C21.93,17.69 22.42,16.83 22.71,15.91C22.85,15.44 22.94,14.97 23,14.5C23,14.03 23,13.56 22.94,13.09C22.81,12.18 22.5,11.32 22,10.54C21.56,9.83 21,9.2 20.31,8.67V8.67L13.42,3.38C13.19,3.21 12.89,3.12 12.58,3.12M15.34,9.21C16.5,9.21 17.59,9.59 18.46,10.29C18.9,10.65 19.25,11.07 19.5,11.54C19.77,12 19.94,12.55 20,13.11C20.04,13.67 19.96,14.23 19.77,14.77C19.57,15.31 19.25,15.81 18.82,16.26C17.93,17.16 16.69,17.68 15.34,17.68C14,17.68 12.75,17.17 11.86,16.27C11.43,15.83 11.11,15.32 10.91,14.78C10.72,14.25 10.64,13.69 10.69,13.12C10.74,12.56 10.91,12.03 11.17,11.55C11.43,11.08 11.79,10.66 12.23,10.3C13.09,9.59 14.19,9.21 15.34,9.21M15.44,10.61C14.66,10.61 13.94,10.89 13.41,11.34C12.87,11.8 12.5,12.44 12.47,13.18C12.43,13.93 12.73,14.63 13.26,15.15C13.8,15.68 14.58,16 15.44,16C16.3,16 17.07,15.68 17.62,15.15C18.15,14.63 18.45,13.93 18.41,13.18C18.37,12.44 18,11.8 17.47,11.34C16.94,10.89 16.22,10.61 15.44,10.61Z"
            />
          </svg>
          <span>Blender</span>
        </a>
      </div>
      <h2>Version Control Systems</h2>
      <div class="icon-box">
        <a href="https://git-scm.com/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M2.6,10.59L8.38,4.8L10.07,6.5C9.83,7.35 10.22,8.28 11,8.73V14.27C10.4,14.61 10,15.26 10,16A2,2 0 0,0 12,18A2,2 0 0,0 14,16C14,15.26 13.6,14.61 13,14.27V9.41L15.07,11.5C15,11.65 15,11.82 15,12A2,2 0 0,0 17,14A2,2 0 0,0 19,12A2,2 0 0,0 17,10C16.82,10 16.65,10 16.5,10.07L13.93,7.5C14.19,6.57 13.71,5.55 12.78,5.16C12.35,5 11.9,4.96 11.5,5.07L9.8,3.38L10.59,2.6C11.37,1.81 12.63,1.81 13.41,2.6L21.4,10.59C22.19,11.37 22.19,12.63 21.4,13.41L13.41,21.4C12.63,22.19 11.37,22.19 10.59,21.4L2.6,13.41C1.81,12.63 1.81,11.37 2.6,10.59Z"
            />
          </svg>
          <span>Git</span>
        </a>
        <a href="https://github.com/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z"
            />
          </svg>
          <span>GitHub</span>
        </a>
        <a href="https://about.gitlab.com/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
              d="M21.94 13.11L20.89 9.89C20.89 9.86 20.88 9.83 20.87 9.8L18.76 3.32C18.65 3 18.33 2.75 17.96 2.75C17.6 2.75 17.28 3 17.17 3.33L15.17 9.5H8.84L6.83 3.33C6.72 3 6.4 2.75 6.04 2.75H6.04C5.67 2.75 5.35 3 5.24 3.33L3.13 9.82C3.13 9.82 3.13 9.83 3.13 9.83L2.06 13.11C1.9 13.61 2.07 14.15 2.5 14.45L11.72 21.16C11.89 21.28 12.11 21.28 12.28 21.15L21.5 14.45C21.93 14.15 22.1 13.61 21.94 13.11M8.15 10.45L10.72 18.36L4.55 10.45M13.28 18.37L15.75 10.78L15.85 10.45H19.46L13.87 17.61M17.97 3.94L19.78 9.5H16.16M14.86 10.45L13.07 15.96L12 19.24L9.14 10.45M6.03 3.94L7.84 9.5H4.23M3.05 13.69C2.96 13.62 2.92 13.5 2.96 13.4L3.75 10.97L9.57 18.42M20.95 13.69L14.44 18.42L14.46 18.39L20.25 10.97L21.04 13.4C21.08 13.5 21.04 13.62 20.95 13.69"
            />
          </svg>
          <span>GitLab</span>
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

#about-me {
  padding: 60px;
  a {
    text-decoration: none;
    color: #ffffff;
  }
}

h2 {
  margin: 100px 0 20px 0;
}

p {
  text-align: justify;
}

#language-flex {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: stretch;
  margin-bottom: 60px;
  gap: 20px;
  // p {
  //   max-width: 300px;
  // }
}

#language-desc {
  gap: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  max-width: 300px;
}

#language-box {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 420px;
  flex-grow: 2;
}

.language {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 10px;
  img {
    zoom: 40%;
  }
}

#about-p p a {
  &:hover {
    // border: 2px solid $bg1;
    // border-style: none none solid none;
    text-decoration: underline;
    text-decoration-thickness: 2px;
    color: $bg2;
  }
  // padding: -5px;
}

#skills {
  margin-bottom: -60px;
}

.icon-box {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  gap: 60px;
  margin: 0 40px 0 40px;
  svg {
    width: 100px;
    fill: $bg1;
  }
  a {
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: transform 0.15s ease-out;
    flex-grow: 1;
    span {
      text-align: center;
    }
    &:hover {
      transform: scale(1.1);
      svg {
        fill: white;
      }
      span {
        color: white;
      }
    }
  }
}

#about {
  background-color: $primary;
  color: $bg1;
  z-index: 2;
  //   height: 110vh;
}
#down {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  svg {
    fill: $bg1;
    width: 70px;
    transition: transform 0.1s ease-out;
  }
  &:hover {
    svg {
      fill: $bg2;
      transform: translateY(10px);
    }
  }
}

@media only screen and (min-width: 1300px ) {
  #language-desc {
    max-width: 500px;
    justify-content: flex-start;
  }
}
@media only screen and (min-width: 2040px ) {
  #language-desc {
    max-width: 1000px;
  }
}
</style>