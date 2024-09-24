# Configuracion de Gradle

### 1. **Instalar Java Development Kit (JDK)**
   React Native depende de Java, por lo que necesitas tener instalado el JDK. Asegúrate de instalar la versión correcta de Java, generalmente JDK 11 o JDK 17 funcionan bien.

   - Descarga el JDK desde [Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o [OpenJDK](https://openjdk.java.net/).
   - Instálalo y agrega la ruta de instalación a las variables de entorno:
     - Ve a **Configuración del sistema avanzado** → **Variables de entorno**.
     - En **Variables del sistema**, selecciona **Path** y edita.
     - Agrega la ruta `C:\Program Files\Java\jdk-XX\bin`.

### 2. **Instalar Android Studio y Configurar SDK**
   - Descarga e instala [Android Studio](https://developer.android.com/studio).
   - Durante la instalación, asegúrate de que el **Android SDK**, **Android SDK Platform**, y **Android Virtual Device (AVD)** estén seleccionados.
   - Abre Android Studio y ve a **Preferences** → **Appearance & Behavior** → **System Settings** → **Android SDK**. Desde allí, selecciona y descarga las versiones necesarias del SDK.

### 3. **Configurar las Variables de Entorno para Android SDK**
   Después de la instalación, necesitas configurar las variables de entorno para Android SDK y `gradle`.

   - **ANDROID_HOME**:
     - Ve a **Configuración del sistema avanzado** → **Variables de entorno**.
     - Crea una nueva variable de entorno llamada `ANDROID_HOME` y como valor pon la ruta de tu SDK, que suele ser algo como `C:\Users\YourUsername\AppData\Local\Android\Sdk`.
   - Luego, en la misma ventana, selecciona **Path** y agrega estas rutas:
     - `%ANDROID_HOME%\platform-tools`
     - `%ANDROID_HOME%\tools`
     - `%ANDROID_HOME%\tools\bin`

### 4. **Instalar Node.js, npm y React Native CLI**
   - Descarga e instala [Node.js](https://nodejs.org/), que incluye `npm`.
   - Verifica la instalación ejecutando:
     ```bash
     node -v
     npm -v
     ```
   - Instala React Native CLI globalmente:
     ```bash
     npm install -g react-native-cli
     ```

### 5. **Instalar Gradle**
   Aunque Android Studio ya viene con Gradle, a veces es útil instalarlo manualmente.

   - Descarga Gradle desde su sitio web oficial: [https://gradle.org/releases/](https://gradle.org/releases/).
   - Extrae el archivo ZIP y coloca la carpeta de Gradle en una ubicación, por ejemplo, `C:\Gradle\gradle-x.x`.
   - Ve a **Variables de entorno** nuevamente, edita **Path** y agrega la ruta `C:\Gradle\gradle-x.x\bin`.

### 6. **Verifica la Instalación de Gradle**
   Para asegurarte de que Gradle esté correctamente instalado, abre una terminal (CMD o PowerShell) y ejecuta:
   ```bash
   gradle -v
   ```
   Esto debería mostrar la versión instalada de Gradle.

### 7. **Crear un Proyecto React Native**
   Ahora que tienes todo configurado, puedes crear un nuevo proyecto de React Native:
   ```bash
   npx react-native init MyNewApp
   cd MyNewApp
   ```

### 8. **Ejecutar la App en Android**
   Si todo está configurado correctamente, puedes ejecutar tu aplicación en un dispositivo Android conectado o en un emulador:
   ```bash
   npx react-native run-android
   ```

### 9. **Publicar en un Dispositivo Físico**
   Si quieres ejecutar la app en un dispositivo físico:
   - Habilita la **Depuración USB** en tu dispositivo.
   - Conéctalo a tu computadora mediante USB.
   - Asegúrate de que esté detectado con el comando:
     ```bash
     adb devices
     ```
   - Luego, ejecuta:
     ```bash
     npx react-native run-android
     ```

### 10. **Publicar tu Aplicación**
   - Para publicar la aplicación en Play Store, necesitas generar un **keystore** de producción y construir el APK o AAB.
   - Sigue la [documentación oficial de React Native](https://reactnative.dev/docs/signed-apk-android) para firmar y construir el APK listo para producción.

Estos pasos te permitirán trabajar con React Native en Windows y publicar tu app en un dispositivo Android. Si tienes algún problema durante el proceso, no dudes en preguntar.