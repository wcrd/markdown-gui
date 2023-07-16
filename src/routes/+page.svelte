<script>
    import Editor from "$lib/components/editor.svelte";
</script>

<div class="flex flex-col h-screen">
    <div id="header" class="flex flex-row h-8 bg-green-200">
        <p>Header controls</p>
    </div>
    <div id="editor-container" class="flex flex-row h-100 flex-grow">
        <div class="w-1/6 flex border border-black">
            <p>Menu</p>
        </div>
    
        <div class="w-5/6 flex flex-row ">
            <div class="w-3/6">
                <Editor></Editor>
            </div>
        
            <div class="w-3/6 border">
                Toggle Area (to be moved into Editor / super component and have shared state)
            </div>
        </div>
    </div>
    <div id="footer" class="flex flex-row h-6 bg-blue-600 text-white">
        <p>Footer</p>
    </div>
</div>
