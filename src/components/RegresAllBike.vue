<template>
  <div v-if="XMLHttpError" class="verticalMiddle">Error</div>
  <div v-else-if="allData.length === 0" class="verticalMiddle">No Data</div>
  <div v-else class="dataBox">
    <div
      v-for="item in allData"
      :key="item.StationID"
      @click="triggerMap(item)"
    >
      {{ item.StationName.Zh_tw }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    error: Boolean,
    allData: Array,
  },
  methods: {
    triggerMap(item) {
      const { PositionLat, PositionLon } = item.StationPosition;
      this.$emit('trigger', [PositionLat, PositionLon]);
    },
  },
};
</script>
