# Capítulo IV: Product Implementation & Validation

## 4.1.Software Configuration Management

### 4.1.1.Software Development Environment Configuration

Para asegurar una colaboración eficiente y mantener la calidad en el desarrollo de **Chapa Tu Ruta**, se ha definido un entorno de desarrollo común para todos los miembros del equipo. A continuación, se listan los productos de software utilizados en las distintas etapas del ciclo de vida del producto digital, indicando su propósito y su enlace de referencia o descarga correspondiente.

**Product UX/UI Design**

Para el diseño de la experiencia de usuario y la interfaz de la Landing page de Eventify, se utilizaron las siguientes herramientas:

- Figma: Se empleó para la creación de wireframes, mock-ups y prototipos de la aplicación web.[https://www.figma.com/es-es/](https://www.figma.com/es-es/)
- UXPressia: Utilizada para elaborar User Personas, Empathy Maps, Journey Maps e Impact Maps. [https://uxpressia.com/](https://uxpressia.com/)
- Miro: Se utilizó para la creación de Event Storming, Domain Message Flow Modelling, Bounded Context Canvases. [https://miro.com/es/](https://miro.com/es/)

**Software Development**

Para el desarrollo del software del Landing Page, Backend y Mobile App, se adoptaron los siguientes productos:

- WebStorm (Instalación local): Utilizado como entorno de desarrollo para trabajar con HTML, CSS y JavaScript. [https://www.jetbrains.com/es-es/webstorm/](https://www.jetbrains.com/es-es/webstorm/)
- Android Studio (Instalación local): Este es un IDE para desarrollar aplicaciones móviles para Android, utilizando Kotlin y JetPack Compose. [https://developer.android.com/studio?hl=es-419](https://developer.android.com/studio?hl=es-419)
- Rider(Instalación local): Utilizamos este IDE para desarrollar el backend de la aplicación. [https://www.jetbrains.com/es-es/rider](https://www.jetbrains.com/es-es/rider)
- Git (Instalación local): Empleado para gestionar los cambios de código de manera local mediante commits y ramas. [https://git-scm.com/](https://git-scm.com/)
- GitHub: Plataforma de repositorio remoto para la gestión de versiones del código, implementando el flujo GitFlow para garantizar un desarrollo organizado. [https://github.com/](https://github.com/)

**Project Management and Collaboration**

En la gestión de proyectos y colaboración del equipo se utilizaron:

- **Trello:** Utilizado para la planificación y seguimiento de tareas, distribuidas en listas de "por hacer", "en progreso" y "hecho".
- **WhatsApp:** Medio de comunicación instantánea para coordinar avances, resolver dudas rápidas y hacer recordatorios. [https://web.whatsapp.com/](https://web.whatsapp.com/)
- **Google Meet:** Herramienta utilizada para realizar reuniones virtuales más formales, presentaciones de avances y coordinación general del equipo. [https://www.zoom.com/es](https://www.zoom.com/es)

**Software Documentation**

Para la documentación del proyecto se emplearon las siguientes herramientas:
 
- Lucidchart: Utilizada para la creación de diagramas UML, wireflows y user flows que ayudan en la planificación y visualización del sistema. [https://www.lucidchart.com/pages](https://www.lucidchart.com/pages)
- Visual Paradigm: Herramienta usada para modelar la arquitectura de software mediante diagramas C4. [https://online.visual-paradigm.com/drive/#proj=0&dashboard](https://online.visual-paradigm.com/drive/#proj=0&dashboard)


### 4.1.2.Source Code Management

La gestión del código fuente es una parte fundamental en el desarrollo colaborativo de software, ya que permite un control eficiente sobre las modificaciones realizadas en el proyecto a lo largo de su ciclo de vida. En esta sección del informe, se describe el sistema de control de versiones implementado en el proyecto Chapa Tu Ruta, utilizando GitHub como plataforma principal. Además, se detallan las convenciones de trabajo adoptadas por el equipo, como el modelo GitFlow, el versionado semántico (Semantic Versioning) y las convenciones de commit mediante Conventional Commits. Estas prácticas aseguran un desarrollo ordenado y una integración continua efectiva entre los miembros del equipo.

**URL de los Repositorios:**
- Organización: [https://github.com/Aplicaciones-Moviles-Grupo](https://github.com/Aplicaciones-Moviles-Grupo)
- Reporte: [https://github.com/Aplicaciones-Moviles-Grupo/Report](https://github.com/Aplicaciones-Moviles-Grupo/Report)
- Landing Page: [https://github.com/Aplicaciones-Moviles-Grupo/landing-page-original](https://github.com/Aplicaciones-Moviles-Grupo/landing-page-original)
- Backend: [https://github.com/Aplicaciones-Moviles-Grupo/ChapaTuRutaBackend](https://github.com/Aplicaciones-Moviles-Grupo/ChapaTuRutaBackend)
- Aplicación Movil: [https://github.com/Aplicaciones-Moviles-Grupo/ChapaTuRuta-MobileApp](https://github.com/Aplicaciones-Moviles-Grupo/ChapaTuRuta-MobileApp)

**Estructura de Ramas:**

Para mantener un flujo organizado en el desarrollo y facilitar la colaboración, se ha implementado el modelo GitFlow, creando las siguientes ramas:

- Main Branch: Rama principal (main) que contiene las versiones estables del proyecto. Todas las demás ramas derivan de esta.
- Develop: Rama secundaria donde se integran todas las características nuevas antes de fusionarse a la rama main.
- Feature Branches: Estas ramas se crean a partir de develop y son en base a las características del proyecto. Una vez se termina de trabajar en la rama, se hace merge hacia develop.

**Convenciones de commits:**

Para la escritura de commits en el proyecto Eventify, se sigue la convencion 'Conventional Commits', el cual cuenta con un formato estándar para facilitar la lectura y entendimiento del historial de cambios dentro del proyecto.
```
    <type>[optional scope]: <description>
    
    [optional body]
    
    [optional footer(s)]
```
- Type:
    - feat: Añadir una nueva característica.
    - fix: Correción de errores.
    - docs: Modificaciones en la documentación.
    - style: Cambios que no afectan la lógica del código.
    - refactor: Modificaciones que no añaden características y/o errores.
    - test: Adición/Modificación de pruebas.


- Scope: Brinda información extra acerca del área del codigo afectado.
```
   feat(auth): add register functionality.
```
**Ejemplos básicos de commits:**
```
   feat(login): add organizer authentication module.
```
```
   fix(payment): resolve payment security issue.
```
```
   docs(README): update index instructions.
```

### 4.1.3.Source Code Style Guide & Conventions

**Nomenclatura General**

Para el desarrollo de la aplicación móvil en **Android Studio** utilizando **Kotlin** y **Jetpack Compose** bajo el patrón **Clean Architecture**, se aplicarán convenciones de nomenclatura establecidas por **Google Kotlin Style Guide** y **Jetpack Compose Guidelines**.  

Los nombres deben ser claros, expresivos y en inglés. Se empleará **camelCase** para variables y funciones, **PascalCase** para clases y componentes de UI, y **snake_case** solo para recursos XML.

Ejemplos:

```kotlin
// Variables y funciones (camelCase)
val userName: String
fun getUserProfile()

// Clases y componentes (PascalCase)
class LoginViewModel
@Composable
fun HomeScreen()

// Recursos XML (snake_case)
ic_user_avatar.png
activity_main.xml
```

**Sangría**

En Kotlin, la sangría debe ser de 4 espacios por bloque. No se recomienda el uso de tabulaciones, de acuerdo con las convenciones oficiales de Android Developers.
Kotlin

Kotlin es el lenguaje principal utilizado en el proyecto. Las siguientes pautas aseguran consistencia y legibilidad en el código:
```
fun calculateDistance(origin: Location, destination: Location): Float {
    val result = FloatArray(1)
    Location.distanceBetween(
        origin.latitude,
        origin.longitude,
        destination.latitude,
        destination.longitude,
        result
    )
    return result[0]
}
```
**Uso de val y var**

Siempre que sea posible, utilizar val en lugar de var para definir variables inmutables, siguiendo el principio de inmutabilidad recomendado por Google (s.f.).
```
val userName = "Adrian"
var userAge = 21
```

**Formato de funciones y clases**

Las llaves de apertura deben ir en la misma línea que la declaración, y la llave de cierre en su propia línea.
```
class UserRepository {
    fun getUserById(id: String): User {
        return userDao.getUser(id)
    }
}
```

**Espaciado**

Se debe incluir un espacio después de los dos puntos en las declaraciones de tipos y entre operadores.

```
val distance: Float = 23.5f
val sum = x + y
```

**Imports**

No se deben utilizar imports comodín (import com.example.*). Se deben importar solo las clases necesarias.

import com.frock.chapaturuta.core.ui.theme.PrimaryColor
import androidx.compose.material3.Text


**Jetpack Compose**

Compose se usa para la interfaz de usuario. Las convenciones aseguran consistencia visual y estructural.

**Nomenclatura de Composables**

Los nombres de las funciones composables deben usar PascalCase y terminar con la palabra Screen o Component dependiendo de su función.

@Composable
fun LoginScreen(navController: NavController)

@Composable
```
fun RouteCard(routeName: String, onClick: () -> Unit)
```

**Estructura y legibilidad**

Cada Composable debe tener una estructura clara y con espaciado adecuado para mejorar la legibilidad.
```
@Composable
fun HomeScreen() {
    Column(
        modifier = Modifier
            .fillMaxSize()
            .padding(16.dp),
        verticalArrangement = Arrangement.Center,
        horizontalAlignment = Alignment.CenterHorizontally
    ) {
        Text(text = "Welcome to ChapaTuRuta!", style = MaterialTheme.typography.titleLarge)
        Spacer(modifier = Modifier.height(20.dp))
        Button(onClick = { /* Navigate to routes */ }) {
            Text("Explore Routes")
        }
    }
}
```

**Uso de colores y temas**

Los colores y estilos deben provenir del archivo de tema ubicado en core/ui/theme/, respetando las convenciones de Material Design 3.
```
Button(
    onClick = { /* TODO */ },
    colors = ButtonDefaults.buttonColors(containerColor = PrimaryColor)
) {
    Text("Register", color = Color.White)
}
```

**Clean Architecture**

El proyecto sigue la arquitectura en capas Domain, Data, y Presentation, donde cada capa tiene una responsabilidad definida:

Domain Layer
Contiene los casos de uso (use cases) y las entidades del negocio.
```
class GetUserUseCase(private val repository: UserRepository) {
    suspend operator fun invoke(id: String): User {
        return repository.getUserById(id)
    }
}
```

**Data Layer**
Gestiona las fuentes de datos (API, base de datos local).
```
class UserRepositoryImpl(private val api: UserApi) : UserRepository {
    override suspend fun getUserById(id: String): User {
        return api.getUser(id)
    }
}
```

**Presentation Layer**
Maneja la lógica de interfaz (ViewModel + Composables).
```
@HiltViewModel
class LoginViewModel @Inject constructor(
    private val loginUseCase: LoginUseCase
) : ViewModel() {
    var uiState by mutableStateOf(LoginUiState())
        private set

    fun onLoginClicked() {
        viewModelScope.launch {
            uiState = uiState.copy(isLoading = true)
            loginUseCase(uiState.email, uiState.password)
        }
    }
}
```

**XML (Resources)**

Aunque Jetpack Compose reemplaza gran parte del XML, se mantendrán recursos para íconos, cadenas y temas.

**Nombres de archivos**

Deben escribirse en snake_case, en minúsculas.
```
ic_logo_app.xml
background_primary.xml
colors.xml
strings.xml
```
**Cadenas**

Todas las cadenas visibles al usuario deben almacenarse en res/values/strings.xml.
```
<string name="app_name">ChapaTuRuta</string>
<string name="login_button">Iniciar sesión</string>
```

### 4.1.4.Software Deployment Configuration
**Landing Page**

Para el despliegue de la **Landing Page**, se utilizó **GitHub Pages**, la funcionalidad integrada de GitHub que permite publicar sitios web estáticos de manera sencilla y gratuita.

### Proceso de implementación

- **Creación del repositorio:**  
  Desde la cuenta de GitHub, se seleccionó la opción **"New Repository"** para crear un nuevo repositorio donde se alojará el proyecto.

- **Configuración del repositorio:**  
  Se asignó un nombre identificativo al repositorio y se configuró con visibilidad **pública**, requisito necesario para que GitHub Pages pueda realizar el despliegue del sitio.

**Configuración del despliegue con GitHub Pages**

Para proceder con el despliegue de la **Landing Page**, se creó una nueva rama denominada `feature/chapter-IV-deployment`, con el objetivo de mantener aislados los cambios relacionados con la configuración del entorno de publicación.  
A continuación, se ejecutó el comando `git branch` para verificar las ramas activas en el repositorio, confirmando que la rama actual de trabajo era la recién creada.

Posteriormente, se instaló el paquete **gh-pages** mediante el siguiente comando:

```bash
npm install gh-pages --save-dev
```
![img_1.png](img_1.png)

**Ejecución del despliegue**

Una vez instalada la dependencia **gh-pages** y configurado el script de despliegue en el archivo `package.json`, se procedió a ejecutar el comando:

```bash
npm run deploy
```
![img_2.png](img_2.png)
**Configuración de github Pages**

Una vez ejecutado el despliegue con `npm run deploy`, el sitio quedó alojado en la rama **`gh-pages`** del repositorio.  
Para finalizar la configuración, se accedió a la pestaña **Settings → Pages** dentro del repositorio de GitHub.

### Detalles de la configuración

- **Fuente de despliegue (Source):**  
  Se seleccionó la opción **"Deploy from a branch"**, indicando que el sitio será publicado directamente desde una rama del repositorio.

- **Rama de publicación (Branch):**  
  Se estableció la rama **`gh-pages`** como la fuente del sitio, con el directorio raíz **`/(root)`**, lo que permite a GitHub Pages leer directamente los archivos estáticos generados en la carpeta `dist` durante el proceso de build.

- **URL del sitio:**  
  GitHub genera automáticamente la URL de acceso público:  
  👉 [https://aplicaciones-moviles-grupo.github.io/landing-page-original/](https://aplicaciones-moviles-grupo.github.io/landing-page-original/)

Esta configuración asegura que la **Landing Page** se mantenga disponible en línea y que cualquier actualización futura en el código pueda desplegarse fácilmente con un nuevo `npm run deploy`.

![img_3.png](img_3.png)


## 4.2.Landing Page & Mobile Application Implementation

### 4.2.1.Sprint 1

#### 4.2.1.1.Sprint Planning 1

En este primer sprint, el equipo se centró en el desarrollo y mejora de la aplicación móvil “Chapa Tu Ruta” en Android Studio.  
El objetivo principal fue implementar las principales vistas funcionales y establecer la navegación entre ellas.  

Las tareas se distribuyeron de la siguiente manera:

- **Adrián Valerio**: Implementación de las vistas de **Login** y **Registro de usuario** (RegisterUserView y RegisterProfileView), además de la configuración del **AppNavHost** para gestionar la navegación.
- **Yasser Renteria**: Desarrollo de la **pantalla de creación de rutas**, enfocada en permitir al conductor o usuario registrar rutas personalizadas dentro de la app móvil.
- **Renzo Araujo**: Implementación de la **página de edición de perfil**, donde los usuarios pueden actualizar sus datos personales y de vehículo.
- **Fabrizio Cutiri**: Creación de la **página principal (Home)** que sirve como punto de inicio después del inicio de sesión, mostrando las rutas y accesos a las demás funcionalidades.

También se añadió el **logo oficial de la aplicación** en todas las vistas principales para unificar la identidad visual.

#### 4.2.1.2.Sprint Backlog 1

| ID | Historia de Usuario | Descripción | Prioridad | Responsable | Estado |
|----|----------------------|-------------|------------|--------------|---------|
| HU-01 | Inicio de Sesión | Como usuario, quiero iniciar sesión con mis credenciales para acceder a la app. | Alta | Adrián | Completado |
| HU-02 | Registro de Usuario | Como nuevo usuario, quiero registrarme ingresando mis datos personales y del vehículo. | Alta | Adrián | Completado |
| HU-03 | Crear Ruta | Como conductor, quiero registrar rutas para ofrecer mis servicios. | Media | Yasser | En desarrollo |
| HU-04 | Editar Perfil | Como usuario, quiero editar mi información personal para mantenerla actualizada. | Media | Renzo | Completado |
| HU-05 | Página Principal (Home) | Como usuario, quiero acceder a la pantalla principal después del login para ver y navegar entre secciones. | Alta | Fabrizio | Completado |
| HU-06 | Navegación entre pantallas | Implementar navegación entre Login, Registro, Perfil, Home y Crear Ruta. | Alta | Fabrizio | Completado |

#### 4.2.1.3.Development Evidence for Sprint Review

**Mobile Application**<br>

<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Masagge body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/Aplicaciones-Moviles-Grupo/ChapaTuRuta-MobileApp </td>
    <td align="center"> feature/auth-pages</td>
    <td align="center"> 66487f2afc89c882577b8e92685db43c8efb177d</td>
    <td align="center"> feat: add LoginView UI with email and password fields</td>
    <td align="center"> ---</td>
    <td align="center"> 09/10/2025</td>
  </tr>

  <tr>
    <td align="center">feature/auth-pages</td>
    <td align="center" > b87a5475155f686be3926e95bb0cb78e802e8fcf</td>
    <td align="center"> feat: implement RegisterUserView for account creation</td>
    <td align="center"> ---</td>
    <td align="center"> 09/10/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-pages</td>
    <td align="center">caa18cc86f6e1a8af8a3fc3aa45c040f26fdc65a</td>
    <td align="center"> feat: create RegisterProfileView for user and vehicle information</td>
    <td align="center"> ---</td>
    <td align="center"> 09/10/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-pages</td>
    <td align="center"> 609cb3566f24c9bb12057bcae7fc863a58281c88</td>
    <td align="center"> feat: add app navigation trough auth pages</td>
    <td align="center"> ---</td>
    <td align="center">09/10/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-pages</td>
    <td align="center"> 405689e121163c44e21b4f308a1daf616c1bf4ab</td>
    <td align="center"> chore: add chapaturuta logo in LoginView</td>
    <td align="center"> ---</td>
    <td align="center">09/10/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-pages</td>
    <td align="center"> 5a5f1f78e4740aed4efd928d48964c15f7eab143</td>
    <td align="center">chore: add chapaturuta logo in RegisterProfileView</td>
    <td align="center"> ---</td>
    <td align="center"> 09/10/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-pages</td>
    <td align="center"> 40e3ba253984c2fcffcf2c72d487484cf9285a1a</td>
    <td align="center"> chore: add chapaturuta logo in RegisterUserView</td>
    <td align="center"> ---</td>
    <td align="center"> 09/10/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-pages</td>
    <td align="center"> 6436ec9ab34c796d6771bd2fa2a060e03851acab</td>
    <td align="center"> chore: add chapaturuta logo file</td>
    <td align="center"> ---</td>
    <td align="center"> 09/10/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/home</td>
    <td align="center">17cd59d784361edeb29dc54149b3d7f0d3434613</td>
    <td align="center"> feat(quote): implement methods to update and delete quote orders and services</td>
    <td align="center"> ---</td>
    <td align="center">09/10/2025</td>
  </tr>

  <tr>
      <td align="center"> feature/home</td>
      <td align="center">e0cd5ab7b01728e98e0970074778ae7f8e47b946</td>
      <td align="center"> feat(task): create task service api.</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>

  <tr>
      <td align="center"> feature/home</td>
      <td align="center">4431b8d3813c931938917855a7ce4f101adb07b1</td>
      <td align="center"> feat(task): create task entity..</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
<tr>
      <td align="center"> feature/home</td>
      <td align="center">13effac1e4b0455aa5d1fc57e33157375a2351f3</td>
      <td align="center"> feat(task): create task board entity..</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">e4ae6ad750816498a130df50cad7af0ed1a20c23</td>
      <td align="center"> feat(home): add home composable view</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">9ce54864a86ca661acde64eb4d2cbb0ba621dd2a</td>
      <td align="center"> feat(root): add main composable</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">b6aa1266cd9582cb8544efe6cd29eca8040aaa3c</td>
      <td align="center"> refactor(navigation): move appnav composable to navigation package</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">ea8acfe9ff3274a249c915c826c4aa6dc69e1310</td>
      <td align="center"> feat(ui): add route card composable</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">a978e0a08754ae83eb9d1167ddc04d181deeb4b0</td>
      <td align="center"> feat(ui): add stop card composable</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">c3ae6b7501544e324e03b0e66f6501b08b31aed2</td>
      <td align="center"> feat(ui): add vehicle card composable</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">c98af691595bc30d49a9169765d1bbd21425ca0c</td>
      <td align="center"> feat(home): update home view composable</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">7b024b225417b9dff7f662a6fd78959015f27ff4</td>
      <td align="center"> chore: add drawable images</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/home</td>
      <td align="center">9cf8ec946fb863db03bcd7bf8c6dee0611955ea1</td>
      <td align="center"> feat(navigation): add navigation to main composable</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops_and_routes</td>
      <td align="center">a7b50b5750847b03dd189d45b2111ccebbba8512</td>
      <td align="center"> feat: added Route view</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops_and_routes</td>
      <td align="center">a7b50b5750847b03dd189d45b2111ccebbba8512</td>
      <td align="center"> feat: added Stops view</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops_and_routes</td>
      <td align="center">313c3857d9f07d6c07dfbd0c651790e7e39a3933</td>
      <td align="center"> chore: added a function in components cards</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops_and_routes</td>
      <td align="center">697265af12e3772009451502593de357aa94046e</td>
      <td align="center"> chore: added a function and images</td>
      <td align="center"> ---</td>
      <td align="center">09/10/2025</td>
  </tr>
</table>


**LANDING PAGE**<br>
En el desarrollo de la **Landing Page**, la implementación estuvo a cargo de un único integrante del equipo.  
Por esta razón, el proyecto se trabajó **exclusivamente en su entorno local**, sin requerir colaboración simultánea en línea.  
Esta decisión se tomó por **comodidad y eficiencia**, dado que el alcance del proyecto era reducido y no implicaba la necesidad de integración con otros desarrolladores.

Posteriormente, el proyecto fue desplegado en **GitHub Pages** para su publicación, permitiendo que el resto del equipo y los evaluadores pudieran visualizar la versión final directamente desde la web.

<table><thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Repository&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Branch&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Commit ID&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Commit<br>&nbsp;&nbsp;&nbsp;<br>Message&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Commit<br>&nbsp;&nbsp;&nbsp;<br>Message Body&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Committed on&nbsp;&nbsp;&nbsp;(Date)&nbsp;&nbsp;&nbsp;</th>
  </tr></thead>
<tbody>
  <tr>
<td rowspan="10">
	<h5>Landing Page</h5>
	<a href="https://aplicaciones-moviles-grupo.github.io/landing-page-original" target="_blank" rel="noopener noreferrer">https://aplicaciones-moviles-grupo.github.io/landing-page-original</a>
	<br>
</td>
    <td><br>main</td>
    <td><br>9d66d7fd7ccd87ec117c25cb8dcc7bb561dad065</td>
    <td><br>first commit</td>
    <td><br>first commit</td>
    <td><br>Oct 8, 10:38 PM GMT-5</td>
  </tr>
</tbody></table>

**BACKEND**<br>
<table><thead>
  <tr>
    <th>&nbsp;&nbsp;&nbsp;<br>Repository&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Branch&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Commit ID&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Commit<br>&nbsp;&nbsp;&nbsp;<br>Message&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Commit<br>&nbsp;&nbsp;&nbsp;<br>Message Body&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Committed on&nbsp;&nbsp;&nbsp;(Date)&nbsp;&nbsp;&nbsp;</th>
  </tr></thead>
<tbody>
  <tr>
    <td rowspan="10">
	    <h5>back-end</h5>
	      <a href="https://github.com/Aplicaciones-Moviles-Grupo/back-end" target="_blank" rel="noopener noreferrer">https://github.com/Aplicaciones-Moviles-Grupo/back-end</a>
	      <br>
    </td>
    <td><br>main</td>
    <td><br>fc929b77270f95aba6a35387a96a7503c3523529</td>
    <td><br>first commit</td>
    <td><br>first commit</td>
    <td><br>Oct 6, 2025</td>
  </tr>
 <tr>
   <td><br>main</td>
    <td><br>cf7d59caa7536a1f3aa87852fa8ef0b899349d49</td>
    <td><br>feature: update database connection settings for production environment</td>
    <td><br>feature: update database connection settings for production environment</td>
    <td><br>Oct 8, 2025</td>
  </tr>
</tbody></table>

#### 4.2.1.4.Testing Suite Evidence for Sprint Review

Se realizaron pruebas manuales de navegación entre pantallas utilizando el **emulador de Android Studio**, verificando que:
- Las rutas definidas en `AppNavHost` funcionen correctamente.  
- La navegación de **Login → Register → Profile → Home** se ejecute sin errores.  
- Los datos ingresados en los formularios de registro y edición se mantengan estables durante la sesión.

---

#### 4.2.1.5.Execution Evidence for Sprint Review

Durante este primer Sprint logramos realizar la implementación del Landing page, Backend y Mobile App, sin embargo este último por el momento se realizó de forma local.

A continuación se presentan evidencias de ejecución de los 3 productos:


**Landing Page**

**Hero Section**: En esta sección se colocó un mensaje que atraiga la atención del visitante, junto con un boton call to action para posteriormente enviarlo a la aplicación movil desplegada. 

<img src="resources/chapter-4/Hero%20Section.png" height=400>

**How It Works Section**: En esta sección se le presenta como funciona la app para que el usuario obtenga información sobre las rutas y paraderos de los colectivos 

<img src="resources/chapter-4/How-it-Work.png" height=400>

**Advantages Section**: Se presentan los beneficios que ofrece la aplicación para facilitar la búsqueda de colectivos

<img src="resources/chapter-4/Advantages%20Section.png" height=400>

**FAQ Section**: Se muestran las preguntas frecuentes que realizan los visitantes cuando visitan por primera vez la página

<img src="resources/chapter-4/FAQ%20Section.png" height=400>

**Footer Section**: Finalmente en el footer se presenta información de contacto como redes sociales, numero de telefono, etc.

<img src="resources/chapter-4/Footer%20Section.png" height=400>


**Backend**

<img src="resources/chapter-4/Backend-Execution-1.png" height=400>

<img src="resources/chapter-4/Backend-Execution-2.png" height=400>

<img src="resources/chapter-4/Backend-Execution-3.png" height=400>

<img src="resources/chapter-4/Backend-Execution-4.png" height=400>

<img src="resources/chapter-4/Backend-Execution-5.png" height=400>

**Mobile App**

<img src="resources/chapter-4/Mobile-App-Execution-1.png" height=400>

<img src="resources/chapter-4/Mobile-App-Execution-2.png" height=400>

<img src="resources/chapter-4/Mobile-App-Execution-3.png" height=400>

<img src="resources/chapter-4/Mobile-App-Execution-4.png" height=400>



#### 4.2.1.6.Services Documentation Evidence for Sprint Review

Tras finalizar el Sprint 1, hemos logrado implementar los endpoints principales de nuestra API backend, estableciendo una base sólida para la comunicación entre el frontend y la base de datos. Durante este sprint nos enfocamos en desarrollar la funcionalidad core del sistema, implementando los bounded contexts de Stops, Companies y Geographic con sus respectivos controladores y servicios. A continuación, presentamos la evidencia de los avances alcanzados durante este período de desarrollo.

*Companies* : Este bounded context maneja la información de las compañías o empresas de transporte. Proporciona funcionalidades para registrar nuevas empresas, consultar su información, actualizarla y eliminarla. También permite verificar qué compañía está asociada a un usuario específico, siendo esencial para el control de acceso y la gestión empresarial del sistema.

![login](./assets/SCompany.PNG)

*Geographic*: Este bounded context administra la información geográfica y territorial del sistema. Maneja una jerarquía de ubicaciones que incluye regiones, provincias, distritos y localidades. Permite consultar la información geográfica a diferentes niveles y establecer relaciones entre las divisiones territoriales, proporcionando el contexto geográfico necesario para ubicar paradas y rutas de transporte.

![inicio](./assets/SGeo.PNG)

*Stops*: Este bounded context se encarga de administrar las paradas o estaciones de transporte público. Permite crear, consultar, actualizar y eliminar paradas, así como buscarlas por diferentes criterios como compañía, localidad o nombre. Es fundamental para el sistema de rutas y ubicaciones del transporte.

![paraderos](./assets/SStop.PNG)


#### 4.2.1.7.Software Deployment Evidence for Sprint Review

**Evidencias del despliegue de la Landing Page**

A continuación, se presentan las evidencias del **despliegue de la Landing Page**, desarrollada con **Vue 3**, **Vite** y **JavaScript**.  
El proyecto fue construido aplicando componentes dinámicos y estilos personalizados, y posteriormente publicado mediante la funcionalidad de **GitHub Pages**, la cual permite alojar sitios web estáticos directamente desde un repositorio.

Durante el proceso se generó la carpeta `dist/` con los archivos optimizados para producción, y se configuró el despliegue automático hacia la rama `gh-pages`.  
De esta manera, la página quedó disponible públicamente, mostrando la integración entre **Vue**, **Vite** y las configuraciones de despliegue en **GitHub Pages**.

**url:** <a href="https://aplicaciones-moviles-grupo.github.io/landing-page-original">https://aplicaciones-moviles-grupo.github.io/landing-page-original</a>


![img_4.png](img_4.png)
**Como trabajamos**<br>
![img_5.png](img_5.png)
![img_6.png](img_6.png)
![img_7.png](img_7.png)

**Evidencias del despliegue del Back End**<br>
**Despliegue del Web Service**

Para el **despliegue del Web Service**, se utilizó la plataforma **Railway**, la cual se integró directamente con el repositorio de **GitHub**.  
Esta conexión permitió automatizar el proceso de despliegue, de modo que cada cambio o actualización en el código del repositorio se reflejara automáticamente en el entorno en línea.

Railway ofrece una configuración sencilla y flexible, ideal para proyectos con backend ligero o servicios web basados en APIs.  
A través de su panel, se vinculó el repositorio del proyecto, se configuraron las variables de entorno necesarias y se ejecutó el despliegue con un solo clic, sin necesidad de herramientas externas o autenticaciones adicionales desde el IDE.

![img_8.png](img_8.png)

**Actualización del despliegue en Railway**

En la imagen se muestra el panel de control de **Railway**, donde se registran los cambios aplicados al proyecto del **Web Service**.  
El sistema indica que se realizaron **dos actualizaciones** relacionadas con la configuración del entorno de despliegue:

- **Branch:**  
  Se confirma que la rama activa para el despliegue es `main`, lo que significa que Railway tomará automáticamente el código más reciente de esta rama cada vez que se realice un nuevo commit o push en GitHub.

- **Repo:**  
  Se muestra el repositorio vinculado al servicio, en este caso **`Aplicaciones-Moviles-Grupo/back-end`**, el cual contiene el código fuente del backend.

El mensaje **“back-end was updated”** confirma que Railway detectó cambios en el repositorio y actualizó el entorno de producción de forma automática.  
Esta funcionalidad garantiza una **integración continua** entre GitHub y Railway, permitiendo que cada modificación validada en la rama principal se despliegue sin intervención manual adicional. 
![img_9.png](img_9.png)

**Evidencia de despliegue en Railway**

La imagen muestra el entorno de **producción** en **Railway**, donde el **backend** fue desplegado correctamente.

- **Estado:** El mensaje *“Deployment successful”* confirma que el despliegue se realizó sin errores.
- **Origen:** El código se obtuvo automáticamente desde la rama `main` del repositorio **`Aplicaciones-Moviles-Grupo/back-end`**, mediante integración con **GitHub**.
- **Configuración:** El servicio usa un **Dockerfile** para su construcción y ejecuta el comando `./Frock-backend` al iniciar.

Con esto se valida que el **Web Service** se encuentra activo y funcionando en producción con un flujo automatizado de despliegue continuo.
![img_10.png](img_10.png)

**Despliegue del Web Service en Railway**

finalmente, se muestra la URL pública generada por **Railway** para acceder al **Web Service** desplegado.
![img_11.png](img_11.png)

#### 4.2.1.8.Team Collaboration Insights during Sprint
El equipo mantuvo reuniones periódicas mediante **Discord** y **Meet** para coordinar tareas y compartir avances.  
La colaboración fue efectiva al dividir las vistas según especialidad y mantener coherencia visual con el tema `AppTheme`.

Se destaca la integración exitosa del flujo completo de navegación móvil y la consolidación de la identidad visual de la aplicación.

---

**Resumen del Sprint 1:**
- Se implementaron las vistas principales del aplicativo móvil.
- Se estableció el flujo completo de navegación.
- Se hizo el despliegue de la landing page
- Se alcanzó el 100% de las metas planificadas para el sprint.

### 4.2.2.Sprint 2

Durante este Sprint nos enfocamos en desarrollar toda la aplicación en Android Studio, usando Kotlin con JetPackCompose.

#### 4.2.2.1.Sprint Planning 2

|            Sprint #            |                                                                                                                                                                             Sprint 2                                                                                                                                                                             |
|:------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| **Sprint Planning Background** |                                                                                                                                                                                                                                                                                                                                                                  |
|              Date              |                                                                                                                                                                             03/11/25                                                                                                                                                                             |
|              Time              |                                                                                                                                                                           19:00 horas                                                                                                                                                                            |
|            Location            |                                                                                                                                                                         Reunión Virtual                                                                                                                                                                          |
|          Prepared By           |                                                                                                                                                                 Fabrizio Alexander Cutiri Agüero                                                                                                                                                                 |
|           Attendees            |                                                                                                                               - Yasser Renteria Palacios   <br> - Renzo José Araujo Ingunza  <br> - Adrian Emanuel Valerio Garcia                                                                                                                                |
|    Sprint 1 Review Summary     |                                                                                Durante el sprint 1 se realizó el despliegue del landing page, backend y se desarrollo las pantallas de la aplicación movil en Android Studio. Además se implementó la navegación entre pantallas.                                                                                |
| Sprint 1 Retrospective Summary |                               En el sprint 1 se visualizó oportunidades de mejora para el backend, de tal forma que guarde relación con las pantallas presentadas en la aplicación. Además de mejorar el diseño de las pantallas de la aplicación donde se presentan el uso de GoogleMaps, para que estos ocupen toda la pantalla.                               |
| **Sprint Goal & User Stories** |                                                                                                                                                                                                                                                                                                                                                                  |
|         Sprint 2 Goal          | Nuestro objetivo en este Sprint 2 es mejorar el backend presentado anteriormente. Además mejorar el uso de los Mapas de Google Maps en las pantallas de Rutas y Paraderos. Por último, completar el desarrollo total de la aplicación de Android Studio, implementando los servicios externos de GoogleMaps, tales como MapsSDK, Geocoding API y Directions API. |
|       Sprint 2 Velocity        |                                                                                                                                                                    Velocidad de 85 - Sprint 2                                                                                                                                                                    |
|      Sum of Story Points       |                                                                                                                                                                    Sprint 2 - 79 Story Points                                                                                                                                                                    |


#### 4.2.2.2.Sprint Backlog 2

| Sprint # | Sprint 2 |
|----------|----------|

| User Story |  | Work Item / Task |  |  | Estimation (Hours) | Assigned To | Status (To-do / In-Process / To-Review / Done) |
|------------|----------|------------------|----------|-------------|-------------------|-------------|------------------------------------------------|
| **Id** | **Title** | **Id** | **Title** | **Description** | | | |
| SS01 | Integración de Google Maps | T01 | Configurar Google Maps API | Integrar la API de Google Maps en el proyecto y configurar las credenciales necesarias | 4 | Fabrizio Cutiri | Done |
| SS01 | Integración de Google Maps | T02 | Implementar mapa interactivo | Desarrollar el componente de mapa con funcionalidades de zoom, pan y marcadores | 4 | Fabrizio Cutiri | Done |
| US08 | Buscar rutas disponibles | T03 | Diseñar interfaz de búsqueda | Crear el formulario de búsqueda con filtros de origen, destino y horario | 3 | Fabrizio Cutiri | Done |
| US08 | Buscar rutas disponibles | T04 | Implementar lógica de búsqueda | Desarrollar el algoritmo de búsqueda y conexión con el backend | 5 | Fabrizio Cutiri | Done |
| US09 | Activar disponibilidad de ruta | T05 | Crear toggle de disponibilidad | Implementar el control para activar/desactivar disponibilidad de ruta | 3 | Fabrizio Cutiri | Done |
| US09 | Activar disponibilidad de ruta | T06 | Gestionar estados de ruta | Desarrollar la lógica para actualizar el estado de disponibilidad en tiempo real | 5 | Fabrizio Cutiri | Done |
| US10 | Gestión de Rutas | T07 | Crear módulo CRUD de rutas | Implementar las operaciones de crear, leer, actualizar y eliminar rutas | 5 | Fabrizio Cutiri | Done |
| US10 | Gestión de Rutas | T08 | Validar datos de rutas | Desarrollar validaciones para los campos de rutas | 3 | Adrián Valerio | Done |
| US11 | Ver detalles completos de una ruta | T09 | Diseñar vista de detalle | Crear la interfaz para mostrar toda la información de una ruta | 4 | Fabrizio Cutiri | Done |
| US11 | Ver detalles completos de una ruta | T10 | Integrar datos de ruta | Conectar la vista con los endpoints para obtener información completa | 4 | Yasser Rentería | Done |
| US13 | Ver paraderos en el mapa | T11 | Mostrar marcadores de paraderos | Implementar marcadores en el mapa para cada paradero | 4 | Fabrizio Cutiri | Done |
| US13 | Ver paraderos en el mapa | T12 | Agregar información de paraderos | Crear popups informativos al hacer clic en los marcadores | 4 | Fabrizio Cutiri | Done |
| US14 | Gestión de paraderos | T13 | Crear módulo CRUD de paraderos | Implementar operaciones para gestionar paraderos | 5 | Fabrizio Cutiri | Done |
| US14 | Gestión de paraderos | T14 | Validar ubicaciones de paraderos | Desarrollar validaciones geográficas para paraderos | 3 | Adrián Valerio | Done |
| US15 | Ver paraderos en la página de inicio | T15 | Diseñar sección de paraderos | Crear el componente de paraderos para la página principal | 3 | Fabrizio Cutiri | Done |
| US15 | Ver paraderos en la página de inicio | T16 | Cargar paraderos destacados | Implementar lógica para mostrar paraderos más relevantes | 2 | Yasser Rentería | Done |
| US01 | Navegación Sencilla | T17 | Diseñar menú de navegación | Crear estructura de navegación intuitiva y responsiva | 2 | Renzo Araujo | Done |
| US01 | Navegación Sencilla | T18 | Implementar rutas de navegación | Desarrollar sistema de routing entre vistas principales | 3 | Adrián Valerio | Done |
| US05 | Postular como colaborador | T25 | Diseñar formulario de postulación | Crear interfaz para registro de colaboradores | 3 | Fabrizio Cutiri | Done |
| US05 | Postular como colaborador | T26 | Implementar envío de postulación | Desarrollar lógica de envío y validación de formulario | 2 | Renzo Araujo | Done |
| US06 | Video about the product | T27 | Integrar reproductor de video | Implementar componente de video embebido del producto | 2 | Adrián Valerio | Done |
| US06 | Video about the product | T28 | Optimizar carga de video | Configurar lazy loading y optimización de recursos | 3 |Fabrizio Cutiri  | Done |
| US07 | Video About the team | T29 | Integrar video del equipo | Implementar sección de video sobre el equipo | 3 | Fabrizio Cutiri | Done |
| US07 | Video About the team | T30 | Diseñar presentación del equipo | Crear layout para mostrar miembros del equipo | 2 | Fabrizio Cutiri  | Done |
| US17 | Crear Perfil | T31 | Diseñar formulario de perfil | Crear interfaz de registro de perfil de usuario | 2 | Yasser Rentería | Done |
| US17 | Crear Perfil | T32 | Implementar validaciones de perfil | Desarrollar validaciones para campos del perfil | 1 | Yasser Rentería | Done |
| US18 | Editar Perfil | T33 | Crear vista de edición | Implementar interfaz para modificar datos del perfil | 2 | Yasser Rentería | Done |
| US18 | Editar Perfil | T34 | Actualizar datos de perfil | Desarrollar lógica de actualización y persistencia | 1 | Yasser Rentería | Done |
| US19 | Ver información del conductor | T35 | Diseñar vista de conductor | Crear interfaz para mostrar datos del conductor | 2 | Yasser Rentería | Done |
| US19 | Ver información del conductor | T36 | Obtener información del conductor | Integrar endpoint para consultar datos del conductor | 1 | Yasser Rentería | Done |
| US21 | Iniciar Sesión | T37 | Diseñar formulario de login | Crear interfaz de inicio de sesión | 2 | Fabrizio Cutiri | Done |
| US21 | Iniciar Sesión | T38 | Implementar autenticación | Desarrollar lógica de autenticación con JWT | 1 | Fabrizio Cutiri | Done |
| US22 | Cerrar Sesión | T39 | Implementar logout | Desarrollar funcionalidad para cerrar sesión y limpiar tokens | 2 | Fabrizio Cutiri | Done |
| US22 | Cerrar Sesión | T40 | Validar cierre de sesión | Asegurar que se limpien correctamente las sesiones | 1 | Fabrizio Cutiri | Done |
| US23 | Registrar Usuario | T41 | Diseñar formulario de registro | Crear interfaz de registro de nuevos usuarios | 2 | Fabrizio Cutiri | Done |
| US23 | Registrar Usuario | T42 | Implementar registro | Desarrollar lógica de creación de usuarios | 1 | Fabrizio Cutiri | Done |

#### 4.2.2.3.Development Evidence for Sprint Review

**Mobile Application**<br>

<table>
  <tr>
    <td align ="center" > <strong>Repository</strong></td>
    <td  align ="center" > <strong>Branch</strong></td>
    <td  align ="center" > <strong>Commit ID</strong></td>
    <td  align ="center" > <strong>Commit message</strong></td>
    <td  align ="center" > <strong>Commit Masagge body</strong></td>
    <td  align ="center" > <strong>Commit on (date)</strong></td>
  </tr>

  <tr>
    <td rowspan="27" align="center"> https://github.com/Aplicaciones-Moviles-Grupo/ChapaTuRuta-MobileApp </td>
    <td align="center"> feature/auth-functional</td>
    <td align="center"> cf5a17e27a8436632e7924372248c13ac6a9cc4a</td>
    <td align="center"> feat(auth): implements data store and interceptor for token</td>
    <td align="center"> ---</td>
    <td align="center"> 08/11/2025</td>
  </tr>

  <tr>
    <td align="center">feature/auth-functional</td>
    <td align="center" > 78e8e976905c11c332e5f717cd8192d984de4b27</td>
    <td align="center"> feat(auth): add sign in, sign up and user dto</td>
    <td align="center"> ---</td>
    <td align="center"> 08/11/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-functional</td>
    <td align="center">1f9d96d1244123eb6f5b25833b1040261076cdfd</td>
    <td align="center"> feat(auth): add remote and repository modules</td>
    <td align="center"> ---</td>
    <td align="center"> 08/11/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-functional</td>
    <td align="center"> a82c99d594970ee87e53186250a6054733592540</td>
    <td align="center"> feat(auth): add auth service and repository</td>
    <td align="center"> ---</td>
    <td align="center">08/11/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-functional</td>
    <td align="center"> 789b0952f6e61e23628d1780013ae2e4fc33f286</td>
    <td align="center"> feat(auth): add login view presentation</td>
    <td align="center"> ---</td>
    <td align="center">08/11/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-functional</td>
    <td align="center"> 4344eb9a8fdd367587f5fa71ad45d086ae19a610</td>
    <td align="center">feat(auth): update register user and profile presentation views</td>
    <td align="center"> ---</td>
    <td align="center"> 08/11/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-functional</td>
    <td align="center"> e6519a751abc29bca63b8e3f4132bc8454459bc9</td>
    <td align="center"> feat(auth): add my application hilt android app</td>
    <td align="center"> ---</td>
    <td align="center"> 08/11/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/auth-functional</td>
    <td align="center"> dab781e6ae3e87e8c64aae25a5c5fad616eb7989</td>
    <td align="center"> feat(manifest): add permissions into manifest</td>
    <td align="center"> ---</td>
    <td align="center"> 08/11/2025</td>
  </tr>

  <tr>
    <td align="center"> feature/profile-functional</td>
    <td align="center">a345bda1a32895bcac49d1aa46a256f01bbce1c8</td>
    <td align="center"> feat(profile): add profile repository and service</td>
    <td align="center"> ---</td>
    <td align="center">10/11/2025</td>
  </tr>

  <tr>
      <td align="center"> feature/profile-functional</td>
      <td align="center">092a1237c7eb7ee4d32fa2e17a5850455a6bae0b</td>
      <td align="center"> feat(profile): implement profile viewmodel</td>
      <td align="center"> ---</td>
      <td align="center">10/11/2025</td>
  </tr>

  <tr>
      <td align="center"> feature/profile-functional</td>
      <td align="center">8ab1ad2f01a0d8a0f47ee0b247e4ac70b1a1e541</td>
      <td align="center"> feat(profile): add vehicle dto, model and ui state</td>
      <td align="center"> ---</td>
      <td align="center">10/11/2025</td>
  </tr>
<tr>
      <td align="center"> feature/profile-functional</td>
      <td align="center">268742b9fd0cf23c3c4e9cffdc0bffc6072faa9a</td>
      <td align="center"> feat(profile): add profile to remote and repository modules</td>
      <td align="center"> ---</td>
      <td align="center">10/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/profile-functional</td>
      <td align="center">57800996ffea22b12eff14a2b3d6e9aea602f4f1</td>
      <td align="center"> feat(profile): add views for profile and vehicle</td>
      <td align="center"> ---</td>
      <td align="center">10/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/profile-functional</td>
      <td align="center">a8360e5096091a2c14abb3de1d88431199dc1bbb</td>
      <td align="center"> feat(profile):feat(profile): add navigation for profile context</td>
      <td align="center"> ---</td>
      <td align="center">10/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops-functional</td>
      <td align="center">07210aecfedaec3a3f885b2dc5a38cd27f72c2fe</td>
      <td align="center"> feat(stops): add google maps implementation</td>
      <td align="center"> ---</td>
      <td align="center">11/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops-functional</td>
      <td align="center">5b2a915aae400d7ecbad5ccdcda1604a0b925b2e</td>
      <td align="center"> feat(geocoding): add geocoding external service</td>
      <td align="center"> ---</td>
      <td align="center">11/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops-functional</td>
      <td align="center">5b4850e71183e8e9c69e77724919024d83a0971e</td>
      <td align="center"> feat(logo): add logo chapa tu ruta</td>
      <td align="center"> ---</td>
      <td align="center">11/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops-functional</td>
      <td align="center">f6f8ec2f0a976daa02b3a3eadca207fbad510dde</td>
      <td align="center"> feat(stops): add stop repository and service in modules</td>
      <td align="center"> ---</td>
      <td align="center">11/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops-functional</td>
      <td align="center">c6bf532245c9229c5b54dd0dd989706681b24a18</td>
      <td align="center"> feat(stops): add stop viewmodel</td>
      <td align="center"> ---</td>
      <td align="center">11/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/stops-functional</td>
      <td align="center">a888524e69a72e201e6c8db7affd03778645488f</td>
      <td align="center"> feat(stops): add stop context to navigation</td>
      <td align="center"> ---</td>
      <td align="center">11/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/routes-functional</td>
      <td align="center">7bf26a893f425c3339422dc9a1b6e743dc13ca2a</td>
      <td align="center"> feat(routes): add google maps utils implementation</td>
      <td align="center"> ---</td>
      <td align="center">12/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/routes-functional</td>
      <td align="center">bc9608338c835937204300a0382c7150d4833096</td>
      <td align="center"> feat(routes): add directions api external service</td>
      <td align="center"> ---</td>
      <td align="center">12/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/routes-functional</td>
      <td align="center">a20aaa0dae3c5696ca86f3e54fec4ab123ef4ca9</td>
      <td align="center"> feat(routes): add route service and repository</td>
      <td align="center"> ---</td>
      <td align="center">12/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/routes-functional</td>
      <td align="center">1c9385635e03ea29cb7dcf088b63103724af7af4</td>
      <td align="center"> feat(routes): implements route service and repository into modules</td>
      <td align="center"> ---</td>
      <td align="center">12/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/routes-functional</td>
      <td align="center">b053401d28b39734cc810fd2204cfc73a42e9097</td>
      <td align="center"> feat(routes): add route models and viewmodel</td>
      <td align="center"> ---</td>
      <td align="center">12/11/2025</td>
  </tr>
  <tr>
      <td align="center"> feature/routes-functional</td>
      <td align="center">2fc85011fcaea9f644f82e54c70a5873586a1d4f</td>
      <td align="center"> feat(routes): add navigation for route context</td>
      <td align="center"> ---</td>
      <td align="center">12/11/2025</td>
  </tr>
</table>

#### 4.2.2.4.Testing Suite Evidence for Sprint Review

<img width="1851" height="949" alt="image" src="https://github.com/user-attachments/assets/b99dbdae-c023-4250-81e2-a0c1214082e6" />

[https://github.com/Aplicaciones-Moviles-Grupo/Acceptance-Criteria] 


#### 4.2.2.5.Execution Evidence for Sprint Review

Para este sprint 2 se ha desarrollado todo el app movil en Android Studio, usando Kotlin y JetpackCompose. Además, se realizaron algunos cambios al backend.

**Video de Ejecución:** [https://shorturl.at/G1rir](https://shorturl.at/G1rir)

**Mobile Application - Kotlin & Jetpack Compose**


**Login**
<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/login-view.png" alt="" height="500">
  <img src="resources/chapter-4/execution-evidence-sprint-2/home-view.png" alt="" height="500">
</p>

**Stops**

<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/stops-view.png" alt="" height="500">
  <img src="resources/chapter-4/execution-evidence-sprint-2/create-stop-1.png" alt="" height="500">
</p>
<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/create-stop-2.png" alt="" height="500">
  <img src="resources/chapter-4/execution-evidence-sprint-2/create-stop-3.png" alt="" height="500">
</p>

**Routes**

<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/routes-view.png" alt="" height="500">
  <img src="resources/chapter-4/execution-evidence-sprint-2/routes-view-2.png" alt="" height="500">
</p>
<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/create-route-1.png" alt="" height="500">
  <img src="resources/chapter-4/execution-evidence-sprint-2/create-route-2.png" alt="" height="500">
</p>

<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/create-route-3.png" alt="" height="500">
  <img src="resources/chapter-4/execution-evidence-sprint-2/create-route-4.png" alt="" height="500">
</p>

**Profiles**

<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/profile-view.png" alt="" height="500">
  <img src="resources/chapter-4/execution-evidence-sprint-2/edit-profile-1.png" alt="" height="500">
</p>
<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/edit-profile-2.png" alt="" height="500">
  <img src="resources/chapter-4/execution-evidence-sprint-2/edit-profile-3.png" alt="" height="500">
</p>
<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/edit-profile-4.png" alt="" height="500">
</p>
<br>
<br>

**Backend**

<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/backend-execution-1.png" alt="" height="600">
</p>
<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/backend-execution-2.png" alt="" height="500">
</p>
<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/backend-execution-3.png" alt="" height="500">
</p>
<p align="center">
  <img src="resources/chapter-4/execution-evidence-sprint-2/backend-execution-4.png" alt="" height="350">
</p>

Continuando con el Sprint 2, se desarrolló una aplicación móvil utilizando Flutter y Dart, enfocada en los viajeros y en la visualización de rutas de transporte y sus paradas.

**Card list**
<p align="center">
  <img src="assets/flutter_card_list.png" alt="" height="550">
</p>

**Profile**

<p align="center">
  <img src="assets/flutter_profile.png" alt="" height="550">
</p>

**Stops detail**

<p align="center">
  <img src="assets/flutter_detail.png" alt="" height="550">
</p>
<p align="center">
  <img src="assets/flutter_detail2.png" alt="" height="550">
</p>

**Favorites**
<p align="center">
  <img src="assets/flutter_favorites.png" alt="" height="550">
</p>

#### 4.2.2.6.Services Documentation Evidence for Sprint Review

En esta sección del informe se presentan todos los endpoints desarrollados en el backend, detallando que funcion realizan cada uno.

Link del backend desplegado: [https://chapaturutabackend.onrender.com/swagger/index.html](https://chapaturutabackend.onrender.com/swagger/index.html)

<table> 
  <tr>
    <td> <strong>Action </strong></td>
    <td> <strong>End Point </strong></td>
    <td align="center"> <strong>Funciones</strong> </td>
  </tr>

  <tr>
    <td> POST</td>
    <td> /api/v1/auth/sign-in</td>
    <td> Permite iniciar sesión al usuario y genera el token</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/auth/sign-up</td>
    <td> Permite registrar a un usuario</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/users/{userId}/profile</td>
    <td> Obtiene el perfil asociado a un usuario</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/users/{id}</td>
    <td> Obtiene un usuario por su Id</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/drivers/{driverId}/routes</td>
    <td> Obtiene la lista de rutas asociadas a un perfil de conductor</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/drivers/{profileId}/vehicle/{id}</td>
    <td> Obtiene el vehiculo de un conductor mediante su Id</td>
  </tr>
  <tr>
    <td> PUT</td>
    <td> /api/v1/drivers/{profileId}/vehicle/{id}</td>
    <td> Actualiza el vehiculo de un conductor mediante su Id</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/drivers/{profileId}/vehicle</td>
    <td> Obtiene el vehiculo de un conductor mediante el Id del perfil</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/drivers/{profileId}/vehicle</td>
    <td> Crea el vehículo de un conductor mediante su profileId</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/profiles/{id}</td>
    <td> Obtiene el perfil por su Id</td>
  </tr>
  <tr>
    <td> PUT</td>
    <td> /api/v1/profiles/{id}</td>
    <td> Actualiza el perfil mediante su Id</td>
  </tr>

  <tr>
    <td> POST</td>
    <td> /api/v1/profiles</td>
    <td> Crea un nuevo perfil</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /drivers</td>
    <td> Obtiene el perfil de todos los conductores registrados</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/routes/{id}</td>
    <td> Obtener una ruta por su Id</td>
  </tr>
  <tr>
    <td> DELETE</td>
    <td> /api/v1/routes/{id}</td>
    <td> Elimina una ruta por su Id</td>
  </tr>  
  <tr>
    <td> POST</td>
    <td> /api/v1/routes</td>
    <td> Crea una ruta</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/routes/{routeId}/active</td>
    <td> Actualiza el estado de una ruta a "Active"</td>
  </tr>  
  <tr>
    <td> POST</td>
    <td> /api/v1/routes/{routeId}/inactive</td>
    <td> Actualiza el estado de una ruta a "Inactive"</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/routes/{routeId}/stops/{id}</td>
    <td> Obtiene un paradero de una ruta por su Id</td>
  </tr>  
  <tr>
    <td> DELETE</td>
    <td> /api/v1/routes/{routeId}/stops/{id}</td>
    <td> Elimina un paradero de una ruta mediante su Id</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/routes/{routeId}/stops</td>
    <td> Obtiene todos los paraderos asociados a una ruta</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/routes/{routeId}/stops</td>
    <td> Crea un paradero de una ruta</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/stops/{id}</td>
    <td> Obtiene un paradero por su Id</td>
  </tr>
  <tr>
    <td> PUT</td>
    <td> /api/v1/stops/{id}</td>
    <td> Actualiza un paradero por su Id</td>
  </tr>
  <tr>
    <td> DELETE</td>
    <td> /api/v1/stops/{id}</td>
    <td> Elimina un paradero por su Id</td>
  </tr>
  <tr>
    <td> GET</td>
    <td> /api/v1/stops?driverId</td>
    <td> Obtiene los paraderos asociados al perfil de un conductor</td>
  </tr>
  <tr>
    <td> POST</td>
    <td> /api/v1/stops</td>
    <td> Crea un paradero</td>
  </tr>
</table>

#### 4.2.2.7.Software Deployment Evidence for Sprint Review

Para realizar el despliegue de la aplicación movil, usamos Firebase Console, la opción de App Distribution. A continuación se detalla el proceso que se siguió para realizar el despliegue.

**Mobile Application - Kotlin & JetPack Compose**

Primero se creo un nuevo proyecto en Firebase Console.

<img src="resources/chapter-4/deployment-evidence-sprint-2/depliegue-movil.png" alt="" height="450">

<img src="resources/chapter-4/deployment-evidence-sprint-2/depliegue-movil-2.png" alt="" height="450">

Una vez creado el proyecto nos dirigimos a "App Distribution" y seleccionamos la opción de android para nuestra aplicación

<img src="resources/chapter-4/deployment-evidence-sprint-2/depliegue-movil-3.png" alt="" height="450">

<img src="resources/chapter-4/deployment-evidence-sprint-2/depliegue-movil-4.png" alt="" height="450">

Cuando seleccionamos que nuestra aplicación es android nos piden colocar el nombre del paquete de nuestro proyecto (com.frock.chapaturuta) 

<img src="resources/chapter-4/deployment-evidence-sprint-2/depliegue-movil-5.png" alt="" height="450">

Una vez finalizado la configuración del proyecto, solo se sube el APK del proyecto y posteriormente se agrega verificadores para que prueben la aplicación.

<img src="resources/chapter-4/deployment-evidence-sprint-2/depliegue-movil-6.png" alt="" height="450">

<img src="resources/chapter-4/deployment-evidence-sprint-2/depliegue-movil-7.png" alt="" height="450">


**Backend**

 En lo que respecta al backend, se realizo el despliegue en Render y para la base de datos se utilizó el servicio de Railway.

<img src="resources/chapter-4/deployment-evidence-sprint-2/deployment-backend-render.png" alt="" height="450">

<img src="resources/chapter-4/deployment-evidence-sprint-2/database-railway.png" alt="" height="450">


#### 4.2.2.8.Team Collaboration Insights during Sprint

**Pulse**

<img src="resources/chapter-4/sprint-2/insights-pulse.png" alt="" height="400">

<img src="assets/flutter_pulse.png" alt="" height="600">
<br>

**Contributors**

<img src="resources/chapter-4/sprint-2/insights-contributors.png" alt="" height="400">

<img src="assets/flutter_contributors.png" alt="" height="600">

**Network**

<img src="resources/chapter-4/sprint-2/insights-network.png" alt="" height="400">

<img src="assets/flutter_network.png" alt="" height="600">

### 4.2.3. Sprint 3

#### 4.2.3.1. Sprint Planning 3

#### 4.2.3.2. Sprint Backlog 3

#### 4.2.3.3. Development Evidence for Sprint Review

#### 4.2.3.4. Testing Suite Evidence for Sprint Review

#### 4.2.3.5. Execution Evidence for Sprint Review

#### 4.2.3.6. Services Documentation Evidence for Sprint Review

#### 4.2.3.7. Software Deployment Evidence for Sprint Review

#### 4.2.3.8. Team Collaboration Insights during Sprint

## 4.3. Validation Interviews

### 4.3.1. Diseño de Entrevistas

**Preguntas Generales**

* ¿Cuál es su nombre?

* ¿Cuántos años tiene?

* ¿Cuál es su profesión?

* ¿En qué ciudad vive?

**Preguntas sobre la aplicación - Conductores de Colectivo**

* Después de ver las funcionalidades de la aplicación, ¿qué impresión general le genera?

* ¿Cree que una herramienta así podría ayudarle en su servicio diario? ¿Por qué?

* ¿Qué funcionalidad le parece más útil para su trabajo?

* ¿Considera que esta aplicación facilitaría a los usuarios conocer la información de los colectivos? ¿De qué manera?

* ¿Qué tan importante es para usted poder compartir la ruta y el precio de manera clara al cliente?

* ¿Le sería útil visualizar la ruta en un mapa antes de iniciarla?

* ¿Cree que los usuarios confiarían más en un servicio que muestre rutas y datos organizados en una aplicación?

### 4.3.2. Registro de Entrevistas

**Segmento Objetivo:** Conductores de colectivo

#### Entrevistado N° 1

![validation-interview-1.png](resources/chapter-4/validation-interview-1.png)

- **Nombre:** Luis Cutiri
- **Edad:** 55 años
- **Ciudad:** Lima
- **Duración:** 00:12:40
- **Enlace de la Entrevista:** [https://shorturl.at/XCrKp](https://shorturl.at/XCrKp)

- Resumen de la entrevista: <br><br> La entrevista se realizó a Luis Cutiri, un conductor de colectivo con 55 años. Durante la entrevista se presentaron al conductor las funcionalidades principales de la aplicación móvil. El entrevistado mencionó que la herramienta le sería de gran utilidad para el servicio de transporte colectivo que realiza, ya que considera que le permitiría captar a más clientes al poder compartir información clara sobre el precio y la ruta que ofrece. Explicó que, en su experiencia, muchos usuarios desconocen las rutas exactas de los colectivos, por lo que disponer de una aplicación que muestre esta información de manera accesible podría mejorar significativamente la visibilidad de su servicio. <br><br> Asimismo, el entrevistado destacó que la aplicación no solo beneficiaría a los conductores, sino también a los clientes. Según él, permitir que los usuarios visualicen previamente las rutas les facilitaría planificar sus viajes, evitar confusiones respecto a los puntos de partida y llegada, y tener mayor seguridad al conocer el trayecto antes de abordar. Consideró también que esta transparencia podría generar mayor confianza en el servicio y diferenciar a los conductores que utilicen la herramienta frente a quienes no lo hagan.

### 4.3.3. Evaluaciones según heurísticas

<p style="text-align: center; font-weight: bold"> UX Heuristics & Principles Evaluation </p>
<p style="text-align: center; font-weight: bold">Usability - Inclusive Design - Information Architecture</p>

**CARRERA :** Ingeniería de Software

**CURSO :** 1ACC0238 - Aplicaciones para Dispositivos Móviles

**NRC :** 1821

**PROFESOR :** Mayta Guillermo, Jorge Luis

**AUDITOR :** Frock

**CLIENTE(S) :** Frock

**APP A EVALUAR:** Chapa Tu Ruta

**TAREAS A EVALUAR**

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas dentro de la aplicación móvil:

* Registro de un usuario nuevo

* Registro de un vehículo

* Creación de un paradero (Stop)

* Edición de un paradero

* Edición de datos del vehículo

* Visualización de la vista de paraderos (Stops)

* Navegación entre formularios y pantallas de registro


**ESCALA DE SEVERIDAD**

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad

| Nivel | Descripcion                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Problema superficial: Puede ser fácilmente superador por el usuario y ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo.                   |
| 2     | Problema menor: Puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente reléase. |
| 3     | Problema mayor: Ocurre frecuentemente o los usuarios no son capaces de resolverlos. Es importante que sean corregidos y se les debe asignar una prioridad alta.                                 |
| 4     | Problema muy grave: Un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento.                               |

**TABLA DE RESUMEN**

| # | Problema                                                                                | Severidad | Heurística / Principio Violada(o)                              |
|---|-----------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------|
| 1 | Campos de FirstName y LastName tienen altura inconsistente respecto a Phone y Email     | 2         | **Usability:** Consistencia y estándares                       |
| 2 | El título "Create Vehicle" muestra información interna no relevante ("ProfileId: {Id}") | 2         | **Information Architecture:** Is it relevant?                  |
| 3 | Las imágenes de los formularios se muestran más pequeñas que su contenedor              | 2         | **Usability:** Diseño estético y minimalista / Consistencia    |
| 4 | Al crear un nuevo paradero, la imagen previa sigue apareciendo en el diálogo            | 3         | **Usability:** Prevención de errores                           |
| 5 | En edición de vehículo, los datos se guardan desordenados (placa, modelo, color)        | 4         | **Usability:** Correspondencia entre sistema y el mundo real   |
| 6 | En la pantalla de Stops, el mapa no ocupa el espacio cuando no existen paraderos        | 2         | **Information Architecture:** Layout adaptable / Is it usable? |

**DESCRIPCIÓN DE PROBLEMAS**

**PROBLEMA 1: Campos de FirstName y LastName tienen altura inconsistente respecto a Phone y Email**

**Severidad:** 2

**Heurística Violada:** Usabilidad – Consistencia y estándares

**Problema:**

En el formulario de registro de perfil, los campos FirstName y LastName presentan una altura mayor que los campos Phone y Email. Esto genera una interfaz visualmente inconsistente, lo que puede generar sensación de desorden o falta de interés en la aplicación.

<img src="resources/chapter-4/auditoria/problema1-auditoria.png" height=400>

**Recomendación:**

Alinear la altura, padding interno y estilo visual de todos los campos para mantener consistencia visual dentro del formulario.

<br>

**PROBLEMA 2: El título "Create Vehicle" muestra información interna no relevante**

**Severidad:** 2

**Heurística Violada:** Information Architecture – Is it relevant?

**Problema:**

El formulario de creación de vehículo muestra el texto “ProfileId: {Id}”, que corresponde a información interna del sistema y que no tiene utilidad para el usuario final. Esto genera ruido visual y puede causar confusión.

<img src="resources/chapter-4/auditoria/problema2-auditoria.png" height=400>

**Recomendación:**

Eliminar el ID del perfil del encabezado del formulario. Esta información debe manejarse internamente y no mostrarse en la UI.

<br>

**PROBLEMA #3: Las imágenes de los formularios se muestran más pequeñas que su contenedor**

**Severidad:** 2

**Heurística Violada:** Usabilidad – Diseño estético y minimalista / Consistencia

**Problema:**

En los formularios de registro y edición, tales como registro de paraderos, registro y edición de vehiculos, el área destinada a mostrar la imagen o la previsualización no se ocupa completamente; la imagen renderizada aparece pequeña en relación al contenedor. El usuario percibe esto como un error visual.

<img src="resources/chapter-4/auditoria/problema2-auditoria.png" height=400>

<img src="resources/chapter-4/auditoria/problema3-parte2.png" height=400>

**Recomendación:**

Usar **Modifier.fillMaxSize()** junto con **contentScale = ContentScale.Crop** para asegurar que la imagen cubra completamente el espacio asignado.

<br>

**PROBLEMA 4: Al crear un nuevo paradero, la imagen previa sigue apareciendo en el diálogo**

**Severidad:** 3

**Heurística Violada:** Usabilidad – Prevención de errores

**Problema:**

Cuando un usuario crea un paradero en un diálogo y luego vuelve a abrir el mismo diálogo para crear otro, la imagen del paradero anterior continúa visible. Esto sugiere que el estado no se está reiniciando correctamente, lo que puede llevar a errores involuntarios del usuario.

<img src="resources/chapter-4/auditoria/problema4-parte1.png" height=400>
<img src="resources/chapter-4/auditoria/problema4-parte2.png" height=400>

**Recomendación:**

Resetear los estados (imageUri, campos del formulario) cada vez que se abre el diálogo. Esto puede lograrse inicializando valores antes de mostrar el modal.

<br>

**PROBLEMA 5: En edición de vehículo, los datos se guardan desordenados (placa, modelo, color)**

**Severidad:** 4

**Heurística Violada:** Usabilidad – Correspondencia entre sistema y mundo real

**Problema:**

Cuando el usuario edita un vehículo, los datos se guardan de manera incorrecta: la placa aparece en el campo Color y viceversa, etc. Este error compromete la funcionalidad principal del formulario y puede generar datos incorrectos en el sistema. Este es un problema crítico que afecta la integridad de los datos del usuario.

<img src="resources/chapter-4/auditoria/problema5-auditoria-parte1.png" height=400>
<img src="resources/chapter-4/auditoria/problema5-auditoria-parte2.png" height=400>
<img src="resources/chapter-4/auditoria/problema5-auditoria-parte3.png" height=400>

**Recomendación:**

Verificar la asignación de parámetros en el updateVehicle (orden de RequestBody y nombres de los campos). Asegurar que el backend reciba los campos correctos y que los nombres coincidan exactamente con la API.

<br>

**PROBLEMA 6: En la pantalla de Stops, el mapa no ocupa el espacio cuando no existen paraderos**

**Severidad:** 2

**Heurística Violada:** Information Architecture - Layout adaptable / Is it usable?

**Problema:**

Cuando un usuario nuevo entra a la vista de stops y aún no tiene paraderos, el mapa solo ocupa la mitad superior de la pantalla mientras que la parte inferior permanece vacía. Esto genera sensación de error visual y desaprovecha espacio.

<img src="resources/chapter-4/auditoria/problema6-auditoria.png" height=400>

**Recomendación:**

Usar condicionales: Si no hay paraderos, mostrar el mapa ocupando Modifier.weight(1f) sin reserva de espacio para lista. Si existen paraderos, mostrar el mapa y la lista de paraderos con distribución actual.


# Conclusiones

## Conclusiones y recomendaciones.

## Video App Validation

## Video About the product

## Video About the team
