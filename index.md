---
layout: home
---
<section id="featured">
  <h2>Featured</h2>
  <div class="multi-column">
  {% assign featured_posts = (site.posts | where:"featured", "true") %}
  {% for post in featured_posts %}
      <div class="article-info">
        <h3>{{ post.title }}</h3>
        <p>{{ post.lede }}</p>
        <div class="leader-link"><a href="{{ post.url }}">Read more</a></div>
      </div>
  {% endfor %}
  </div>
</section>

<section id="backfile">
  <h2>More posts</h2>
  <ul class="post-list">
    {% for entry in site.data.toc %}
    <li>
        <a href="{{ entry.url }}">{{ entry.title }}</a> <span>{{entry.date | date_to_long_string}}</span>
    </li>
    {% endfor %}
  </ul>
</section>

<section id="resources">
  <h2>Resources</h2>
  <section>
    <h3>Data Dictionary</h3>
    <p>A reference resource for those interested in using the open data from the New York Public Library's menu transcription project.</p>
    <div class="leader-link"><a href="/data_dictionary">View</a></div>
  </section>
</section>

<section id="about">
  <h2>About</h2>
  <div class="multi-column">
    <section class="about-part">
      <h3>The Collection</h3>
      <p>The <a href="http://legacy.www.nypl.org/research/chss/grd/resguides/menus/index.html">New York Public Library Rare Book Division</a> holds over 45,000 historical menus. About half of these were collected and curated by Frank E. Buttolph between 1900 and 1921. The menus date from the 1850s to the present and include menus from restaurant, railroad and steamship companies, as well as a range of other organizations.</p>
    </section>
    <section class="about-part">
      <h3>The Crowd</h3>
      <p>Beginning in 2011, menus from the NYPL's collection were digitized and transcribed with the help of thousands of volunteers. Through the NYPL’s <a href="http://menus.nypl.org/">What’s on the Menu?</a> project, volunteers looked at digitized copies of the menus and typed in the many pieces of information included on each one, such as restaurant names, locations, dishes, prices, and dates. </p>
    </section>
    <section class="about-part">
      <h3>The Data</h3>
      <p>The <em>What's on the Menu?</em> project makes all the data from its crowdsourced transcriptions available via <a href="http://menus.nypl.org/data">bulk downloads</a> and via an <a href="http://nypl.github.io/menus-api/">application programming interface (API)</a>. The current data set includes around 400,000 data points from the transcription project and the library's metadata on the over 17,000 menus digitized so far.</p>
    </section>
  </div>
  <section class="about-part bio">
    <h3>The Researchers</h3>
    {% assign author1 = site.data.authors['KR'] %}
    {% assign author2 = site.data.authors['TM'] %}
    <p><span class="author-name">{{ author1.name }}</span> {{ author1.bio }}</p>
    <p><span class="author-name">{{ author2.name }}</span> {{ author2.bio }}</p>
  </section>
</section>
