# cartopy municipios
Libreta para crear un mapa con las divisiones municipales de México y señalizaciones en puntos en específico.

1. Los archivos .shp son obtenidos de la página de conabio:
    1. [Divisiones estatales](http://www.conabio.gob.mx/informacion/metadata/gis/destdv250k_2gw.xml?_xsl=/db/metadata/xsl/fgdc_html.xsl&_indent=no)
    2. [Divisiones municipales](http://www.conabio.gob.mx/informacion/metadata/gis/muni_2018gw.xml?_httpcache%20=%20yes&_xsl=/db/metadata/xsl/fgdc_html.xsl&_indent%20=%20no) 
1. Aunque es posible graficar todas las divisiones municipales sin manipular el shp municipal, opté por únicamente filtrar los municipios de un estado para no saturar la imagen. Esto es con la paquetería geopandas y se realiza un filtro sobre el nombre del estado (NOM_ENT) para únicamente tener la información de ese estado. La nomenclatura es la misma que en un df de pandas.
1. La posición de los letreros están referenciados en la imagen usando el mismo sistema de coordenadas del mapa.
1. El estilo de las cajas de texto y las flechas es altamente personalizable dentro de los comandos arrowprops y bbox, es recomendable leer la documentación para conocer mayores propiedades.
