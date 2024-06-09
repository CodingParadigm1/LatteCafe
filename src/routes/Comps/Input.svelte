<script>
    export let inner_text = ""; 
</script>

<input type="text" bind:value={inner_text}/>

<style>
    input{
        width:175px;
        height:24px;
        padding:3px 5px;
        border-radius: 7px;
        background-color: rgb(42, 41, 41);
        color:green;
        box-shadow: 0 4px 12px brown;
        font-size:22px;
        transition-duration: .75s;
    }
    input:hover{
        color:rgb(42, 195, 42);
        box-shadow: 0 0 16px brown;
    }
    input:focus{
        color:rgb(42, 195, 42);
        box-shadow: 0 0 16px brown;
    }
</style>
