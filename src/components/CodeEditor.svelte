<link rel="stylesheet" href="../node_modules/codemirror/lib/codemirror.css">

<script>
    import CodeMirror from 'codemirror'
    import javascript from 'codemirror/mode/javascript/javascript'
    import colorize from 'codemirror/addon/runmode/colorize'
    import "codemirror/lib/codemirror.css";
    import { onMount } from "svelte";
    let editor

    onMount(()=>{

        console.log(editor);
        CodeMirror(editor, {
            value: "// void function",
            mode:  "javascript",
            lineNumbers: true
        }) 

        
    })

</script>

<style>

</style>

<div id="editor" bind:this={editor}></div>