# b0-0.1 · Metodología y estructura

- Alumno: Alvaro Garcia
- Bloque: B0 — Prerrequisitos
- Fase / ejercicio: B0.P02 Casa Manual de soporte
- Fecha de inicio: 23/10/2026
- Fecha de entrega: 26/10/2026

## 🎯 Qué se pedía

Crear un manual de soporte técnico desde cero dentro de una bóveda de Obsidian y un repositorio local y remoto en Git/GitHub (`sor-manual-soporte-casa`). Había que gestionar tres versiones progresivas del producto (manual inicial, corrección de un procedimiento de conexión y ampliación con nuevos procedimientos e imagen), consultar de forma histórica la primera versión sin alterar el flujo y cerrar la bitácora con un commit documental final.

## ⌨️ Comandos y pasos importantes

- `git --version`.
- git init.
- git branch -M main
- git remote add origin  
- git add
- git commit -m  
- git push 
- git switch -detach  

## 🛠️ Qué he hecho

- Comprobé la identidad global de Git, la versión instalada y la autenticación mediante claves SSH con GitHub.
- Creé la bóveda local `Boveda_Manual_Casa` en una ubicación independiente fuera de OneDrive y de SOR, estructurando únicamente las carpetas iniciales requeridas (`00_Grabaciones`, `01_Proyecto`, `00_Bitacora`, `manual/procedimientos`).
- Redacté la bitácora con la plantilla correspondiente, el fichero `.gitignore` para excluir los vídeos locales, el `README.md` inicial y el procedimiento `manual/procedimientos/sin-conexion.md`.
- Inicialicé el repositorio de Git dentro de `01_Proyecto`, creé el repositorio vacío `sor-manual-soporte-casa` en GitHub y vinculé el remoto `origin`.
- Realicé la primera versión seleccionando los archivos iniciales con `git add`, comprobando el estado con `git diff --cached`, guardando con `git commit` y subiendo con `git push -u origin main`.
- Modifiqué el procedimiento de conexión (`sin-conexion.md`) intercambiando el orden de las comprobaciones técnicas, y registré la segunda versión mediante commit y push.
- Amplié el producto creando las carpetas `manual/imagenes/` y `manual/videos/`, añadiendo los procedimientos `impresora.md` y `sin-sonido.md`, actualizando el `README.md` con nuevos enlaces e incorporando una captura de diagnóstico en PNG junto a los clips de prueba locales ignorados por `.gitignore`.
- Preparé de forma individualizada cada archivo de la ampliación, comprobé el índice y subí la tercera versión al repositorio remoto.
- Consulté de forma histórica y desacoplada la primera versión del manual empleando el código hash del primer commit (`git switch -detach`) y regresé con seguridad a la rama `main`.
- Cerré la grabación en vídeo añadiendo las marcas de tiempo requeridas y completé la bitácora con los enlaces definitivos, ejecutando un cuarto commit documental y su respectivo `push`.

## 🚩 Qué me ha fallado y cómo lo he resuelto

Nada, ya que se siguieron estrictamente las comprobaciones paso a paso de la guía (como git status, git diff y la revisión previa de rutas y selecciones en el índice) para evitar mezclar archivos, dejar cambios pendientes o saltarse restricciones de exclusión.

## 🤔 Respuestas a las preguntas

1. **¿Por qué Git se inicializa solo en 01_Proyecto y la grabación queda fuera?** Para que el control de versiones y el historial afecten exclusivamente al proyecto de trabajo, manteniendo los archivos de configuración de Obsidian y las grabaciones pesadas de vídeo independientes del repositorio.
    
2. **¿Qué muestran status y diff antes de preparar la corrección del procedimiento? Cita la instrucción anterior y la nueva.** `git status` identifica el archivo modificado (`manual/procedimientos/sin-conexion.md`) sin otros cambios pendientes. `git diff` muestra con líneas retiradas (`-`) la instrucción anterior (`1. Abre el navegador y prueba la página interna.`) y con líneas añadidas (`+`) la nueva (`1. Comprueba visualmente que el cable de red está conectado.`).
    
3. **¿Por qué un archivo nuevo aparece en status pero no en el diff de README.md?** Porque los archivos nuevos sin seguimiento todavía no forman parte del repositorio ni del índice que evalúa ese diff específico del `README.md`.
    
4. **¿Qué preparas con cada add y qué compruebas con diff --cached antes del commit?** Con cada `add` se selecciona un archivo concreto para incorporarlo al índice de preparación del siguiente commit. Con `git diff --cached` se revisa el contenido exacto que está listo en el índice para verificar que solo se guardarán los cambios deseados.
    
5. **¿Qué demuestra check-ignore y qué comprobaste además para saber que los clips existen?** `git check-ignore -v` demuestra y justifica la regla y línea del archivo `.gitignore` por la cual los vídeos de prueba son excluidos del seguimiento. Además, se comprobó visualmente en el gestor de archivos y reproduciéndolos que los clips existían de forma local.
    
6. **¿Qué diferencias concretas observaste en el manual del primer commit y qué recuperaste al volver a main?** En el primer commit, el procedimiento de conexión indicaba primero abrir el navegador y luego comprobar el cable, y no existían los ficheros de impresora, sonido ni la imagen de diagnóstico. Al volver a `main`, se recuperó la versión actual avanzada con el orden corregido, los tres enlaces nuevos y la imagen de diagnóstico.
    
7. **¿Qué aporta un historial cuando dos técnicos necesitan conocer el procedimiento vigente?** Aporta un registro estructurado y entregas fechadas que permiten comparar de forma fiable qué instrucciones exactas recibió el equipo en cada momento.
    
8. **¿Por qué commit y push son acciones diferentes y qué miraste en GitHub?** `git commit` guarda una versión local de los cambios en el equipo, mientras que `git push` transfiere esos cambios guardados al repositorio remoto. En GitHub se revisó que los ficheros, la estructura de carpetas, la ausencia de elementos ignorados y la bitácora estuvieran publicados de forma correcta.
    
9. **¿Qué pasos repetirías para corregir otra instrucción y cuáles se hicieron una sola vez?** Se repetirían los pasos de editar el archivo, comprobar el estado con `git status` y `git diff`, preparar el cambio con `git add`, verificar con `git diff --cached`, guardar con `git commit` y subir con `git push`. Se hicieron una sola vez la inicialización del repositorio (`git init`), la fijación de la rama principal (`git branch -M main`) y el registro del remoto

## 🔗 Enlaces

- **Vídeo de esta fase:** https://youtu.be/XXXXXXXXXXX
- **Playlist:** B0_Prerrequisitos

## 💭 Dudas / a repasar

- (lo que no te ha quedado claro)