<script>
  import { fly} from 'svelte/transition';
  import Back from './Back.svelte'

  let comprar = false
  const showComprar = () => {
    comprar = !comprar
  }

</script>

{#if comprar == false}

<div class="container" in:fly="{{x:-300, duration: 600}}">

<h1 ><span>Curriculum</span> Web</h1>
<h2>Product</h2>

<div class="card">
<div class="card-content">
<i class="fas fa-briefcase"></i>
 <p>Creación de curriculum-web y sitios personales.</p>
 <i class="fas fa-globe-americas" ></i>
 <p> Compartí toda tu info profesional con el mundo</p>
 
  <a href="https://wa.me/542392462524/?text=Hola!.%20Vi%20tu%20web%20.">
  <div class="btn">Escribime</div></a>
</div>

</div>
</div>
<Back on:click/>

{/if}



<style>

i {
  font-size: 70px;
  margin-top: 10px;
}

.container {
    text-align: center;
    margin-top: 20px;
     font-weight: normal;
     color: #333;
    margin-bottom: 90px;
}
.container h1, h2 {
       font-family: "Satisfy", cursive;

}
.container h2 {
         font-family: "Satisfy", cursive;
         color: rgba(78, 158, 250, 0.795);

}

.container span {
  color: rgba(78, 158, 250, 0.795);

}

.card {
      width: 270px;
      margin: 10px auto;
     font-family: "Comfortaa", cursive;
     background:  rgba(78, 158, 250, 0.192);


  }
  .card p {
    padding: 20px;
    margin-bottom: 20px;
    margin-top: 10px;
  }

  .btn {
    background:rgba(78, 158, 250, 0.733);
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    border: 2px solid rgb(78, 158, 250);
    border-radius: 5px;
    font-weight: bold;
  }
  .card a {
    text-decoration: none;
    color: #333;

  }

   /* ################### TABLETS ############################### */

  @media (min-width: 500px) {
    
     .container {
		  margin-top: 50px;
	  }


    .card {
      width: 450px;
    }

    .container h1 {
      font-size: 50px;
    }
    
  }
 
     
</style>