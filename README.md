# YouTelly

## Definiciones:  
  
  **Páginas**:  
    Login        
    Index  
    Details    
  
  **Paleta de colores**:  
    --gunmetal: rgba(52, 58, 64, 1);  
    --slate-gray: rgba(108, 117, 125, 1);  
    --light-gray: rgb(241, 240, 240);  
    --apple-green: rgba(134, 188, 37, 1);  
    --azure: rgba(0, 123, 255, 1);      
    --heat-wave: rgba(253, 126, 20, 1);      
  
  **Fuente por defecto**:  
    font-family: Signika;  
    src: url('../fonts/Signika-Regular.ttf');  
  
  **Logos**:  
    logo-square-text-large.png  
    logo-square-text-medium.png  
    logo-square-text-small.png  
    logo-square-large.png  
    logo-square-small.png  
    logo-small.png  
    logo-large.png  
   
  **Barras de scroll**:  
    Rediseñadas  
  
  **Titulos y subtitulos**:  
    Los títulos de las secciones son grandes con una linea verde debajo.  
    Los subtítulos son más pequeños con una linea gris debajo. (Usados en la página de Details)  
    
  **Schema.org Movies**
    Utilizado los schemas Person y Movie para marcar la información de las películas y actores así como el video del Trailer.  

## Página de login:  
  - Login con video BG responsive (**media query**)  
  - Inputs estilo material. La linea del input se pone roja si el dato no es valido. (**transition, :invalid**)  
  - Enlaces <a> en display flex. Si la pantalla es estrecha, se ponen en columna con la correspondiente separación entre ellos. (**Flex-box**)  
  
## Navbar: 
 - Dos logos. Uno ancho para cuando hay espacio suficiente y otro cuadrado para cuando el ancho de la pantalla es pequeño. (**picture source**)  
 - La caja de búsqueda siempre está visible y se ajusta en base al ancho de la pantalla. Dejando sitio al menú en pantallas más anchas y ocupando casi toda la barra en pantallas estrechas donde el logo y el menú se han adaptado para ocupar poco (Burger y logo cuadrado).  
 - Cuando el menú se muestra en pantallas pequeñas (pulsando **Burger-checkbox**) éste aparece deslizandose desde arriba. (**animation**)  

## Footer:  
  - Secciones de enlaces orgnaizadas con **Flex-box** con un ancho mínimo para que en se agrupen de 2 en 2 secciones. Si la pantalla es menor que ese ancho mínimo, entonces sí se agrupan una encima de otra.  
    
## Página de Inicio:    
  Sección de "Trending now" (Carrusel)  
  - Maqueta de un carrusel.  
  - Corto video de la película en autoplay. (**&lt;video&gt; tag con atributos adaptados**)  
  - En pantallas grandes, la info de la película se muestra solo al hacer Hover sobre el video.  (**Hover / Selectores avanzados**)  
  - En pantallas pequeñas la info de la pelicula se muestra debajo del video de forma permanente. Esto evita que el texto de la info ocupe todo el vide al ser la pantalla demasiado pequeña. (**media query**)  
  - Efecto de televisión en el video de la sección Trending (box-shadow + animation). Leves destellos alrededor del video. (**keyframes + animation**)  
  
  Parrillas de películas (New Releases, Series, Movies).  
  - Contenido reajustado con **Flex-box**. El tamaño de las caratulas varía (escogiendo una imagen más grande o más pequeña) según el ancho de la pantalla. (**&lt;source&gt; tag con varias alternativas**)  
  - En móviles, las secciónes muestran las carátulas en una sola linea con scroll horizontal. (**Flex-box nowrap + overflow**) 
  - Al pasar por encima de cada carátula se muestran pequeños detalles de está además de los iconos de "Favorito" y "Ver Después". En pantallas pequéñas (principalmente táctiles) se mostrará este contenido al tocar con el dedo en la carátula. Pudiendo ver más detalles si se pulsa en el enlace de "View Details".  (**Hover**)  
  - El main ajusta su margen exterior en función del ancho de la pantalla. En móviles el margen es menor para aprovechar mejor el escaso espacio. (**media query**)  
  
## Página de Detalles:  
  - Secciones organizadas con **css-grid**.  
  - Usando **media queries** se recolocan las celdas.  
    - Encima de los detalles se muestra el path de navegación.  
    - En version móvil se muestra primero la carátula junto con los detalles y debajo botón de "Watch Now" y la descripción. La carátula se hace más grande y más pequeña. (**&lt;source&gt; tag con varias alternativas**)  
    - La ficha del director se muestra en un sitio u otro dependiendo de la pantalla. (**media queries**)  
    - En pantallas más anchas, el botón de "Watch Now" y los detalles quedan debajo de la carátula dejando todo el lado derecho para la descripción y el trailer. (**&lt;video&gt; tag con controles**)  
    - Debajo siempre irá el reparto de la película que en pantallas pequeñas se mostrará en una sola linea con scroll horizontal. (**Flex-box nowrap + overflow**)
  - Debajo del detalle de la película se muestra carrusel con Contenido Relacionado. **CSS reutilizado de Carruseles de página de inicio**  

