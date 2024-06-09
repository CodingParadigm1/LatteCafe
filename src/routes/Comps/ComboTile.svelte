<script>
    export let title = "", pic = "", price=0.0; 
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
        height:90%;
        width:85px;
        padding:2px 5px;
        border-radius: 7px;
        border:none;
        background-color: white;
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