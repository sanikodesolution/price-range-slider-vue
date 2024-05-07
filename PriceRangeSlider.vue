<template>
<MultiRangeSlider :min="0" :max="100" :min-value="sBarMinValue" :max-value="sBarMaxValue" :step="1" :range-margin="0" @input="update_sBarValues" />
</template>
<script>
import { ref } from "vue";
import MultiRangeSlider from "multi-range-slider-vue";

export default {
  name: "App",
  components: {
    MultiRangeSlider
  },
  data: () => {
    return {
      videoIsOpen: false,
      sBarMinValue: 0,
      sBarMaxValue: 45,
    };
  },
  methods: {
    update_sBarValues(e) {
      this.sBarMinValue = e.minValue;
      this.sBarMaxValue = e.maxValue;
    }
  }
};
</script>