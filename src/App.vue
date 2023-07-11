<script>
import Button from "./components/Button.vue";
export default {
  data() {
    return {
      buttons: [
        {
          id: "1",
          buttonColor: "black",
          count: 0,
        },
        {
          id: "2",
          buttonColor: "black",
          count: 0,
        },
        {
          id: "3",
          buttonColor: "black",
          count: 0,
        },
        {
          id: "4",
          buttonColor: "black",
          count: 0,
        },
      ],
    };
  },
  methods: {
    ChangeColor(button) {
      button.count++;
      if (button.count >= 10) button.buttonColor = "+10";
    },
  },
  components: {
    Button,
  },
};
</script>

<template>
  <div class="box_buttons">
    <div class="button_container">
      <Button
        v-for="button in buttons"
        @click="ChangeColor(button)"
        :key="button.id"
        :button="button"
        :class="button.buttonColor === '+10' ? 'boquita' : ''"
      />
    </div>
  </div>
</template>

<style>
.box_buttons {
  display: flex;
  height: auto;
  width: 100%;
  padding: 15px;
  margin-bottom: 150px;
  border: none;
  /*background-color: #003391;*/
  border-radius: 12px;
  color: #fff;
}
.boquita {
  background-color: #f0b029;
  color: #02236d;
}
.button_container {
  width: 60vw;
  height: 50vh;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>
