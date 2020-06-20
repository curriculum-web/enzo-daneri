<script>
// Transition from Svelte
import {fly} from 'svelte/transition';

//Imports
import Goal from './Goal.svelte';

// Variables
let goals= [ {
    name: '',
    description: '',
    id: null
}];

let name = '';
let description = '';
let id = null;

//Functions
const addGoal = ({name, description}) => {
     let goal = {id: Math.random() * Date.now(),
     name, description};
     goals = [goal, ...goals];
      name = '';
     description = '';
     id = null;
     }

</script>


<!-- #########--------------STYLES--------------################## -->
<style>
.container {
    text-align: center;
    margin-top: 20px;
}


.input {
    color: #333;
    outline-color:  rgba(78, 158, 250, 0.568);
    background-color:  rgba(78, 158, 250, 0.075);
    border: none;

}

</style>

<!-- ############--------HTML---------############################# -->

<div class="container"  in:fly="{{x:-300, duration: 600}}">

<h1>Success!</h1>
<div class="form-fields">
<div class="for-control"><input class="input" type="text" bind:value={name} placeholder="Me propongo..."> 
</div><br>
<div class="form-control"><input class="input" type="text" bind:value={description} placeholder="de la siguiente manera...">
</div> <br>
<button class="btn" type="submit" on:click={addGoal}>Guardar</button>
</div>

<Goal {goals}/>
</div>

