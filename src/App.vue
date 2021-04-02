<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3>{{goal.goal}}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button @click="toggleGoal">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
  setup(){
    //separate refs
    // const goal = ref('Become the best developer');

    // const toggleGoal = () => {
    //   goal.value = "Retire at an early age"
    // }

    //ref object
    const obj = ref({
      goal: 'Become the best developer',
    });

    const toggleGoal = () => {
      obj.value.goal = "Retire at an early age"
    }


    return {goal: obj, toggleGoal}
  }
}
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>