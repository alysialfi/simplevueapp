<template>
    <div class="container">
        <h3>Conditional Rendering</h3>
        <div class="box">
            <div class="first-match">
                First match: <span id="first_match">{{ firstMatch }}</span>
            </div>
            <div class="second-match">
                <div>
                    Second match: <span id="second_match">{{ secondMatch }}</span>
                </div>
                <button type="button" id="btn-counter" @click="secondMatch += 1">+</button>
            </div>
            <div v-if="secondMatch >= 10" class="result">
                Result: <span id="result">{{ firstMatch + secondMatch }}</span>
            </div>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ConditionalRendering',
    data() {
      return {
          firstMatch: 21,
          secondMatch: 3,
      }
    },
  }
  </script>
  
  <style scoped>
      .container {
          display: flex;
          justify-content: center;
          flex-direction: column;
          align-items: center;
      }
      .box {
          width: 20%;
          border: 2px solid rgb(46, 46, 46);
          border-radius: 4px;
          text-align: left;
          padding: 8px;
      }
      .second-match {
          display: flex;
          justify-content: space-between;
      }
      .first-match {
          color: rgb(155, 155, 155);
      }
      .result {
          margin-top: 8px;
          font-size: 20px;
          font-weight: bold;
      }
  </style>
  