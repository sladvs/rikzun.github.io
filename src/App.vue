<template>
    <pre><span class="reserved">const</span> <span class="variable">me</span> = {
    <span class="param">firstName</span>: <span class="string">'Михаил'</span>,
    <span class="param">lastName</span>: <span class="string">'Якименко'</span>,
    <span class="param">age</span>: <span class="number">{{Math.floor((Date.now() - Date.parse('2000-12-11')) / 3154e7)}}</span>,
    <span class="param">sex</span>: <span class="string">'male'</span>,
    <span class="param">сity</span>: <span class="string">'Новороссийск'</span>,

    <span class="param">technicalSkills</span>: [
      <span class="string">'JavaScript'</span>, <span class="string">'TypeScript'</span>,
      <span class="string">'HTML'</span>, <span class="string">'CSS'</span>, <span class="string">'SCSS'</span>,
      <span class="string">'React'</span>, <span class="string">'Vue.js'</span>, 
      <span class="string">'Webpack'</span>, <span class="string">'Node.js'</span>, 
      <span class="string">'REST API'</span>
    ],

    <span class="param">familiarWith</span>: [
      <span class="string">'Nuxt.js'</span>,
      <span class="string">'Python'</span>,
      <span class="string">'C++'</span>,
      <span class="string">'C#'</span>
    ],

    <span class="param">workExperience</span>: [
      <span class="param">sevenWinds</span>: {
        <span class="param">position</span>: <span class="string">'Frontend React Developer'</span>,
        <span class="param">time</span>: <span class="string">'{{Math.ceil((Date.now() - 16230132e5) / (1000 * 3600 * 24))}} days'</span>
      }
    ]

    <span class="param">acceptable</span>: {
      <span class="param">kindОfWork</span>: [
        <span class="string">'Стажировка'</span>,
        <span class="string">'Частичная занятость'</span>,
        <span class="string">'Полная занятость'</span>
      ],
      <span class="param">workSchedule</span>: [
        <span class="string">'Полный день'</span>,
        <span class="string">'Сменный график'</span>,
        <span class="string">'Гибкий график'</span>,
        <span class="string">'Удаленная работа'</span>
      ]
    },

    <span class="param">desiredPositions</span>: [
      <span class="string">'Frontend Developer'</span>,
      <span class="string">'Frontend Vue Developer'</span>,
      <span class="string">'Frontend React Developer'</span>,
      <span class="string">'Backend JavaScript Developer'</span>,
      <span class="string">'Backend TypeScript Developer'</span>
    ],

    <span class="param">mail</span>: <span class="string">'<a href="mailto:rik.zunqq@gmail.com">rik.zunqq@gmail.com</a>'</span>,
    <span class="param">github</span>: <span class="string">'<a href="https://github.com/rikzun" target="_blank">https://github.com/rikzun</a>'</span>,
    <span class="param">linkedin</span>: <span class="string">'<a href="https://www.linkedin.com/in/rik-zun/" target="_blank">https://www.linkedin.com/in/rik-zun</a>'</span>
  }</pre>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class App extends Vue {}
</script>

<style lang="sass">
* 
  box-sizing: border-box

  &::selection
    background: #094771 !important
    border: 1px solid red

body
  margin: 0
  cursor: text
  color: white
  background-color: #1E1E1E
  font-family: Consolas, "Courier New", monospace

pre
  width: max-content
  white-space: pre-wrap
  line-height: 19px
  left: 0
  right: 0
  margin-inline: auto

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