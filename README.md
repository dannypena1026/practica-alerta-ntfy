# Práctica: Hola Mundo + alerta ntfy.sh

**Estudiante:** Danny Peña Adames  
**Matrícula:** 2025-1124

## Objetivo

Al realizar un `git push` a la rama `main`, GitHub Actions ejecuta un programa de Hola Mundo en JavaScript y envía una notificación al canal https://ntfy.sh/devops-itla.

## Archivos

- `hola.js`: muestra dos mensajes en consola con Node.js.
- `.github/workflows/alerta.yml`: automatiza la ejecución y el envío de la notificación.

## Instrucciones

1. Crea en GitHub un repositorio **público** vacío llamado `practica-alerta-ntfy` (sin README, gitignore ni licencia, porque estos archivos ya están preparados).
2. Descomprime este proyecto y abre **Git Bash** en la carpeta `practica-alerta-ntfy`.
3. Ejecuta:

   ```bash
   git init -b main
   git add .
   git commit -m "Hola Mundo con alerta ntfy"
   git remote add origin https://github.com/dannypena1026/practica-alerta-ntfy.git
   git push -u origin main
   ```

4. En GitHub entra a **Actions** y confirma que el flujo `Hola Mundo y alerta a ntfy` termina con marca verde.
5. Abre https://ntfy.sh/devops-itla para encontrar la notificación.
6. Para probar la integración continua otra vez, edita `hola.js`, guarda y ejecuta:

   ```bash
   git add .
   git commit -m "Probar nueva alerta"
   git push
   ```

**Nota:** el tema `devops-itla` en ntfy.sh es público y compartido: cualquiera que lo conozca puede consultar o enviar avisos. No incluyas contraseñas, tokens o datos sensibles en los mensajes. Como otros estudiantes pueden usarlo, identifica tu alerta con el nombre del repositorio.
