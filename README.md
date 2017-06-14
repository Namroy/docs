
<li>configuraremos nuestros datos:</li>
<p><code>git config --global user.name "Yorman"<br>
git config --global user.email "Your@MYEmail.com"
</code></p><br>

<li>Obtencion de la clave ssh mediante el comando:</li>

comando:ssh-keygen
La consola responde de esta manera:
nter file in which to save the key ($/home/Namroy/.ssh/id_rsa):

nos pedirá una contraseña <b>-passphrase-</b> la contraseña es opcional,
para saltarla le damos doble enter, pero no es recomendable en entornos de produccion reales.
<br>
codigo de respuesta automatico de shell (ejemplo):
Enter passphrase (empty for no passphrase):
Enter same passphrase again: 

Para leer la clave ssh:

codigo$: cat ~/.ssh/id_rsa.pub

Y la consola nos responderá algo como esto:

Código : ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDMpPqnv9XBAnNAU60o+zxoXxrl79LBaqpEgUdBk9zjSslkVqWJpu3VKWU/JC3nToPP7zRv0wDWWFaWdNaeJAT9AWsExrhbLZumKQJE1IONhqO1FBvEOrhT5HLAfN7FII89OM+rAP8ojQonbZqddKZaZ5ik5U7kIz/Z4oG8bKosSw6fqtf5I0Ya7G+egAW9QxjLdFyC6Y2MyftjKZsaugnpr7EHtsM2RoGdZAmUWND3ofE/DltrNh2KF4e3OhuPQUPXtP7uKtRW1orC0QxHfd7jMPOujtE1+dT5mb3itlLD7tnddoyNgzgjN/vKyl7O4igB4hdgD/MUOYqdmjbI73iv namroy@namroy-PC

--Copiamos el contenido y lo pegaremos en SSH Keys en GitHub:
  para esto vamos a settings->SSH Keys y pegamos la llave ssh y le damos un titulo  y guardamos listo por aqui.
  

--validamos nuestra keys-ssh con este comando:

codigo: ssh -T git@github.com 

y listo ya hay conexion entre github y tu pc

5) subir archivos a tu githob:

*entramos al direcctorio del proyecto y aplicamos el comando<b>init</b> para activar git en ese directorio.

comando: git add -A OR <name.file> 

comando:git commit -m "siempre comentar el commit"

comando:git push -u origin master


