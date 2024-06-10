
<script>
    export let vendors = [
        {
            title: "StarBucks", 
            cost: 5, 
            address: "10 Windley Ave",
            in_stock: true,
            item_reference: "3472IA" 
        },
        {
            title: "Bee's Coffee", 
            cost: 8, 
            address: "10 Windley Ave",
            in_stock: true,
            item_reference: "3472IA" 
        },
        {
            title: "Truck Stop", 
            cost: 2, 
            address: "10 Windley Ave",
            in_stock: true,
            item_reference: "3472IA" 
        },
        {
            title: "StarBucks", 
            cost: 10, 
            address: "10 Windley Ave",
            in_stock: true,
            item_reference: "3472IA" 
        },
        {
            title: "StarBucks", 
            cost: 10, 
            address: "10 Windley Ave",
            in_stock: true,
            item_reference: "3472IA" 
        },
        {
            title: "DutchBros", 
            cost: 8, 
            address: "24 Ramsley Trl", 
            in_stock: true,
            item_reference: "3472BA" 
        },
        {
            title: "DutchBros", 
            cost: 4, 
            address: "24 Ramsley Trl", 
            in_stock: true,
            item_reference: "3472IA" 
        }
    ],
    item_ref="3472IA";
</script>

<main>
    <article>
        <ul>
            {#each vendors as vendor}
                {#if item_ref==vendor.item_reference}
                    <li>
                        <span>
                            {vendor.title}
                        </span>
                        <span>
                            {vendor.cost}
                        </span>
                    </li>
                {/if}
            {/each}
        </ul>
    </article>
</main>

<style>
    article{
        border:none;
        border-radius:7px;
        margin-top:15px;
        height:85%;
        width:95%;
        overflow-y: auto;
        padding-bottom:5px;
    }
    main{
        color:white;
        background-color: rgb(12, 12, 12);
        border-top-left-radius: 12%;
        border-top-right-radius: 12%;
        box-shadow:0 0 12px turquoise;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    ul{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap:15px;
        margin-top:15px;
        overflow: visible;
    }

    li{
        border:none;
        border-radius:7px;
        width:80%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        background-color: white;
        color:black;
        padding:3px 5px;
        box-shadow:0 0 12px turquoise;
    }
</style>