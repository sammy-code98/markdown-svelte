<script>
  import { marked } from "marked";
  let source = `# New Document`;
  let markdown = marked(source) 

  // let source = `
	// # H1 heading

	// ## H2 heading

	// ### H3 heading

	// ---------

	// **bold text**

	// *Italiced text*

	// ---------

	// 1. first item
	// 2. second item

	// - first item
	// - second item
	// - third item

	// [Svelte](https://svelte.dev/)


	// `;

  // let markdown = marked(source);
</script>

 <!-- <main class="container">
  <header class="header">
    <h1 class="header-title">Svelte markdown editor</h1>
  </header>

  <div class="markdown-editor">
    <div class="left-panel">
      <textarea bind:value={source} class="source" />
    </div>

    <div class="right-panel">
      <div class="output">{@html markdown}</div>
    </div>
  </div> 
</main>  -->
<header class="header">
  <h1 class="header-title">Markdown editor</h1>
</header>
<div class="markdown-editor">
  <div class="markdown-editor_leftpanel">
    <textarea  class="markdown-editor_source"></textarea>
  </div>
  <div class="markdown-editor_rightpanel">
    <div class="markdown-editor_output">{@html markdown}</div>
  </div>
</div>

<style>
  /* .container {
    background: #ff3e00d6;
    padding: 10px 30px;
  }
  .header {
    height: 10vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .header-title {
    margin: 0;
    color: #fff;
  }
  .markdown-editor {
    width: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: space-evenly;
  }
  .left-panel,
  .right-panel {
    width: 50%;
    border: solid 1px black;
    height: 85vh;
    background: #ffffff;
  }
  .right-panel {
    overflow: auto;
  }
  .source {
    border: none;
    width: 100%;
    height: 100%;
    background: #001628;
    color: #83ba52;
  }
  .source:focus {
    outline: none;
  }
  .output {
    width: 100%;
    padding: 0 2em;
  } */

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
       

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
