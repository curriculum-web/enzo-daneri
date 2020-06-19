<script>
  import { fly, fade} from 'svelte/transition';


</script>


<div class="container"  in:fly="{{x:-300, duration: 600}}">
 <h1>Info</h1>
<h2 ><span>Enzo</span> Daneri</h2>


<div class="card">
<div class="card-content">
<p>Gracias por visitar mi Sitio Web Personal </p>
</div>
</div>

<div class="cardDos">
<div class="card-content">
<p>Aquí muestro mis servicios, tanto para empresas, como para particulares.</p>
</div>
</div>


<div class="card">
<div class="card-content">
<p>Es mi objetivo lograr interfaces de usuario limpias e intuitivas</p>
</div>
</div>


<div class="cardDos">
<div class="card-content">
<p>Siempre con pasión por la programación! </p>
</div>
</div>

</div>

<style>
.container {
    text-align: center;
    margin-top: 20px;
    margin-bottom: 90px;

}
.container h1 {
font-family: "Comfortaa", cursive;
font-weight: normal;
color: rgba(78, 158, 250, 0.795);
font-size: 40px;

}
.container h2 {
    color: #333;
   font-family: "Satisfy", cursive;
   margin-top: 10px;

}
.container span {
        font-family: "Satisfy", cursive;
         color: rgba(78, 158, 250, 0.795);

}
.card { 
      width: 270px;
      background:  rgba(78, 158, 250, 0.548);
      margin: 10px auto;
      border-radius: 5px;
      font-family: "Comfortaa", cursive;
      color:#333;
      margin-top: 20px;
      padding: 20px;
}
 
.cardDos {
    background:  rgba(78, 158, 250, 0.192);
    color:#333;
    margin-top: 20px;
    padding: 20px;
    border-radius: 5px;
    font-family: "Comfortaa", cursive;
     width: 270px;
     margin: auto;


}


  /* ################### TABLETS ############################### */

  @media (min-width: 500px){

       .container {
		  margin-top: 50px;
	  }

       .container h1 {
      font-size: 50px;
    }

    .card, .cardDos {
       width: 450px;

    }
  }


</style>