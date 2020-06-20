<script>
  //Transition from Svelte
  import { fly, fade} from 'svelte/transition';

  //Components
  import Programacion from './Programacion.svelte';
  import Back from './Back.svelte'
  import Compania from './Compania.svelte'
  import Tips from './Tips.svelte'
  import Contacto from './Contacto.svelte'
  import Info from './Info.svelte'
  import ContentManager from './ContentManager.svelte'
  import GoalsApp from './GoalsApp.svelte'

  //Variables
  let programacion = false
  let compania = false
  let tips = false
  let contacto = false
  let info = false
  let contentManager = false
  let goalsApp = false

  //Functions
  const showProgramacion = () => {
	  programacion = !programacion
  }
  const showCompania = () => {
	  compania = !compania
  }
  const showTips = () => {
	  tips = !tips
  }
  const showContacto = () => {
	  contacto = !contacto
  }
  const showInfo = () => {
	  info = !info
  }
  const showContentManager = () => {
	  contentManager = !contentManager
  }
  const showGoalsApp = () => {
	  goalsApp = !goalsApp;
  }

</script>

<!-- ##################---------HTML ----------######################>

<!-- Main Content/Conditional rendering -->
{#if programacion == false && compania == false && 
tips == false && contacto == false && info == false
&& contentManager == false && goalsApp == false}

<div class="container"  in:fade>
<div  class="containerImg"><img on:click={showGoalsApp} src="./img/en.jpg" alt="Foto de Enzo Daneri"></div>
<h1><span>Enzo</span> Daneri</h1>
<h2>Servicios Remotos</h2>

<div class="btn" on:click={showProgramacion}>Programador</div>
<div class="btn" on:click={showCompania}>Producto</div>
<div class="btn" on:click={showContentManager}>Blog</div>


  <footer>
   <div class="footerCont">
    <span on:click={showContacto}>Contacto</span>
    <span on:click={showTips} ><i class="fas fa-check"></i> Tips</span>
    <span on:click={showInfo} >Info</span>
   </div>
   </footer>

</div>
{/if}

<!-- Conditional rendering- Programming -->
{#if programacion == true}
<Programacion on:click={showProgramacion}/>
<Back on:click={showProgramacion}/>
{/if}

<!-- Conditional rendering- Product -->
{#if compania == true}
<Compania on:click={showCompania}/>
{/if}

<!-- Conditional rendering- Tips -->
{#if  tips == true}
 <Tips/>
 <Back on:click={showTips}/>
{/if}

<!-- Conditional rendering- Contact -->
{#if contacto == true}
<Contacto/>
 <Back on:click={showContacto}/>
{/if}

<!-- Conditional rendering- Info -->
{#if info == true}
<Info/>
<Back on:click={showInfo}/>
{/if}

<!-- Conditional rendering- Blog-->
{#if contentManager == true}
<ContentManager/>
<Back on:click={showContentManager}/>
{/if}

<!-- Conditional rendering- Goals(secret section) -->
{#if goalsApp == true}
<GoalsApp/>
<Back on:click={showGoalsApp}/>
{/if}


<!-- ####################---------STYLES---------######################### -->
<style>
.container {
	text-align: center;
	padding-left: 25px;
	padding-right: 25px;
	margin-top: 35px;
}

.container h1 {
	font-family: "Satisfy", cursive;
	font-weight: normal;
	font-size: 45px;
	color: #333;
	margin: 20px;
	margin-top: 8px;
}
.container span {
	color: rgba(78, 158, 250, 0.897);
}
.container h2 {
	font-family: "Satisfy", cursive;
	font-weight: normal;
	color: rgba(78, 158, 250, 0.897);
	margin-top: -10px;

}
.container img {
	border-radius: 50%;
	width: 100px;
    border: 5px solid rgba(78, 158, 250, 0.568);

}

.btn {
	width: 270px;
	height: 60px;
	background: rgba(51, 51, 51, 0.959);
	margin: 10px auto;
	border-radius: 5px;
	cursor: pointer;
	display: flex;
	align-items: center;
	justify-content: center;
	color: #fff;
	font-family: "Comfortaa", cursive;
	font-size: 20px;

}


footer {
  text-align: center;
  margin-top: 60px;
  font-family: "Comfortaa", cursive;
  margin-bottom: 30px;
  color: var(--textColor);

}
 
 .footerCont {
   text-align: center;
 }


footer span {
    cursor: pointer;
	margin: 20px;
}


   /* ################### TABLETS ############################### */

  @media (min-width: 500px) {
	  .container {
		  margin-top: 50px;
	  }

	  .container h1 {
		  font-size: 60px;
	  }
	 .btn {
		 width: 450px;
	 } 
	 .container img {
		 width: 130px;
         border: 5px solid rgba(78, 158, 250, 0.568);

	 }

footer span {
    cursor: pointer;
	margin: 50px;
	font-weight: bold;
}


  }

</style>