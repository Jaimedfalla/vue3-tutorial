<template>
  <div class="App">
    <main>
      <router-view :key="$route.fullPath"></router-view>
    </main>
  </div>
</template>
<style>
:root {
  --font-primary: Lato,Roboto,Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
  --font-display: "IBM Plex Sans",Roboto,Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
  --font-code: "IBM Plex Mono",Menlo,Monaco,Consolas,"Liberation Mono","Courier New",monospace;
  --font-size-xs: 1.15rem;
  --font-size-sm: 1.3rem;
  --font-size-md: 1.5rem;
  --font-size-lg: 1.8rem;
  --font-size-xl: 2.4rem;
  --line-height: 1.6;
  --color-back: #fff;
  --color-front: #444;
  --color-theme: #09a3d5;
  --color-theme-dark: #1095bf;
  --color-theme-contrast: #fff;
  --color-subtle-dark: #777;
  --color-subtle-medium: #eee;
  --color-subtle-light: #f9f9f9;
  --color-background-code: rgba(122,129,129,0.09);
  --color-button-primary: #29c15b;
  --color-button-primary-contrast: #fff;
  --color-button-secondary: #cdcdd4;
  --color-button-secondary-contrast: #686873;
  --color-button-danger: #d21313;
  --color-button-danger-contrast: #fff;
  --color-correct-light: #e3fde8;
  --color-correct-dark: #007737;
  --color-incorrect-light: #fde7e7;
  --color-incorrect-dark: #d21313;
  --syntax-background: #f7f7f7;
  --syntax-text: #403f53;
  --syntax-selected-background: rgba(122,129,129,0.17);
  --syntax-comment: #989fb1;
  --syntax-tag: #994cc3;
  --syntax-number: #aa0982;
  --syntax-selector: #994cc3;
  --syntax-operator: #994cc3;
  --syntax-function: #4876d6;
  --syntax-keyword: #994cc3;
  --syntax-regex: #5ca7e4;
  --ansi-green: #12dc55;
  --ansi-red: #f76464;
  --ansi-cyan: #00d8ff;
  --plyr-color-main: var(--color-theme);
  --plyr-font-family: var(--font-primary);
  --width-container: 800px;
  --size-profile-pic: 125px;
  --border-radius: 5px;
}
html, body {
  font-size: 14px;
  font-family: var(--font-display);
  line-height: var(--line-height);
}
a {
  background-color: transparent;
  color: inherit;
}
h1, h2 {
  font-family: var(--font-primary);
}
h1 {
  font-size: var(--font-size-xl);
  margin-bottom: 2rem;
}
h2 {
  font-size: var(--font-size-lg);
  margin-bottom: 1.5rem;
}
.underline {
  text-decoration: underline;
}
.no-underline {
  text-decoration: none;
}
.cursor-pointer {
  cursor: pointer;
}
.page {
  width: var(--width-container);
  max-width: 100%;
  margin: 0 auto;
}
.summary {
  border: 1px solid var(--color-subtle-medium);
  border-radius: var(--border-radius);
  margin: 0 auto 2rem;
}
.summary > div {
  padding: 2rem;
}
.summary .title {
  display: flex;
  justify-content: space-between;
}
.summary .title svg {
  height: 25px;
  width: 25px;
  color: var(--color-subtle-medium);
}
.summary .title svg.enrolled {
  color: var(--color-theme-dark);
}
.summary .title svg.complete {
  color: var(--color-button-primary);
}
.summary p {
  font-size: var(--font-size-sm);
  color: var(--color-subtle-dark);
  margin: 0;
}
.Lesson header,
.Course header {
  margin-bottom: 2rem;
}
.Home header h1 {
  text-align: center;
}
.page header p {
  font-size: var(--font-size-xs);
  color: var(--color-subtle-dark);
}
.button.auth {
  padding: 0.75rem 1.5rem;
  font-size: var(--font-size-xs);
  background: var(--color-subtle-medium);
  border: 0;
  font-family: var(--font-primary);
  font-weight: 700;
  border-radius: var(--border-radius);
  transition: opacity .2s ease;
  cursor: pointer;
}
.button.primary {
  padding: 1rem 1.5rem;
  font-size: var(--font-size-xs);
  background: var(--color-theme);
  color: var(--color-theme-contrast);
  border: 0;
  font-family: var(--font-primary);
  font-weight: 700;
  border-radius: var(--border-radius);
  transition: opacity .2s ease;
  cursor: pointer;
  text-decoration: none;
  line-height: 1.2;
}
.button.primary:hover {
  background: var(--color-theme-dark);
}
.button.primary.icon {
  display: inline-flex;
}
.button.primary.icon svg {
  margin-left: 7px;
  height: 20px;
  width: 20px;
}
@keyframes spinner {
  from {
    transform: rotate(0turn);
  }
  to {
    transform: rotate(1turn);
  }
}
</style>