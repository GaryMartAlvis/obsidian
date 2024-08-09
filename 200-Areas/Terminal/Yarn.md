**Yarn** es un gestor de paquetes desarrollado por Facebook que se utiliza para manejar dependencias en proyectos JavaScript y Node.js. Su principal objetivo es ofrecer una alternativa más rápida y fiable a npm para la instalación y gestión de paquetes, con características como la instalación paralela de paquetes, la resolución determinista de dependencias y un caché local para mejorar la velocidad. Yarn se enfoca en la consistencia y en la reducción de errores mediante el uso de un archivo de bloqueo (`yarn.lock`) que asegura que las mismas versiones de las dependencias se instalen en cada entorno.

- **`yarn add <paquete>`**: Instala un paquete y lo agrega a las dependencias del proyecto.
- **`yarn install`**: Instala todas las dependencias listadas en el archivo `package.json`.
- **`yarn remove <paquete>`**: Elimina un paquete de las dependencias del proyecto.
- **`yarn upgrade`**: Actualiza las dependencias a sus versiones más recientes.
- **`yarn list`**: Muestra una lista de los paquetes instalados y sus versiones.
- **`yarn init`**: Crea un nuevo archivo `package.json` para el proyecto.
- **`yarn run <script>`**: Ejecuta un script definido en el `package.json`.
- **`yarn outdated`**: Muestra los paquetes que están desactualizados.
- **`yarn cache clean`**: Limpia la caché de Yarn.