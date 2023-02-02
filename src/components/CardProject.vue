<template>
  <div>
    <h3>{{ info.title }}</h3>
    <p>{{ info.content }}</p>
    <div>
      <img v-if="info.image_url" :src="info.image_url" :alt="info.title" />
    </div>
    <p>Tipologia:{{ info.type_id }}</p>
  </div>
</template>

<script>
export default {
  props: {
    info: Object,
  },
};
</script>

<style lang="scss" scoped>
p {
  font-size: 10px;
}
</style>
