<template>
    <survey :survey="survey" />
</template>
<script>
import Vue from "vue";
import { Model, StylesManager } from "survey-vue";
import "survey-vue/defaultV2.min.css";
import "./index.css";
import { json } from "./json";

StylesManager.applyTheme("defaultV2");

export default Vue.component("survey-component", {
  name: "survey-component",
  data() {
    const survey = new Model(json);
    return {
      survey: survey,
    };
  },
});
</script>