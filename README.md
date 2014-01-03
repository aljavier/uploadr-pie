Uploader de archivos a uploadpie.com desde la linea de comandos
---------------------------------------------------------------

Tan simple como eso, este es un sencillo script para subir archivos
(gif, png, jpg, pdf y txt) al gran sitio [Upload Pie](http://uploadpie.com/),
el cual suele ser usado un buen poco por algunas caracteristicas del
mismo, como son:
+ Los archivos subidos se almacenan de forma temporal.
+ No existe una forma de que alguien vea tus archivos si no le das la url.
+ Por tanto, eso indica que no existe una galeria de imagenes ni nada de eso en el portal.
+ Puedes elegir el tiempo de duracion del archivo, que puede ser: 30 minutos, 1 hora, 6 horas,
1 dia o 1 semana.

Por tanto, me gusta el sitio por su estilo de privacidad y demas. El caso es que
prefiero usar la terminal para la mayoria de cosas que puedo hacer porque es mas
rapido (y porque me gusta!), asi que por eso hize este sencillo script, que posiblemente
pueda servirle a alguien mas ahi afuera, es la razon por la cual lo comparto aqui.

En lo personal uso un directorio **bin/** en mi **$HOME**, donde puedo agregar este tipo de script
y demas programas creados por mi mayormente y asi poder usarlos como si estan localizados
en **/usr/local/bin** o similiar directorio. Algunas distros pueda ser que venga con ese directorio
en el $HOME del usuario, en ese caso ellos mismos agregan ese directorio al **$PATH**, para que 
sea posible hacer lo que dije antes, otras distros como Ubuntu segun lei y quizas Linux Mint
una vez creas un directorio bin/ en tu $HOME e inicias sesion de nuevo en alguna terminal
o tty agregan el bin/ al $PATH automaticamente.

En mi caso uso Arch Linux, asi que haria lo siguiente:

	[yo@linux-box ~]$ mkdir bin/
	
Entonces lo siguiente es agregar ese directorio al $PATH, para eso abre tu archivo **.bashrc**
con tu editor de texto favorito (vim en mi caso) y agregas esta linea:

	export PATH=~/bin:"$PATH"

Guardas el archivo y luego ejecutas:

	source ~/.bashrc

Entonces copias el script a ese directorio bin/ en tu $HOME y ya podras ejecutarlo como
 cualquier otro binario en tu /usr/local/bin, simplemente poniendo el nombre, si ejecutas
sin argumento:

	[yo@linux-box ]$ uploadr-pie

Obtendras una ayuda del script(muy mal elaborada quizas x) como la siguiente:

	Uso: uploadr-pie mi_archivo.ext [DURACION]

	Donde DURACION es un numero del 1 al 5 (1 por defecto):
	1 = 30 minutos	2 = 1 Hora	3 = 6 Horas	4 = 1 Día	5 = 1 Semana

El segundo parametro([DURACION]) es opcional indica el tiempo que el servidor hosteara el archivo,
puede verse claramente en la ayuda, si no se indica nada, por defecto seran 30 minutos.


