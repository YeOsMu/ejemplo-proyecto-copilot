# ejemplo-proyecto-copilot
Proyecto de prueba para Estructura de Datos 2
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog Técnico: Tablas Hash</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Blog Técnico: Tablas Hash</h1>
        <nav>
            <ul>
                <li><a href="#post1">Introducción</a></li>
                <li><a href="#post2">Colisiones</a></li>
                <li><a href="#post3">Implementación</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="post1">
            <h2>Post #1: Introducción a las Tablas Hash</h2>
            <p>Una <strong>Tabla Hash</strong> es una estructura de datos que asocia claves (<em>key</em>) con valores (<em>value</em>) usando una <strong>función hash</strong> para calcular el <strong>índice</strong> donde se almacena cada par clave-valor. Las tablas hash son muy eficientes, permitiendo operaciones promedio de <strong>O(1)</strong> para insertar, buscar y eliminar.</p>
            <ul>
                <li><strong>Clave (key):</strong> Identificador único.</li>
                <li><strong>Valor (value):</strong> Dato asociado a la clave.</li>
                <li><strong>Función hash:</strong> Algoritmo que convierte la clave en un índice.</li>
                <li><strong>Índice:</strong> Posición en el arreglo base.</li>
                <li><strong>Colisiones:</strong> Cuando dos claves generan el mismo índice.</li>
            </ul>
            <h3>¿Por qué son tan eficientes?</h3>
            <p>Las operaciones de inserción, búsqueda y eliminación suelen ser O(1) gracias a la función hash.</p>
            <h3>Ejemplo visual</h3>
            <img src="img/hash-diagrama1.svg" alt="Diagrama función hash" style="max-width:400px;">
        </section>
        <section id="post2">
            <h2>Post #2: Manejo de Colisiones en Tablas Hash</h2>
            <p>Las colisiones ocurren cuando dos claves diferentes generan el mismo índice. Las dos estrategias más comunes para manejarlas son:</p>
            <h3>1. Encadenamiento (Chaining)</h3>
            <ul>
                <li>Cada posición almacena una lista enlazada.</li>
                <li>Fácil de implementar y crece dinámicamente.</li>
            </ul>
            <h3>2. Direccionamiento Abierto (Open Addressing)</h3>
            <ul>
                <li><strong>Linear Probing:</strong> Busca la siguiente celda libre.</li>
                <li><strong>Quadratic Probing:</strong> Busca en saltos cuadráticos.</li>
                <li><strong>Double Hashing:</strong> Usa una segunda función hash.</li>
            </ul>
            <h3>Ejemplo visual</h3>
            <img src="img/hash-diagrama2.svg" alt="Diagrama colisiones" style="max-width:400px;">
        </section>
        <section id="post3">
            <h2>Post #3: Implementación y Operaciones Fundamentales</h2>
            <h3>Insertar (<em>put</em>)</h3>
            <p>Se calcula el hash de la clave, se obtiene el índice y se almacena el par clave-valor.</p>
            <h3>Buscar (<em>get</em>)</h3>
            <p>Se accede al índice y se localiza el valor asociado a la clave.</p>
            <h3>Eliminar (<em>delete</em>)</h3>
            <ul>
                <li>En chaining: se elimina el nodo de la lista.</li>
                <li>En open addressing: se marca la celda como "deleted".</li>
            </ul>
            <h3>Ejemplo visual</h3>
            <img src="img/hash-diagrama3.svg" alt="Diagrama operaciones" style="max-width:400px;">
        </section>
    </main>
    <footer>
        <p>Blog técnico desarrollado para la actividad de Estructura de Datos I.</p>
    </footer>
    <script src="scripts.js"></script>
</body>
</html>
