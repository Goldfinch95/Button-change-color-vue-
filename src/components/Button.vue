<script>
export default {
  props: {
    button: {
      name: {
        type: String,
        required: true,
      },
    },
  },
};
</script>
<template>
  <button>Clickeaste {{ button.count }} veces</button>
</template>
<style>
button {
  height: 10%;
  width: 40vw;
  margin: 15px;
  margin-top: 30px;
  background-color: #02236d;
  border-radius: 7px;
  font-size: 15px;
  border: none;
  color: #f0b029;
}
button:focus {
  border: 1px solid #f0b029;
}
</style>
