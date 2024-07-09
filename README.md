# TALLER-INDIVIDUAL
![image](https://github.com/Marylin-Rosero/TALLER-INDIVIDUAL/assets/169502533/3c044d86-a956-48ee-9423-883a0ec3e3a8)
![image](https://github.com/Marylin-Rosero/TALLER-INDIVIDUAL/assets/169502533/4c5fd068-981b-45fa-95f1-d51248962f84)
![image](https://github.com/Marylin-Rosero/TALLER-INDIVIDUAL/assets/169502533/e71556c6-d3e7-4ed1-9d16-1c5177ce16af)

El código proporcionado es una aplicación de interfaz gráfica en Java Swing que se conecta a una base de datos PostgreSQL para mostrar información sobre pilotos de Fórmula 1 según el año seleccionado en un combo box. Aquí tienes un resumen de lo que hace cada parte del código:

1. *Paquetes e importaciones: Importa las clases necesarias de Java Swing y SQL.

2. Clase `InterfazGrafica`:
   - Atributos: `conn` para la conexión a la base de datos, `frame` para la ventana principal, `comboBox` para seleccionar el año de carrera, `table` para mostrar los datos en una tabla, y `tableModel` para manejar los datos de la tabla.
   
   - Constructor `InterfazGrafica()`:
     - Establece la conexión a la base de datos llamando al método `connectDB()`.
     - Crea la interfaz gráfica llamando al método `createGUI()`.

   - Método `connectDB()`:
     - Establece la conexión con PostgreSQL utilizando los parámetros de URL, usuario y contraseña especificados.

   - Método `createGUI()`:
     - Crea y configura la ventana (`JFrame`) con un título y tamaño predefinido.
     - Crea un combo box (`JComboBox`) para seleccionar el año de carrera.
     - Crea una tabla (`JTable`) para mostrar los datos de los pilotos y carreras.
     - Centra el contenido de las celdas de la tabla.

   - Método `populateComboBox()`:
     - Ejecuta una consulta SQL para obtener los años disponibles desde la base de datos y los agrega al combo box.

   - Método `updateTable()`:
     - Actualiza la tabla de pilotos según el año seleccionado en el combo box.
     - Ejecuta una consulta SQL compleja que obtiene el nombre del piloto, victorias, puntos totales y posición en las carreras para el año seleccionado.
     - Organiza los datos obtenidos en vectores y actualiza el modelo de la tabla con estos datos.
     - Centra el contenido de las celdas de la tabla.

   - Método `main()`:
     - Inicia la aplicación Swing en el hilo de despacho de eventos (`Event Dispatch Thread`).

En resumen, este código crea una interfaz gráfica que permite seleccionar un año de carrera de Fórmula 1 y muestra información detallada sobre los pilotos, incluyendo sus victorias, puntos totales y posición en las carreras de ese año, todo gestionado desde una base de datos PostgreSQL.
