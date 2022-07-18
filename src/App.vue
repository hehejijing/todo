<template>
  <section class="todoapp">
    <!-- 除了驼峰, 还可以使用-转换链接 -->
    <TodoHeader @add="addFn"></TodoHeader>
    <TodoMain :list="list"></TodoMain>
    <TodoFooter></TodoFooter>
  </section>
</template>

<script>
import "./assets/styles/base.css";
import "./assets/styles/index.css";

import TodoHeader from "./components/TodoHeader";
import TodoMain from "./components/TodoMain";
import TodoFooter from "./components/TodoFooter";

export default {
  components: {
    TodoHeader,
    TodoMain,
    TodoFooter,
  },
  data() {
    return {
      list: [
        { id: 100, name: "吃饭", isDone: true },
        { id: 201, name: "睡觉", isDone: false },
        { id: 103, name: "打豆豆", isDone: true },
      ],
    };
  },
  methods: {
    addFn(task) {
      this.list.push({
        name:task,
        isDone:false,
        id: 999
      })
    }
  }
};
</script>

<style></style>
