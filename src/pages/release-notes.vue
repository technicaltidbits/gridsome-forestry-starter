<template>
  <Layout>
    <div class="container">
      <div class="notes-header">
        <h1 class="notes-title">Release notes</h1>
      </div>
      <h2>May 22, 2020 | Version 2.0.0 (is it okay to make such a big jump?)</h2>
      <p>Tada! A whole new look! I decided that although I liked Eleventy and Hylia, it wasn't the look that I really wanted. I've always been a fan of minimalistic, simple websites. The website now uses <a href="https://gridsome.org/">Gridsome</a>.</p>
      <h3>Content</h3>
      <ul>
        <li>
          Mostly migrated the Eleventy content. Added the first part of the Vue CLI tutorial to the front page, including a fancy image I made of the CLI using
          <a href="https://carbon.now.sh/">Carbon</a>.
        </li>
        <li>Updated the resources page to include a link to an article about user stories.</li>
        <li>Changed hover color for posts archive page from gray to blue.</li>
      </ul>
      <h3>Performance</h3>
      <ul>
          <li>Deleted unused images to keep the site from being bogged down.</li>
          <li>Decided to stick with using a basic, sans-serif font for the site.</li>
          <li>PageSpeed Insights currently at 100. I do see the Max Potential First Input Delay is at 160 ms, will figure out how to address later.</li>
      </ul>
      <h2>April 20, 2020 | Version 1.0.0</h2>
      <p>It's been a struggle, but at long last, this site is finally up and running &#x1F389 Overall, installing Eleventy and deploying to Netlify wasn't too bad, but there were a few hiccups along the way.</p>
      <h3>Content</h3>
      <ul>
        <li>Added a resources page that detailed books, websites, tools, and other suggestions.</li>
        <li>Wrote "welcome text" for the homepage.</li>
        <li>Changed highlight value from yellow to a lovely muted blue.</li>
      </ul>
      <h3>Performance</h3>
      <p>Analyzed Page Speed for the first time - currently sitting at 100. I'm aware there's not much here, but that's okay. Will try to keep it between 95 - 100 always.</p>
    </div>
  </Layout>
</template>