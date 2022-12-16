<template>
  <h1>{{testState}}</h1>
  <p>{{testObj.a}}</p>
  <p>{{testArr[0]}}</p>
  <p>{{testArr2[0].head}}</p>
  <p>{{toDos[0].text}}</p>
  <ul id="toDoList" class="item-{{$index}}">
    <li v-repeat="toDos">{{$index}} - {{ text }} {{ details }}</li>
  </ul>
  <button v-on:click="addLI()">add li</button>
  <ul id="tags">
  <li v-repeat="tags">
    {{$value}}
  </li>
</ul>
</template>

<script>
export default {
  data() {
    return {
      toDos: [
        { text: "cook dinner", details: "pasta bolognese would be nice" },
        { text: "feed the cat", details: "that little piece of shit" },
      ],
      testState: "hrloooo",
      testObj: {a: 1, b: 2},
      testArr: [1, 2, 3],
      testArr2: [{head: "head", tail: "tail"}],
      el: '#tags',
      data: {
        tags: ['JavaScript', 'MVVM', 'Vue.js']
      }
    };
  },

  methods: {
    addLI() {
      this.toDos.push({text: "another task", details: "the struggle never ends"});
    },
  },
};
</script>
