He obtado por tener un repositorio independiente para subir la build y realizar el despliegue.

Partiendo de una app de react seguimos los siguientes pasos: 

1. Añadimos en la sección defineConfig de vite.config.ts el base apuntando al nombre del repositorio:
![vite_config_1](https://github.com/user-attachments/assets/80dba3e1-3923-4c56-af34-b87098b61b8b)

2. Cambiamos dentro de nuestro router el alias BrowserRouter por HashRouter. Añadiendo así una '#' antes de todas las rutas para que github pages las reconozca:
![router](https://github.com/user-attachments/assets/746e2815-ba28-4675-84fe-ff6397d71d70)

3. Realizamos una build:
npm run build
![build](https://github.com/user-attachments/assets/7b2c09de-f896-47b2-9e73-a3184eb61813)

4. Copiamos el contenido de dist al repositorio donde queremos desplegar la app y la subimos:
![git_push](https://github.com/user-attachments/assets/6c96c178-4c10-4085-952d-1d7b20fbc3d6)

5. Dentro del apartado de github pages indicamos que queremos usar la rama main partiendo del root:
![github_pages](https://github.com/user-attachments/assets/ad409451-b0ec-450e-9396-234f21d0b17c)

6. Ahora cada vez que github detecta un nuevo commit en la rama main realizará un action para tener nuestro despliegue listo:
![actions](https://github.com/user-attachments/assets/f7c174aa-fe60-428c-930d-f56663e6b034)

7. Url de la app con github pages:
https://oskweb.github.io/modulo7_cloud_laboratorio_ejercicio1/#/orders
