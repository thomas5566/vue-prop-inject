<template>
  <ul>
    <knowledge-element
      v-for="topic in topics"
      :key="topic.id"
      :id="topic.id"
      :topic-name="topic.title"
      :description="topic.description"
    ></knowledge-element>
  </ul>
</template>

<script>
export default {
  // props: ['topics'],
  // provide from App.vue and inject to KnowledgeGrid.vue
  // only inject what has been provided on a higher-up level
  // which means in a parent component of KnowledgeGrid.vue
  // provide and inject needs parent-child relation
  inject: ['topics'],
  // emits: ['select-topic']
};
</script>