<script setup lang="ts">

</script>

<template lang="pug">
main
  h1.pl-5.absolute webxdc
  div.h-screen.flex.items-center.justify-center
    div.absolute.text-3xl.bottom-0.right-0.mr-4.mb-5(i="carbon-arrow-down")
    div#banner.p-2.text-center.rainbow-box.rounded(class="md:p-10 md:m-2")
      h2 Bring messaging to a new level
      p.mb-0 webxdc is empowering developers to create rich interactive content using already known web-technologies and to share them with the world like never before

  div#explanation.flex.p-2.flex-wrap.relative
    div.absolute.text-3xl.bottom-0.right-0.mr-4.mb-5(i="carbon-arrow-down")
    div.flex.flex-col.steps-width
      h2.bold.mb-0.text-3xl Three simple steps:
      div.flex.flex-col.flex-grow.py-5
        div.extra
          h3.text-2xl.mt-0 1. Use Version 1.30
          p The newest deltachat-version is available for all mayor platforms.
        div.extra
          h3.text-2xl 2. Develop your own rich content
          p We created a template for you to start developing cool & exiting apps rich content now
          p There are also plenty of examples to get you started
            a(href="")
        div.extra
          h3.text-2xl 3. Share your App
          p Just drag and drop your bundled *.xdc file into a chat and publish it!

    div.flex.items-center.justify-center.flex-grow(class="md:p-15")
      iframe#video.rounded.shadow-xl(src="https://www.youtube.com/embed/I1K4pBvb2pI" frameborder="0" allowfullscreen)

  div.h-screen.flex.justify-center
    div.p-2
      h2 Ressources
      p We created documentation and many examples to got you onboard as easy as possible
      h2 API
      p You can finde the API-Documentation on our official &nbsp
        a(href="https://github.com/deltachat/deltachat-core-rust/blob/master/draft/webxdc-dev-reference.md")
          | Github Repo
      p
        | We have also written a &nbsp
        span
          a(href="https://deltachat.github.io/webxdc_docs/") book
        | &nbsp for a more thorough introduction
      h2 Examples
      p There are plenty of examples under the webxdc &nbsp
        a(href="https://github.com/webxdc") organisation

      h2 Getting Started
      p To start right off you can clone our &nbsp
        a(href="https://github.com/webxdc/webxdc-dev") boostrap-repo
</template>

<style lang="sass">
:root
  --bg-explanation: #299D61
  --color-light: #9ACE99
  --accent: #0a2e1b

#banner
  width: 40%

@media screen and (max-width: 400px)
  #banner
    width: 100%
    @apply m-2
.steps-width
  width: 40%
  p
    @apply ml-4

@media screen and (max-width: 768px)
  .steps-width
    width: 100%

#video
  width: 100%
  aspect-ratio: 16 / 10

.extra
  @apply shadow-xl border-rounded p-5 m-2 bg-white

#explanation
  min-height: 100vh
  background: #c0e1e9
  h3
    color: var(--accent)
    margin-top: 0px

  h2
    //color: #0d3a23

.rainbow-box
  border: 5px solid transparent
  border-image: linear-gradient(to bottom right, #b827fc 0%, #2c90fc 25%, #b8fd33 50%, #fec837 75%, #fd1892 100%)
  border-image-slice: 1
</style>
