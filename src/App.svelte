<script>
  import { marked } from "marked";
  let source = `# New Document`;
  // let markdown = marked(source) 
// reactive element
  $: markdown = marked(source)

</script>
<header class="header">
  <h1 class="header-title">Markdown editor</h1>
</header>
<div class="markdown-editor">
  <div class="markdown-editor_leftpanel">
    <textarea bind:value={source} class="markdown-editor_source"></textarea>
  </div>
  <div class="markdown-editor_rightpanel">
    <div class="markdown-editor_output">{@html markdown}</div>
  </div>
</div>

<style>
  .header {
        height: 10vh;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .header-title {
        margin: 0;
    }

    .markdown-editor {
        width: 100%;
        display: flex;
        align-items:flex-start;
        justify-content: space-evenly;
    }

    .markdown-editor_leftpanel, .markdown-editor_rightpanel{
        width: 50%;
        border: solid 1px black;
        height: 90vh;
    }

    .markdown-editor_rightpanel {
        overflow: auto;
    }

    .markdown-editor_source {
        border: none;
        width: 100%;
        height: 100%;
    }

    .markdown-editor_source:focus {
        outline: none;
    }

    .markdown-editor_output {
        width: 100%;
    }

  
</style>
