<template>
  <div class="tracking-bar">
    <input
      type="text"
      class="tracking-bar__input"
      placeholder="取貨點，地址或地區"
      v-model="query"
    />
    <button type="button" class="tracking-bar__search-btn" @click="clicked">
      <p class="searchBarText">搜索</p>
      <svg
        width="20"
        height="19"
        viewBox="0 0 20 19"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M2.28204 7.5C2.28204 11.0661 5.25427 14 8.97435 14C12.6944 14 15.6667 11.0661 15.6667 7.5C15.6667 3.93386 12.6944 1 8.97435 1C5.25427 1 2.28204 3.93386 2.28204 7.5Z"
          stroke="white"
          stroke-width="2"
        />
        <path
          d="M14.1026 13L18.718 17.5"
          stroke="white"
          stroke-width="2"
          stroke-linecap="round"
        />
      </svg>
    </button>
  </div>
</template>
<script>
export default {
  name: "TrackingBar",
  props: {
    query: {
      type: String,
      required: false,
    },
  },
  methods: {
    clicked() {
      this.$emit("clicked", this.query);
    },
  },
};
</script>