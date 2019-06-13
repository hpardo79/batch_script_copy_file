Script Batch para copia de archivos segun nombre utilizando una fecha
-----------------------------------------------------------------------
Script en batch para realizar copia de archivos utilizando como variable la fecha actual en el nombre de los archivos.

Ejemplo practico usando script para el cambio de imagen **wallpaper** segun fecha actual

```
@echo off
echo ...Cambio de imagen de fondo, segun fecha actual...
echo.
set fechaimagen=%date:/=%
for /f "delims=" %%a in ('where /r C:\imagenes\ %fechaimagen%.jpg') do set imagenparahoy=%%a
xcopy /f/y "%imagenparahoy%" "C:\imagenesdefondo\fondoparahoy.jpg*"
echo.
echo ...Completado...
eof
```
Para este ejemplo se deben almacenar las imagenes utilizando como nombre la fecha de su cambio en el mismo formato de la fecha actual.
Ej: ddmmyyyy.jpg
