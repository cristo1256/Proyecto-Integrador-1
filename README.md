Proyecto Integrador Flutter (Windows + Código VS)

1. Configuración del entorno (4 puntos)
Instalación completa del entorno Flutter en Windows , utilizando Visual Studio Code como
editor principal y Android Studio únicamente para el SDK y el emulador.
1.1 Instalación de Git
Git es necesario para que Flutter funcione correctamente y para subir el proyecto a GitHub.
Pasos:
1. Ir a la página oficial:
https://git-scm.com/downloads
2. Descargar Git para Windows .
3. Ejecutar el instalador.
4. Presionar Next en todas las opciones por defecto.
5. Finalizar la instalación.

Evidencia1:
![imagen](https://github.com/cristo1256/Proyecto-Integrador-1/blob/main/1.png)

1.2 Instalación de Visual Studio Code (Editor principal)
VS Code será el editor donde escribirás tu código Flutter.
Pasos:
1. Ir a:
https://code.visualstudio.com/
2. Descargar VS Code para Windows .
3. Instalar con opciones por defecto.
Extensiones necesarias:

Abrir VS Code → pestaña Extensions (icono de cuadritos) → instalar:
● Flutter
● Dart

Evidencia2:
![imagen](https://github.com/cristo1256/Proyecto-Integrador-1/blob/main/2.png)

1.3 Instalación de Android Studio (solo para SDK y emulador)
Aunque usarás VS Code, Android Studio es necesario para:
● Android SDK
● Herramientas de plataforma
● Emuladores (AVD Manager)
Pasos:

Ir a:
https://developer.android.com/studio
Descargar Android Studio.
Instalar con opciones por defecto.
1.4 Configurar Android Studio
1.4.1 Instalar Android SDK

Abrir Android Studio.
En la pantalla inicial, seleccione Más acciones → Administrador de SDK .
Verifique que estén instalados:
○ ✔ Android SDK 34 o superior
○ ✔ Android SDK Platform Tools
○ ✔ Android Emulator

Evidencia3:
![imagen](https://github.com/cristo1256/Proyecto-Integrador-1/blob/main/3.png)

1.4.2 Crear un emulador de Android

En la pantalla inicial de Android Studio → Más acciones → AVD Manager .
Crear un nuevo dispositivo:
○ Seleccionar Pixel 5 o similar.
○ Elegir imagen del sistema: Android 13 o 14 .
Finalizar.
Evidencia:
1.5 Instalación del Flutter SDK en Windows
Pasos:
Ir a:
https://docs.flutter.dev/get-started/install/windows (docs.flutter.dev en Bing)
Descargue el archivo ZIP de Flutter.
Extraerlo en una carpeta, por ejemplo:
C:\src\flutter
Agregar Flutter al PATH:
Cómo agregar Flutter al PATH en Windows:
Abrir Panel de Control .
Vaya a:
Sistema → Configuración avanzada → Variables de entorno.
En Variables del sistema , seleccione Ruta → Editar .
Agregar la ruta:
C:\src\flutter\bin
Guardar.
1.6 Verificar instalación de Flutter
Abrir PowerShell o CMD y ejecutar:
flutter --version
Evidencia:
1.7 Ejecutar flutter doctor
Este comando verifica que todo esté correctamente instalado.
flutter doctor
Debe mostrar:
● ✔ Flutter instalado
● ✔ Cadena de herramientas de Android configurada
● ✔ VS Code detectado
● ✔ Dispositivo disponible

Evidencia:
1.8 Verificar dispositivos disponibles
Ejecutar:
flutter devices
Debe aparecer:
● Tu emulador Android
o
● Tu teléfono físico conectado por USB
Evidencia:

2. Creación y ejecución del proyecto (3 puntos)
2.1 Crear el proyecto Flutter
En VS Code:

Abrir la paleta de comandos (Ctrl + Shift + P).
Escribir:
Flutter: New Project
Seleccionar Aplicación .
Elegir carpeta donde guardar el proyecto.
Asignar nombre:
proyecto_flutter
Evidencia:
2.2 Ejecutar la aplicación
En VS Code:
Abrir el archivo main.dart.
Presionar F5 o ejecutar:
flutter run
La aplicación debe abrirse en el emulador.
Pruebas:
3. Modificaciones básicas (4 puntos)
Se modificó el archivo lib/main.dart para cumplir con los requisitos.
3.1 Cambios realizados
● ✔ Título de la aplicación
● ✔ Texto principal
● ✔ Color del AppBar
● ✔ Botón que muestra un SnackBar
3.2 Código implementado
import 'package:flutter/material.dart';
void main() {
runApp(const MiAplicación());
}
clase MiAplicación extiende StatelessWidget {
const MiAplicación({super.key});

@override
Widget build(BuildContext context) {
return MaterialApp(
title: 'Mi App Modificada',
home: const HomeScreen(title: 'Hola esta es mi aplicación Cristopher
Mejia'
),
);
}
}
class HomeScreen extends StatelessWidget {
const HomeScreen({super.key});
@override
Widget build(BuildContext context) {
return Scaffold(
appBar: AppBar(
title: const Text('Pantalla Principal'),
backgroundColor: Colors.purple,
),
body: Center(
child: ElevatedButton(
onPressed: () {
ScaffoldMessenger.of(context).showSnackBar(
const SnackBar(content: Text('Botón presionado')),
);
},
child: const Text('Mostrar SnackBar'),
),
),
);
}
}

Evidencia:

4. Navegación entre pantallas (2 puntos)
4.1 Botón para ir a la segunda pantalla
ElevatedButton(
onPressed: () {
Navigator.push(
context,
MaterialPageRoute(builder: (context) => const SecondScreen()),
);
},
child: const Text('Ir a segunda pantalla'),
)
4.2 Segunda pantalla
class SecondScreen extends StatelessWidget {
const SegundaPantalla({super.key});
@anular

Widget build(BuildContext context) {
return Scaffold(
appBar: AppBar(
title: const Text('Segunda Pantalla'),
),
body: Center(
child: ElevatedButton(
onPressed: () {
Navigator.pop(context);
},
child: const Text('Regresar'),
),
),
);
}
}
Evidencia:

5. Uso de GitHub (1 punto)
5.1 Crear repositorio
1. Ir a https://github.com
2. Crear repositorio público
3. Subir el proyecto con:
git init
git add.
git commit -m "Primer commit"
git rama -M principal
git remoto agregar origen https://github.com/usuario/repositorio.git
git push -u origen principal

Evidencia:

6. README.md (1 punto)

Proyecto Flutter — Evaluación
Descripción
Aplicación Flutter creada para demostrar la correcta instalación del entorno, ejecución de un
proyecto, modificaciones básicas y navegación entre pantallas.

Características
Cambio de título y AppBar
Botón con SnackBar
Navegación entre pantallas
Repositorio con commits reales

