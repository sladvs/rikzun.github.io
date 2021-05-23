<template>
    <pre><span class="reserved">const</span> <span class="variable">me</span> = {
    <span class="param">firstName</span>: <span class="string">'{{firstName}}'</span>,
    <span class="param">lastName</span>: <span class="string">'{{lastName}}'</span>,
    <span class="param">age</span>: <span class="number">20</span>,
    <span class="param">sex</span>: <span class="string">'male'</span>,
    <span class="param">сity</span>: <span class="string">'Новороссийск'</span>,

    <span class="param">skills</span>: [
      { <span class="param">name</span>: <span class="string">'JavaScript'</span>, <span class="param">lvl</span>: <span class="number">7</span> },
      { <span class="param">name</span>: <span class="string">'TypeScript'</span>, <span class="param">lvl</span>: <span class="number">6</span> },
      { <span class="param">name</span>: <span class="string">'Python'</span>, <span class="param">lvl</span>: <span class="number">4</span> },
      { <span class="param">name</span>: <span class="string">'HTML'</span>, <span class="param">lvl</span>: <span class="number">8</span> },
      { <span class="param">name</span>: <span class="string">'CSS'</span>, <span class="param">lvl</span>: <span class="number">7</span> },
      { <span class="param">name</span>: <span class="string">'SCSS'</span>, <span class="param">lvl</span>: <span class="number">6</span> },
      { <span class="param">name</span>: <span class="string">'Vue.js'</span>, <span class="param">lvl</span>: <span class="number">5</span> },
      { <span class="param">name</span>: <span class="string">'Nuxt.js'</span>, <span class="param">lvl</span>: <span class="number">4</span> },
      { <span class="param">name</span>: <span class="string">'Node.js'</span>, <span class="param">lvl</span>: <span class="number">4</span> },
      { <span class="param">name</span>: <span class="string">'REST API'</span>, <span class="param">lvl</span>: <span class="number">7</span> }
    ],

    <span class="param">workExperience</span>: <span class="reserved">null</span>,

    <span class="param">acceptable</span>: {
      <span class="param">kindОfWork</span>: [
        <span class="string">'Стажировка'</span>,
        <span class="string">'Частичная занятость'</span>,
        <span class="string">'Полная занятость'</span>
      ],
      <span class="param">workSchedule</span>: [ <span class="string">'Удаленная работа'</span> ]
    },

    <span class="param">desiredPositions</span>: [
      <span class="string">'Frontend Vue Developer'</span>,
      <span class="string">'Backend TypeScript Developer'</span>,
      <span class="string">'Backend JavaScript Developer'</span>,
      <span class="string">'Frontend Developer'</span>
    ],

    <span class="param">mail</span>: <span class="string">'<a href="mailto:rik.zunqq@gmail.com">rik.zunqq@gmail.com</a>'</span>,
    <span class="param">github</span>: <span class="string">'<a href="https://github.com/rikzun" target="_blank">https://github.com/rikzun</a>'</span>
  }</pre>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class App extends Vue {
  params = new URLSearchParams(document.location.search)
  firstName = this.params.get('fn') || 'Александр'
  lastName = this.params.get('ln') || 'Лень'
  age = Math.floor((Date.now() - Date.parse('11.12.2000')) / 3154e6)
}
</script>

<style lang="sass">
* 
  box-sizing: border-box

  &::selection
    background: #094771 !important
    border: 1px solid red

body
  margin: 0
  color: white

body
  display: flex
  align-items: center
  justify-content: center
  min-height: 100vh
  background-color: #1E1E1E
  cursor: text
  font-family: Consolas, "Courier New", monospace

pre
  white-space: pre-wrap
  margin: 0
  margin: 10px
  line-height: 19px

  > .reserved
    color: #569cd6

  > .variable
    color: #4FC1FF

  > .param
    color: #9CDCFE

  > .string
    color: #ce9178

  > .number
    color: #b5cea8

a
  text-decoration: underline
  text-underline-position: under
  cursor: pointer
  color: unset
</style>