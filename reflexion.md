# Ejercicio 5 – Reflexión

## 1. ¿Qué es la Integración Continua?

La Integración Continua (CI) es una práctica de desarrollo de software en la que los desarrolladores integran su código en un repositorio compartido de forma frecuente. Cada integración se verifica mediante una compilación automatizada y la ejecución de pruebas, lo que permite detectar errores rápidamente. En nuestro caso, cada vez que hacemos push, GitHub Actions ejecuta automáticamente el workflow `ci.yml` que comprueba que los archivos del proyecto existen y que la estructura HTML es válida.

## 2. ¿Qué es el Despliegue Continuo?

El Despliegue Continuo (CD) es la práctica de desplegar automáticamente cada cambio que pasa las pruebas de CI directamente a producción, sin intervención manual. En nuestro proyecto, cada vez que hacemos push a la rama master y el CI pasa correctamente, GitHub Pages se actualiza automáticamente con la nueva versión de la web gracias al workflow `cd.yml`.

## 3. ¿Qué ventajas tienen en un proyecto de software?

- **Detección temprana de errores:** Los problemas se identifican inmediatamente al hacer push, antes de que se acumulen.
- **Mayor calidad del código:** Las pruebas automáticas garantizan que cada cambio cumple los estándares.
- **Despliegues más rápidos y seguros:** Al automatizar el despliegue, se eliminan errores humanos y se reduce el tiempo entre desarrollo y publicación.
- **Colaboración más eficiente:** Varios desarrolladores pueden trabajar en paralelo con la confianza de que la integración se valida automáticamente.
- **Feedback inmediato:** El desarrollador sabe al instante si su cambio funciona correctamente.

## 4. ¿Qué ocurre cuando hacemos push en un proyecto con CI/CD?

Al hacer push en un proyecto con CI/CD ocurre lo siguiente de forma automática:

1. **Se activa el workflow de CI:** GitHub Actions detecta el push y ejecuta las pruebas definidas en `ci.yml` (comprobar archivos, validar HTML, etc.).
2. **Se verifica el resultado:** Si todas las pruebas pasan (✓), el código se considera válido.
3. **Se activa el workflow de CD:** Simultáneamente, el workflow `cd.yml` empaqueta el proyecto y lo despliega en GitHub Pages.
4. **La página se actualiza:** La web publicada en `https://mcfly005.github.io/proyecto_web/` se actualiza automáticamente con los nuevos cambios.

Todo este proceso ocurre sin intervención manual, en cuestión de segundos.
