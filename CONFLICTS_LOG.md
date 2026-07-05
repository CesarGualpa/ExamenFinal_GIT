# CONFLICTS_LOG.md

## Conflicto 1 - Enlaces del menú de navegación

Fecha/Hora: 04/07/2026 - 20:30

Archivos afectados:
- index.html

Descripción del conflicto:
Durante la integración de la rama feature/candidato-a con dev, se detectó un conflicto en los enlaces del menú de navegación. Una versión apuntaba a archivos con nombres como cv_cv1.html y otra versión apuntaba a archivos como cv1.html.

Decisión tomada:
Se decidió usar la estructura solicitada en el examen: cv/cv1.html, cv/cv2.html y cv/cv3.html. Esta decisión permite que los enlaces del menú coincidan con los criterios de validación final.

Código final:
<nav>
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="cv/cv_cv1.html">Candidato 1</a></li>
                <li><a href="cv/cv2.html">Candidato 2</a></li>
                <li><a href="cv/cv3.html">Candidato 3</a></li>
            </ul>
        </nav>


## Conflicto 2 - Ofertas laborales en index.html

Fecha/Hora: 04/07/2026 - 20:40

Archivos afectados:
- index.html

Descripción del conflicto:
Los integrantes modificaron el mismo contenedor de ofertas laborales para agregar sus respectivas tarjetas. Git no pudo decidir automáticamente qué oferta conservar.

Decisión tomada:
Se decidió conservar todas las ofertas laborales, ya que el examen solicita integrar las tarjetas de los integrantes del equipo. El contenedor final mantiene las ofertas A, B y C sin etiquetas de conflicto.

Código final:
El archivo index.html muestra las tres tarjetas de oferta laboral dentro del contenedor de destacados.


## Conflicto 3 - Color de fondo del body

Fecha/Hora: 04/07/2026 - 20:50

Archivos afectados:
- css/styles.css

Descripción del conflicto:
El Estudiante A cambió el fondo del body a lightblue. Otro integrante cambió el fondo del body a lightgreen.

Decisión tomada:
Se decidió mantener background-color: lightblue porque ofrece una apariencia más neutra para el portal y mantiene coherencia visual con el diseño final.

Código final:
body {
    background-color: lightblue;
}


## Conflicto 4 - Diseño del contenedor de destacados

Fecha/Hora: 04/07/2026 - 21:00

Archivos afectados:
- css/styles.css

Descripción del conflicto:
El Estudiante A aplicó display: grid al contenedor de destacados. Otro integrante aplicó display: flex y flex-direction: column al mismo contenedor.

Decisión tomada:
Se decidió mantener display: grid porque permite mostrar las tres ofertas laborales como tarjetas organizadas en columnas. Se descartó flex-direction: column porque mostraba las tarjetas una debajo de otra y no aprovechaba bien el espacio de la pantalla.

Código final:
#contenedor-destacados {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    padding: 20px;
}