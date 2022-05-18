<script setup lang="ts">

</script>

<script lang="ts" setup>
const down1 = ref()
const down2 = ref()
function scrollFirst(a, b) {
  down1.value.scrollIntoView({
    behavior: 'smooth',
    block: 'start',
  })
}

function scrollSecond(a, b) {
  down2.value.scrollIntoView({
    behavior: 'smooth',
    block: 'start',
  })
}
</script>

<template lang="pug">
main
  div.p-5.absolute.flex.w-full.justify-center.border-box.items-center.flex-wrap(class="md:justify-between")
    h1.m-0.mr-2 webxdc
    div.flex
      Link(href="https://github.com/webxdc" icon="carbon-logo-github" text="webxcd")
      Link(href="https://github.com/webxdc" icon="carbon-book" text="book")

      //a(href="" i="") book
  div.h-screen.flex.items-center.justify-center
    div.downbutton(i="carbon-arrow-down" @click="scrollFirst")
    div#banner.p-2.text-center.rainbow-box.rounded(class="md:p-10 md:m-2")
      h2 Bring messaging to a new level
      p.mb-0 webxdc is empowering developers to create rich interactive content using already known web-technologies and to share them with the world like never before

  #explanation.flex.p-2.flex-wrap.relative(ref="down1")
    div.downbutton(i="carbon-arrow-down" @click="scrollSecond")
    #steps.flex.flex-col.justify-center
      div
        h2.bold.mb-0.text-3xl.ml-2 Three simple steps:
        div.flex.flex-col.flex-grow.py-5
          div.modal
            h3.text-2xl.mt-0 1. Use DeltaChat version 1.30
            p The newest deltachat version is available for all major platforms
              |
              |
              a(href="https://delta.chat/en/download") here.
          div.modal
            h3.text-2xl 2. Develop your own rich content
            p We created a template for you to start developing cool & exciting rich content now.
            p There are also plenty of
              |
              |
              a(href="https://github.com/webxdc") examples
              |
              | to get you started.
              a(href="")
          div.modal
            h3.text-2xl 3. Share what you built
            p Just drag and drop your bundled *.xdc file into a chat and share it with the world!

    div.flex.items-center.justify-center.flex-grow(class="md:p-15")
      iframe#video.rounded.shadow-xl(src="https://www.youtube.com/embed/I1K4pBvb2pI" frameborder="0" allowfullscreen)

  div.h-screen.flex.justify-center(ref="down2")
    div.p-2
      h2 Ressources
      p We created documentation and many examples to get you startd as easily as possible.
      h2 API
      p You can find the API documentation in our official
        |
        |
        a(href="https://github.com/deltachat/deltachat-core-rust/blob/master/draft/webxdc-dev-reference.md")
          | Github Repo.
      p
        | For a more thorough introduction see our
        |
        a(href="https://deltachat.github.io/webxdc_docs/") book

      h2 Examples
      p There are plenty of examples under the webxdc
        |
        |
        a(href="https://github.com/webxdc") organisation.

      h2 Getting Started
      p Start right off by cloning our
        |
        |
        a(href="https://github.com/webxdc/webxdc-dev") boostrap repo.
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

.downbutton
  transition: all 0.3s ease
  @apply absolute text-3xl bottom-0 right-0 mr-4 mb-5 hover:text-4xl cursor-pointer

#steps
  width: 40%
  p
    @apply ml-4

@media screen and (max-width: 768px)
  #steps
    width: 100%

#video
  width: 100%
  aspect-ratio: 16 / 10

.modal
  @apply shadow-xl border-rounded p-5 m-2 bg-white text-black

#explanation
  min-height: 100vh
  background: rgb(15 39 78)
  h3
    color: var(--accent)
    margin-top: 0px

.rainbow-box
  border: 5px solid transparent
  border-image: linear-gradient(to bottom right, #b827fc 0%, #2c90fc 25%, #b8fd33 50%, #fec837 75%, #fd1892 100%)
  border-image-slice: 1

.border-box
  box-sizing: border-box
</style>
