<template>
   <div class="tab_title">
        <ul>
          <li @click="tab = 0" :class="{ tab_active: tab == 0 }">主页</li>
          <li @click="tab = 1" :class="{ tab_active: tab == 1 }">智能问答</li>
          <li @click="tab = 2" :class="{ tab_active: tab == 2 }">知识图谱</li>
          <li @click="tab = 3" :class="{ tab_active: tab == 3 }">反馈</li>
        </ul>
   </div>
    <div class="content">
    
        <div class="tab_content" v-if="tab == 0">
          <mainpage></mainpage>
        </div>

        <div class="tab_content" v-else-if="tab == 1">
          <chatbot></chatbot>
        </div>

        <div class="tab_content" v-else-if="tab == 2">
          <neo4j></neo4j>
        </div>

        <div class="tab_content" v-else-if="tab == 3">
          <feedback></feedback>
        </div>

        </div>
    </div>
</template>

<script>
import mainpage from './components/mainpage.vue';
import chatbot from './components/chatbot.vue';
import neo4j from './components/neo4j.vue';
import feedback from './components/feedback.vue';

export default {
  name: 'App',
  components: {
    mainpage,
    chatbot,
    neo4j,
    feedback,
  },
  data() {
    return {
      tab: 0,
    };
  },
}
</script>

<style>

</style>
