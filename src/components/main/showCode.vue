<template>
  <prism-editor
    class="my-editor height-300"
    v-model="code"
    :highlight="highlighter"
    :line-numbers="lineNumbers"
  ></prism-editor>
</template>
<script>
import { PrismEditor } from "vue-prism-editor";
import "vue-prism-editor/dist/prismeditor.min.css"; // import the styles somewhere

// import highlighting library (you can use any library you want just return html string)
import { highlight, languages } from "prismjs/components/prism-core";
import "prismjs/components/prism-clike";
import "prismjs/components/prism-javascript";
import "prismjs/themes/prism-tomorrow.css"; // import syntax highlighting styles
export default {
  components: {
    PrismEditor,
  },
  data() {
    return {
      code: `let sum = 0, 
    table = [
      [1, 2, 3],
      [4, 5, 6],
      [7, 8, 9],
    ];
for (let i = 0; i <= table.length; i++) {
  for (let j = 0; j <= table[i].length; j++) {
    sum += table[i][j];      // 执行 n^2 次
  }
}`,
      lineNumbers: true, // true为编辑模式， false只展示不可编辑
    };
  },
  methods: {
    highlighter(code) {
      return highlight(code, languages.js); //returns html
    },
  },
};
</script>
<style lang="scss" scoped>
/* required class */
.my-editor {
  background: #2d2d2d;
  color: #ccc;

  font-family: Fira code, Fira Mono, Consolas, Menlo, Courier, monospace;
  font-size: 14px;
  line-height: 1.5;
  padding: 5px;
}

/* optional */
.prism-editor__textarea:focus {
  outline: none;
}

/* not required: */
.height-300 {
  height: 300px;
}
</style>
