# Archivo-Legal
App para guardar, escanear y ordenar documentos jurídicos. Funciona en celular (Android y iPhone) y en computador. Los archivos se guardan **solo en tu dispositivo**.

## 1. Ponerla en internet (una sola vez)
La cámara y la instalación necesitan una dirección segura (https).
1. Crea una cuenta gratis en **Netlify** (netlify.com).
2. Entra a *Add new site → Deploy manually* y arrastra la carpeta `archivo-legal` completa.
3. Netlify te da un enlace (ej. `https://mi-archivo.netlify.app`). Ese es el enlace de tu app.

## 2. Instalarla
- **Android (Chrome):** abre el enlace → menú ⋮ → *Instalar app*.
- **iPhone (Safari):** abre el enlace → botón Compartir → *Añadir a pantalla de inicio*.
- **Computador (Chrome o Edge):** abre el enlace → ícono de instalar en la barra de direcciones.

## 3. Uso diario
**Escanear a PDF**
1. Toca *Escanear a PDF* → *Tomar foto*. Repite por cada página.
2. Si una foto salió mal, toca *Quitar*.
3. Toca *Terminar y guardar*, completa los datos y guarda.

**Agregar más hojas a un PDF ya creado:** abre el documento → *Agregar páginas* → toma las fotos → *Agregar al PDF*. (Solo funciona con PDF creados por escaneo en esta app.)

**Subir archivos:** toca *Subir archivos* y elige PDF, Word, imágenes, etc.

**Datos de cada documento:** tipo, número de proceso, fecha del documento, notas. La fecha de creación se pone sola.

**Buscar y ordenar:** usa el buscador (nombre, proceso o nota), el filtro por tipo y el selector *Agrupar por* (fecha del documento, fecha de creación, tipo o proceso).

## 4. Bloqueo opcional (Ajustes)
- **PIN o contraseña:** escríbelo y toca *Guardar PIN*. **Si lo olvidas no se puede recuperar.**
- **Huella (Android) o Face ID (iPhone):** toca *Activar huella / Face ID*. Puedes usar PIN, biometría o ambos.
- Para quitarlos, usa *Quitar PIN* o *Desactivar*.
- Es un bloqueo de entrada: no cifra los archivos.

## 5. Google Drive (cada usuario usa su propia cuenta)
**Configuración (la hace una sola vez quien publica la app):**
1. Entra a console.cloud.google.com y crea un proyecto.
2. *APIs y servicios → Biblioteca* → activa **Google Drive API**.
3. *Pantalla de consentimiento de OAuth* → tipo Externo → agrega los correos de quienes la usarán como usuarios de prueba.
4. *Credenciales → Crear credenciales → ID de cliente de OAuth → Aplicación web*. En *Orígenes autorizados de JavaScript* pon el enlace de tu app (sin barra final).
5. Copia el **Client ID** y pégalo en *Ajustes → Client ID de Google* en cada dispositivo.

**Uso:** *Enviar a Drive* en un documento, o *Enviar todo a Google Drive* arriba. Se crea la carpeta **Archivo Jurídico** con una subcarpeta por tipo. Solo se envía lo que aún no está en Drive. Necesitas internet.

## 6. Respaldo y cambio de dispositivo
*Exportar respaldo* crea un archivo `.json` con todo. En el otro dispositivo usa *Importar respaldo*. Haz un respaldo cada cierto tiempo: si borras los datos del navegador, se pierden los documentos.

## Problemas comunes
- **No abre la cámara:** acepta el permiso de cámara y usa el enlace https.
- **Drive no funciona:** revisa el Client ID, que el enlace esté en *Orígenes autorizados* y que tu correo sea usuario de prueba.
- **El PDF en iPhone solo muestra la primera página en la vista previa:** toca *Abrir* para verlo completo.

