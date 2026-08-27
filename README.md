# 📱 App Países 

Aplicación móvil Android desarrollada en **Kodular Creator** integrada con **Firebase Realtime Database** y **Firebase Authentication** para la gestión de información de países.

---

## Contenido del Repositorio

* `App_Paises.aia`: Código fuente completo del proyecto para importar en Kodular.
* `App_Paises.apk`: Archivo ejecutable/instalador compilado para dispositivos Android.
* `README.md`: Documentación e instrucciones de despliegue y configuración.

---

## Configuración de Seguridad (Firebase)

> **Nota de Privacidad y Seguridad:** Por buenas prácticas de desarrollo y protección de datos, el archivo `google-services.json` ha sido excluido del repositorio público para evitar la exposición de llaves privadas de la base de datos de producción.

Para ejecutar la aplicación o probar la interacción con la base de datos en tiempo real, el usuario o evaluador debe vincular su propio archivo de credenciales de Firebase siguiendo estos pasos:

### Crear / Configurar el proyecto en Firebase
1. Ingrese a [Firebase Console](https://console.firebase.google.com/) y cree un nuevo proyecto.
2. En la sección **Build > Authentication**, habilite el proveedor de inicio de sesión por **Correo electrónico/Contraseña**.
3. En la sección **Build > Realtime Database**, cree una base de datos y active la regla de lectura y escritura (`read: true, write: true`).
4. Añada una aplicación Android a su proyecto Firebase registrando el **Package Name** (ejemplo: `com.miusuario.apppaises`).
5. Descargue el archivo de configuración **`google-services.json`**.

### Vincular credenciales en Kodular
1. Ingrese a [Kodular Creator](https://creator.kodular.io/).
2. Seleccione **Project > Import project (.aia)** y cargue el archivo `App_Paises.aia` de este repositorio.
3. Abra el panel lateral derecho **Assets** en Kodular.
4. Suba el archivo **`google-services.json`** descargado previamente desde su consola de Firebase.
5. Verifique que el **Package Name** en **Project Settings ⚙️ > Publishing** coincida exactamente con el de su proyecto Firebase.

---

## Instrucciones de Instalación y Pruebas

### Opción 1: Probar el APK (Instalador Android)
1. Transfiera o descargue el archivo `App_Paises.apk` a su dispositivo Android.
2. Habilite la opción de **Instalar aplicaciones de fuentes desconocidas** en los ajustes del dispositivo.
3. Abra e instale el ejecutable APK.

### Opción 2: Probar el Código Fuente (AIA) en Kodular
1. Importe el archivo `App_Paises.aia` en Kodular Creator.
2. Realice la vinculación del archivo `google-services.json` (ver sección de seguridad arriba).
3. En el menú superior de Kodular, seleccione **Test > Connect to Companion** para probar en tiempo real mediante la app móvil *Kodular Companion*, o seleccione **Export > Android App (.apk)** para compilar su propia versión instalable.

---

## Información del Desarrollador

* **Autor:** Jose Rivera
* **Plataforma:** Kodular Creator
* **Servicios de Backend:** Firebase Authentication / Realtime Database
