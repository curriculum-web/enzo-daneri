<script>
  import { fly, fade} from 'svelte/transition';


</script>


<div class="container"  in:fly="{{x:-300, duration: 600}}">
<h1>Blog</h1>


<div class="card">
<div class="card-content">
<i class="fas fa-feather-alt"></i>
<p> Creación de Contenidos para Empresas</p>
    <div class="icons"><a href="https://github.com/EnzoDaneri" target="blank"><i class="fab fa-github"></i></a>
     <a href="https://www.linkedin.com/in/enzo-adri%C3%A1n-daneri-desarrollo-web/"target="blank"><i class="fab fa-linkedin-in"></i></a>
     <a href="https://www.facebook.com/enzodaneri"target="blank"><i class="fab fa-facebook-f"></i></a>
     <a href="https://www.instagram.com/danerienzo/" target="blank"><i class="fab fa-instagram"></i></a>


</div>
</div>
</div>

    <a href="https://wa.me/542392462524/?text=Hola!.%20Vi%20tu%20web.%20">
    <div class="btn">Contactar</div></a>
<br>
<hr>
    <div class="card-blog"> <h2>Minimalismo</h2><br>
  <p> Desde sus inicios la web ha crecido de manera exponencial y se ha vuelto cada vez más compleja. En ese proceso los desarrolladores y las modas han ido variando los estilos y las maneras de presentar la información a los usuarios. Pero no siempre estos cambios han sido en beneficio de una buena experiencia de navegación.
</p><br>
<p>
  Existe una tendencia mayoritaria que busca presentar la mayor cantidad de contenido posible en la pantalla. Pero la verdad es que muy pocas veces alguien lee todo lo que aparece allí. En lo personal me gustan las interfaces limpias, claras, e intuitivas. Por supuesto que pueden existir casos en los cuales sea necesario informar muchas cosas, con grandes cantidades de palabras, imágenes y cosas que ofrecer. No obstante, todo ello se podría presentar cuidando siempre el principio de minimalismo.</p><br>

<p> Es mi intención que esta web personal sea un ejemplo de cómo me gusta presentar la información, incluyendo sus botones, textos e imágenes. Espero que sea de tu agrado al usarla y que me tengas en cuenta para desarrollar tu propio proyecto siguiendo estos lineamientos.</p>
</div>
</div>
 
<style>

 .container {
      text-align: center;
      margin-top: 30px;
      margin-bottom: 90px;
  }
  .card i {
      font-size: 90px;
      color: #333;
      margin-bottom: 20px;
  }

.container h1 {
 font-family: "Satisfy", cursive;
 font-weight: normal;

}


.card {
   width: 270px;
   text-align: center;
   margin: 20px auto;
   padding: 20px;
   border-radius: 5px;
   background:  rgba(78, 158, 250, 0.192);

}
.card-blog {
   width: 270px;
   text-align: start;
   margin: 20px auto;
   padding: 20px;
   border-radius: 5px;
   background:  rgba(78, 158, 250, 0.192);

}
.card-blog h2 {
  text-align: center;
  font-family: "Comfortaa", cursive;

}
.card p, .card-blog p {
    color: #333;
    font-family: "Comfortaa", cursive;
    font-size: 18px;
    margin-bottom: 15px;
}
 .icons i{
    font-size: 30px;
    color: rgb(78, 158, 250);
    margin: 7px;
    margin-bottom: 20px;
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
    font-family: "Comfortaa", cursive;
    width: 270px;
    margin: auto;
    margin-top: -20px;
  }
   a {
    text-decoration: none;
    color: #333;
    display: inline;

  }

  /* ################### TABLETS ############################### */

  @media (min-width: 500px){

    .container {
		  margin-top: 50px;
	  }

    .container h1 {
      font-size: 50px;
    }
    .card {
        width: 450px;

    }
    .btn {
        width: 450px;
    }

  }
</style>
