<script>
    import { Editor, rootCtx, defaultValueCtx } from '@milkdown/core';
    import { commonmark } from '@milkdown/preset-commonmark';
    import { nord } from '@milkdown/theme-nord';
    
    // function editor(dom) {
    //   // to obtain the editor instance we need to store a reference of the editor.
    //   const MakeEditor = Editor.make()
    //     .config((ctx) => {
    //       ctx.set(rootCtx, dom);
    //     })
    //     .config(nord)
    //     .use(commonmark)
    //     .create();
    // }
    // MakeEditor.then((editor) => {
    //   // here you have access to the editor instance.
      
    //   // const exampleContent = "# Hello World!";
    //   // editor.action(replaceAll(exampleContent));
    // })
    const markdown =
    `# Milkdown Svelte Commonmark

    > You're scared of a world where you're needed.

    This is a demo for using Milkdown with **Svelte**.`

    function editor(dom) {
        Editor.make()
            .config((ctx) => {
            ctx.set(rootCtx, dom)
            ctx.set(defaultValueCtx, markdown)
            })
            .config(nord)
            .use(commonmark)
            .create();
    }
</script>
    
<div use:editor />