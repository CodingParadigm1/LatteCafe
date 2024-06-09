<script>

    export let title = "default", img="#",add_ons = [{item_name: "cinnamon", price: 10.0}, {item_name: "sugar", price: 10.0}, {item_name: "cool-whip", price: 10.0}], price="5" 

</script>

<main>
    
    <img src={img} alt="#">
    
    <article>
        <span>
            {title}
        </span>
        <section>
            <ul>
                {#each add_ons as item}
                    <li>
                        <span style="margin-left:5px;">
                            {item.item_name}
                        </span>
                        <span style="margin-right:5px;">
                            {item.price}
                        </span>
                    </li>
                {/each}
            </ul>
        </section>
    </article>

</main>

<style>

    article{
        display: flex;
        flex-direction: column;
        align-items: center;
        height:75%;
        width:35%;
        min-width: 100px;
        max-width:125px;
        border-radius:7px;
        padding:5px;
        gap:20px;
        background-color: white;
        color:black;
    }

    main{
        color:white;
        background-color: black;
        border-bottom-left-radius: 12%;
        border-bottom-right-radius: 12%;
        box-shadow:0 0 12px turquoise;
        z-index:0;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-around;
    }

    img{
        background-size: cover;
        width: 100px;
        height: 100px;
        border-radius: 50%;
    }

    ul{
        display: flex;
        flex-direction: column;
        align-items: center;
        width:100%;
        padding:5px 2px;
    }

    li{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        margin:5px 0;
        padding:5px 3px;
        width:85%;
        border-radius: 7px;
        box-shadow:0 0 2px brown;
    }

    li:nth-child(1){
        margin-top:0;
    }

    li:nth-child(-1){
        margin-bottom:0;
    }

    section{
        width:100%;
    }

    span{
        font-size: 12px;
    }

</style>