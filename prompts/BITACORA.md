# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts. Herramienta de IA usada: (escribe aqui cual usaste) ## Ejercicio 2: Tokens y ventana de contexto

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. |35|8|
| The students program in Java. |30 |6|
| desafortunadamente |18|4|

El chat gpt tiene memoria de otro chats y por eso me respondio con el contexto del otro chat .

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 |100%| BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec|
| 0.5 |65.3%|BiblioTec, BiblioTec, BiblioTec, BiblioTec, LibroYa |
| 1 |44.5% |BiblioTec, LectoGo, BiblioTec, BiblioTec, BiblioTec|
| 1.8 |32.2%|PaginaLibre, PrestaLibro, BiblioTec, NubeDeTinta, BiblioTec|

Se puede obserbar que al  subir la temperatura empienzan a haber  mas variabilidad en los nombres. El simulador no dara otra palabra ya que tiene una cantidad limitada de palabras(BilblioTec PrestaLibro, LibroYa,LectoGo, PaginaLibre, NubeDeTinta)
## Ejercicio 4: Prompt vago vs estructurado 

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema    |si|si|
| Menciona a los usuarios principales |no|si|
| Tiene exactamente 3 funcionalidades |no|si|
| Esta en 3 parrafos                  |no|si|
| Lo usaria en un informe real        |no|si|

## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol        |Actua como desarrollador Java. Crea un programa en Java.|
| Instruccion|usando una clase Producto con los atributos codigo, nombre, precio y stock.|
| Contexto   |Crea un programa en Java para gestionar los productos de una tienda.|
| Ejemplo    |Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).|
| Formato    |Explica primero la estructura de la clase y luego presenta el codigo Java.|
## Ejercicio 6: Del prompt basico al profesional

| Qué revisar| Cumple (Sí / No)|
|------------|--------------------|
|¿Está escrito en Java y usa Swing?|Sí|
| ¿Pide correo y contraseña?|Sí|
|¿Explica el funcionamiento antes o después del código?|Sí|
|¿El código está organizado en clases?|Sí|
|¿Valida los datos que ingresa el usuario?|Sí|
### Que cambio en las respuestas 
nivel 1:Realizo un programa cualquiera
nivel 2:Me dio un ejemplo sencilo ya que no le especifique.
nivel 3:Uso el contexto  que le di para crear el programa de gestionar productos .
nivel 4:mejoro la respuesta implementando producto con los atributos codigo, nombre, precio y stock
nivel 5:A la respuesta le agrego ejemplos  fue mas precisa e hiba acorde a lo solicitado.
### Prompt
```text
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```

