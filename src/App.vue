<script setup>
  import T01vbind from './components/T01vbind.vue';
  import T02vbind from './components/T02vbind.vue';
  import T03vbind from './components/T03vbind.vue';
  import T04vif from './components/T04vif.vue';
  import T05vif from './components/T05vif.vue';
  import T06vshow from './components/T06vshow.vue';
  import T07vshow from './components/T07vshow.vue';
  import T08vfor from './components/T08vfor.vue';
  import T09vfor from './components/T09vfor.vue';
  import T10vfor from './components/T10vfor.vue';
  import T11von from './components/T11vonclick.vue';
  import T12voninput from './components/T12voninput.vue';
  import T13vonmousemove from './components/T13vonmousemove.vue';
  import T14vonvfor from './components/T14vonvfor.vue';
  import T15vonShorthand from './components/T15vonShorthand.vue';
  import T16methods from './components/T16methods.vue';
  import T17methodsEvent from './components/T17methodsEvent.vue';
  import T18methodsTextArea from './components/T18methodsTextArea.vue';
  import T19methodsArguments from './components/T19methodsArguments.vue';
  import T20methodsArgumentsObjects from './components/T20methodsArgumentsObjects.vue';
  import T21methodsExample from './components/T21methodsExample.vue';
  import T22eventModifiers from './components/T22eventModifiers.vue';
  import T23eventModifiersKeyUp from './components/T23eventModifiersKeyUp.vue';
  import T24eventModifiersCombined from './components/T24eventModifiersCombined.vue';
  import T25eventModifiersMouseButton from './components/T25eventModifiersMouseButton.vue';
  import T26eventModifiersImages from './components/T26eventModifiersImages.vue';
  import T27forms from './components/T27forms.vue';
  import T28vmodel from './components/T28vmodel.vue';
  import T29vmodelFormsCheckbox from './components/T29vmodelFormsCheckbox.vue';
  import T30vmodelForms from './components/T30vmodelForms.vue';
</script>
<script>
  export default {
    name: 'App',
    components : {},
    data() {
      return {
        bgColor: "greenyellow"
    }
   }
  }  
</script>

<template>
  <h1 v-bind:style="{ backgroundColor: bgColor }">01. "v-bind:" Examples </h1>
  <T01vbind></T01vbind>
  <h1 v-bind:style="{ backgroundColor: bgColor }">02. "v-bind:" Conditional styles </h1>
  <T02vbind></T02vbind>
  <h1 :style="{ backgroundColor: bgColor }">03. "v-bind:" Shorthand form </h1>
  <T03vbind></T03vbind>
  <h1 :style="{ backgroundColor: bgColor }">04. "v-if:" Conditional rendering </h1>
  <T04vif></T04vif>
  <h1 :style="{ backgroundColor: bgColor }">05. "v-if:" Returning value from a function </h1>
  <T05vif></T05vif>
  <h1 :style="{ backgroundColor: bgColor }">06. "v-show:" Conditional visibility </h1>
  <T06vshow></T06vshow>
  <h1 :style="{ backgroundColor: bgColor }">07. "v-show:" v-show vs. v-if </h1>
  <T07vshow></T07vshow>
  <h1 :style="{ backgroundColor: bgColor }">08. "v-for:" List rendering </h1>
  <T08vfor></T08vfor>
  <h1 :style="{ backgroundColor: bgColor }">09. "v-for:" Images and text (Javascript objects) </h1>
  <T09vfor></T09vfor>
  <h1 :style="{ backgroundColor: bgColor }">10. "v-for:" Displaying the INDEX </h1>
  <T10vfor></T10vfor>
  <h1 :style="{ backgroundColor: bgColor }">11. "v-on:" Events - click</h1>
  <T11von></T11von>
  <h1 :style="{ backgroundColor: bgColor }">12. "v-on:" Events - input </h1>
  <T12voninput></T12voninput>
  <h1 :style="{ backgroundColor: bgColor }">13. "v-on:" Events - mousemove </h1>
  <T13vonmousemove></T13vonmousemove>
  <h1 :style="{ backgroundColor: bgColor }">14. "v-on:" Events - v-on & v-for </h1>
  <T14vonvfor></T14vonvfor>
  <h1 :style="{ backgroundColor: bgColor }">15. "v-on:" Shorthand @: </h1>
  <T15vonShorthand></T15vonShorthand>
  <h1 :style="{ backgroundColor: bgColor }">16. Methods </h1>
  <T16methods></T16methods>
  <h1 :style="{ backgroundColor: bgColor }">17. Methods with the "event" object </h1>
  <T17methodsEvent></T17methodsEvent>
  <h1 :style="{ backgroundColor: bgColor }">18. Methods: textarea </h1>
  <T18methodsTextArea></T18methodsTextArea>
  <h1 :style="{ backgroundColor: bgColor }">19. Methods: passing arguments </h1>
  <T19methodsArguments></T19methodsArguments>
  <h1 :style="{ backgroundColor: bgColor }">20. Methods: passing arguments and the Event object </h1>
  <T20methodsArgumentsObjects></T20methodsArgumentsObjects>
  <h1 :style="{ backgroundColor: bgColor }">21. Methods: Larger example </h1>
  <T21methodsExample></T21methodsExample>
  <h1 :style="{ backgroundColor: bgColor }">22. Event modifiers </h1>
  <T22eventModifiers></T22eventModifiers>
  <h1 :style="{ backgroundColor: bgColor }">23. Event modifiers: keyup, keydown </h1>
  <T23eventModifiersKeyUp></T23eventModifiersKeyUp>
  <h1 :style="{ backgroundColor: bgColor }">24. Event modifiers combined </h1>
  <T24eventModifiersCombined></T24eventModifiersCombined>
  <h1 :style="{ backgroundColor: bgColor }">25. Event modifiers: Mouse button </h1>
  <T25eventModifiersMouseButton></T25eventModifiersMouseButton>
  <h1 :style="{ backgroundColor: bgColor }">26. Event modifiers: Images </h1>
  <T26eventModifiersImages></T26eventModifiersImages>
  <h1 :style="{ backgroundColor: bgColor }">27. "v-model:" Forms </h1>
  <T27forms></T27forms>
  <h1 :style="{ backgroundColor: bgColor }">28. "v-model:" Checkbox </h1>
  <T28vmodel></T28vmodel>
  <h1 :style="{ backgroundColor: bgColor }">29. "v-model:" Forms with Checkbox </h1>
  <T29vmodelFormsCheckbox></T29vmodelFormsCheckbox>
  <h1 :style="{ backgroundColor: bgColor }">30. "v-model:" Forms with found items </h1>
  <T30vmodelForms></T30vmodelForms>
</template>

<style scoped>

</style>
