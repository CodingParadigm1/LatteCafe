<script>
  import './style.css'; 
  import KnownCombos from './Comps/KnownCombos.svelte';
  import ComboTile from './Comps/ComboTile.svelte';
  import Combos from './Comps/Combos.svelte';
  import SelectTile from './Comps/SelectTile.svelte';

    let coffee_choices = [
        {
          "title": "Caramel", 
          "pic": "cafe.jpg", 
          add_ons:[
              {
                  "name":"Caramel",
                  "price": 10.0
              }, 
              {
                  "name":"Choc Syrup",
                  "price": 10.0
              }, 
              {
                  "name":"Cool Whip",
                  "price": 10.0

              },  
          ],
          "item_reference": "3472IA", 
          "price": 10, 
          "index": 0
        },{
          "title": "Pmpkn Spice", 
          "pic": "pumpkin.jpg", 
          add_ons:[
              {
                  "name":"Pmkn Spice",
                  "price": 10.0

              }, 
              {
                  "name":"Cinnamon",
                  "price": 10.0

              }, 
              {
                  "name":"Cool Whip",
                  "price": 10.0

              },  
          ],
          item_reference: "3472BA",
          "price": 5,
          "index": 1
        }
    ];

    let selected_coffee = 0; 
    $: chosen_coffee = coffee_choices[selected_coffee];
    $: console.log(chosen_coffee.item_reference); 
</script>

<main>
  <SelectTile title={chosen_coffee.title} add_ons={chosen_coffee.add_ons} img={chosen_coffee.pic}/>
  <Combos>
    <ul>
      {#each coffee_choices as choice}
        <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <li on:click = {()=>{
          selected_coffee = choice.index; 
        }}>
          <ComboTile 
            title = {choice.title} 
            pic = {choice.pic} 
            price = {choice.price}/>
        </li>
      {/each}
    </ul>
  </Combos>
  <KnownCombos item_ref={chosen_coffee.item_reference}/>
</main>


<style>
  main{
    display: grid;
    grid-template-rows: 4fr 3fr 4fr;
    height:100vh;
    width:100vw;
  }
  ul{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    background-color: rgb(40, 38, 38);
    list-style: none;
    width:100%;
    min-width:200px;
  }
  li{
    height:90%;
    overflow: visible;
  }
</style>