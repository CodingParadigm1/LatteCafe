<script>
  import './style.css'; 
  import KnownCombos from './Comps/KnownCombos.svelte';
  import Button from "./Comps/Button.svelte";
    import Input from './Comps/Input.svelte';
    import ComboTile from './Comps/ComboTile.svelte';
    import Combos from './Comps/Combos.svelte';
    import SelectTile from './Comps/SelectTile.svelte';

    let coffee_choices = [{
      "title": "Caramel", 
      "pic": "cafe.jpg", 
      "price": 10
    }];

    let chosen_coffee = coffee_choices[0];
      
</script>

<main>
  <SelectTile/>
  <Combos>
    <ul>
      {#each coffee_choices as choice}
         <ComboTile title = {choice.title} pic = {choice.pic} price = {choice.price}/>
      {/each}
    </ul>
  </Combos>
  <KnownCombos/>
</main>


<style>
  main{
    display: grid;
    grid-template-rows: 4fr 3fr 4fr;
    height:100vh;
    width:100vw;
  }
</style>