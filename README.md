# boubekri
<!-- Gestion d'un stagaire en php  -->
<?php
// session_start();
$filename = "doc.txt";
if (file_exists($filename)) {
$f=fopen($filename,"r");
$visites=fgets($f);
fclose($f);

}
else {
  $visites = 0;
}
$visites++;
$f=fopen($filename,"w");
fwrite($f,$visites);
fclose($f);


?>

<html>
  <head>
    <style>
      h1{
         font-size: 90px;
         color: blue;
      }
      h1:hover{
        background-color: yellow;
      }
      .btn{
        width: 100 px;
        height: 100 px;
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        border-radius: 40px ;
        padding: 10px;
      }
      .btn:hover{
                background-color: black;
                color: wheat;
            }
    </style>
    <title>Mon site web</title>
  </head>
  <body>
    <fieldset><center>

    <h1>Nombre de visites : <?php echo $visites; ?></h1>
    <form action="utilisateur.php" method="post">
      <input class="btn" type="submit" value="valider">
      </center>
      </fieldset>
    </form>
  </body>
</html>


