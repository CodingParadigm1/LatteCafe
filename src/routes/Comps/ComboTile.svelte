<script>
    export let title = "", 
                pic = "", 
                price=0.0; 
</script>

<main>
    <span id="title">
        {title}
    </span>
    <article>
        <section>
            <img src={pic} alt="#">
        </section>
        <span id="price">
            {price}
        </span>
    </article>
</main>


<style>
    main{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap:5px;
        max-height:125px;
        width:85px;
        padding:2px 5px;
        border-radius: 7px;
        border:none;
        background-color: white;
        box-shadow: 0 0 12px black;
        transition-duration: .75s;
    }

    main:hover{
        margin-left:-30px;
        margin-right:15px;
    }

    main:nth-child(1){
        margin-right:-15px;
    }
    main:nth-child(1):hover{
        margin-right:10px;
    }

    img{
        background-size:cover;
        width:80px;
        height:80px;
        border-radius: 50%;
    }

    article{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap:5px;
    }

    section{
        display: flex;
        align-items: center;
        justify-content: center;
        height:100%;
        width:100%;
    }
</style>