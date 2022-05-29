<template>
  <section id="bio" class="bio content-container">
    <header>
      <h2 class="mark">A bit about me.</h2>
    </header>

    <article class="copy-container">
      <p>
        Hi, I'm Elizabeth &mdash; a <strong>makeup artist</strong> who blends
        the best of functional techniques and fx into compelling and engaging
        looks.
      </p>
      <p class="highlight">Art is what I live for.</p>
      <p>
        When I'm not hitting refresh on my Instagram feed or maxing out on
        design sketches, I'm probably watching documentaries, interesting videos
        on YouTube and TED Talks.
      </p>
    </article>

    <article class="media copy-container">
      <p>You can dive into my social media and have a looksee.</p>
      <Socials />
    </article>
  </section>
</template>

<script>
export default {
  name: 'AboutPageBio',
}
</script>

<style lang="scss" scoped>
header {
  width: fit-content;
  h2 {
    font-size: scale('h3');
    font-weight: 900;

    color: $neutral-500;
  }
}

.highlight {
  font-size: scale('h6');
  font-weight: 600;
  padding: $spacing-md 0;
}
</style>
