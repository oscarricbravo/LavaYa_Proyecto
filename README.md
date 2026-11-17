# PROYECTO FINAL DE A Y P
Autores: OSCAR BRAVO, AIDAN ORJUELA, NIKOLAS SARRIA

PROBLEMA

En los autolavados tradicionales los clientes suelen enfrentarse a largas filas, tiempos de espera impredecibles y horarios de atención limitados, lo que genera congestión en horas pico y pérdida de tiempo tanto para los conductores como para el personal operativo. Por otro lado, la gestión manual de turnos en papel o sin control centralizado provoca cruces de horarios, desorden en el registro de vehículos y dificultad para llevar un control claro de las ventas diarias.

USUARIO

La aplicación está pensada para dos tipos de personas:

Clientes: Conductores de automóvil, camioneta o motocicleta que quieren lavar su vehículo rápido, sin hacer filas y eligiendo el horario que más les convenga desde su celular durante las 24 horas del día.
Administrador: La persona encargada del autolavado, que necesita ver en pantalla los turnos agendados, borrar los servicios que ya se atendieron y saber cuánto dinero se ha recaudado en total.
OBJETIVOS

Objetivo General: Desarrollar un prototipo funcional de aplicación móvil en Python que permita a los conductores reservar turnos de autolavado desde su celular las 24 horas sin hacer fila, llevando el control de los clientes, los horarios disponibles y las ventas del negocio.
Objetivos Específicos:

Permitir que los clientes se registren e inicien sesión con su correo "@gmail.com", evitando que se repitan usuarios, correos o placas.
Guiar al cliente paso a paso para elegir su vehículo, el tipo de lavado (30 minutos, 1 hora o 2 horas) y la hora de su turno.
Bloquear automáticamente las horas que ya fueron reservadas por otros clientes para que no haya cruces ni filas.
Crear un panel de administrador donde se guarden todos los pedidos en un archivo de texto (datos.txt), se puedan eliminar turnos ya atendidos y se calcule el dinero total recaudado.
REQUERIMIENTOS

Tipo de aplicación: Prototipo funcional con interfaz diseñada en formato móvil (pantalla vertical tipo smartphone), ejecutado en computador mediante Python o archivo ".exe" para facilitar su prueba y demostración.
Lenguaje: Python 3.
Librerías utilizadas: "tkinter" para crear las ventanas y botones de la aplicación, y "os" para verificar si el archivo donde se guardan los datos ya existe.
Almacenamiento: Un archivo de texto sencillo (datos.txt) donde quedan guardados todos los pedidos realizados.
Equipo: Funciona en cualquier computador con Windows, Linux o Mac que tenga Python instalado.
FUNCIONAMIENTOS

BACKEND: Es la parte interna del programa donde se hacen los cálculos, revisiones y el guardado de datos:

Registro e inicio de sesión: Guarda los datos de cada cliente (nombre, usuario, correo, contraseña y placa) y revisa que nadie cree dos cuentas con el mismo usuario, correo o placa. También verifica que solo puedan entrar personas ya registradas.

Control de horarios disponibles: Revisa el archivo "datos.txt" antes de mostrar los turnos para saber qué horas ya están ocupadas y bloquearlas.

Guardado y cuentas: Cada vez que alguien confirma un turno, lo escribe en una línea nueva dentro de "datos.txt". También suma el valor de todos los pedidos para mostrarle al administrador el total recaudado y permite borrar un pedido cuando ya se atendió.

FRONTEND: Es la parte visual tipo aplicación móvil con la que interactúan el cliente y el administrador:

Pantalla de bienvenida, registro y acceso: Permite crear cuenta o iniciar sesión, acomodando automáticamente las placas en mayúscula y los correos en minúscula, y mostrando avisos claros si falta algún dato o si hay un error.
Reserva en 4 pasos:
Vehículo: El cliente elige entre automóvil, camioneta o motocicleta.
Tipo de lavado: Elige entre lavado de 30 minutos, 1 hora o 2 horas según lo que necesite.
Turno 24 horas: Muestra los horarios disponibles en botones; si una hora ya está tomada, aparece marcada como "Ocupado" y no se puede seleccionar.
Confirmación: Muestra el resumen del pedido antes de guardarlo.
Panel de administrador: Se entra con clave (admin123) y muestra en una sola línea cada pedido registrado, el total de dinero ganado y un botón para eliminar pedidos y volver a liberar ese turno.
VALIDACIÓN

Para comprobar que la aplicación fuera fácil de usar y realmente resolviera el problema de las filas, realizamos pruebas de uso con personas (compañeros de estudio, familiares, vecinos), pidiéndoles que se registraran, agendaran un turno y revisaran la información sin ayuda previa.

Hallazgos y mejoras realizadas a partir de las pruebas:

Claridad en el registro e inicio de sesión:

Durante las pruebas notamos que si alguien escribía mal su usuario o intentaba entrar sin registrarse, el sistema no le avisaba. Gracias a esto agregamos alertas claras cuando el usuario no existe, cuando la contraseña es incorrecta o cuando se intenta repetir un correo "@gmail.com" o nombre de usuario.
Facilidad para elegir turno sin confusiones:

Los usuarios de prueba destacaron que ver los horarios ocupados marcados y bloqueados evita tener que preguntar disponibilidad y da seguridad de que no habrá fila al llegar.
Mejor lectura en el panel del administrador:

Al probar la vista de administración, se observó que los datos de cada cliente se veían pequeños y desordenados. Se ajustó la lista para mostrar cada pedido en una sola línea numerada y en negrita, facilitando revisar las ventas del día de un vistazo.
Evidencias de prueba:
