npm init - inicia el proyecto

npm --version - Muestra la versión de npm

npm list - Muestra los paquetes instalados

npm list -g - Muestra los paquetes instalados de forma global

npm list -g --depth=0 - Muestra los paquetes instalados de forma global sin las dependencias

npm install <nombre paquete>

npm install <nombre paquete> -S - Guarda la dependencia en el package.json

npm install <nombre paquete> -D - Guarda la dependencia en dev en el package.json

npm install <nombre paquete> -g - Instala el paquete de forma global

npm install <nombre paquete>

npm install <nombre paquete> --dry-run - Muestra lo que haría pero no lo ejecuta controlamos que pasaria con las versiones

npm install <nombre paquete>@<version> - Instala una versión específica

npm install <nombre paquete>@latest - Instala la última versión

npm install - actualiza las dependencias o instala las dependencias cuando clonamos un repositorio.

dentro de package.json, en la seccion de script,por defecto viene el comando test, pero podemos crear comandos como por ejemplo: "start": "node index.js" y luego ejecutar npm start en la terminal en nuestro directorio raiz.
podemos en script concatenar con && para ejecutar varios comandos.

npx - Ejecuta un paquete o instancia sin instalarlo

el ejemplo mas comun es npx create-react-app <nombre proyecto>

npx <nombre paquete> - Ejecuta el paquete

npx <nombre paquete> -h - Muestra la ayuda del paquete

npx <nombre paquete> -v - Muestra la versión del paquete

npx <nombre paquete> <comando> - Ejecuta un comando del paquete

npx <nombre paquete> <comando> -h - Muestra la ayuda de un comando del paquete

npx <nombre paquete> <comando> -v - Muestra la versión de un comando del paquete

npm outdated - Muestra los paquetes desactualizados y la versión actual y la última.

npm audit - Muestra los paquetes con vulnerabilidades.

npm audit --json - Muestra los paquetes con vulnerabilidades en formato json.

npm audit fix - Intenta solucionar las vulnerabilidades.

npm audit fix --force - Intenta solucionar las vulnerabilidades forzando la actualización de las dependencias.

npm uninstall <nombre paquete> - Elimina el paquete

npm uninstall <nombre paquete> -S - Elimina el paquete y lo elimina del package.json

npm uninstall <nombre paquete> -D - Elimina el paquete y lo elimina del package.json en dev

npm uninstall <nombre paquete> -g - Elimina el paquete de forma global

si eliminamos de manera manual debemos pasar luego por consola. rm -rf node_modules/ y npm install. asi recompilamos todo de vuelta. sirve para refactorizar.

npm run build - Ejecuta el script build del package.json

npm run build --dd - Ejecuta el script build del package.json en modo debug

npm ci sincroniza el package-lock.json con el package.json.

el package-lock.json es un archivo que se genera cuando instalamos las dependencias y nos sirve para que cuando alguien mas instale las dependencias, se instalen las mismas versiones que nosotros.

al crear un paquete para publicar

debemos recordar hacer la carpeta bin y dentro el archivo que queremos que se ejecute.

luego debemos agregar la logica en el archivo index.js

y agregar todo al package.json como por ejemplo: "bin": { "nombre_paquete": "bin/index.js" },

luego debemos crear una cuenta en npmjs.com y loguearnos con npm login

luego debemos crear un repositorio en github y subir el codigo. debe tener el mismo nombre que tendra en npmjs.com. por eso debemos chequear que no haya ya paquetes con ese nombre.

nos debemos parar en nuestra carpeta y ejecturar

npm link que nos dirá si hay vulnerabilidades o no.

en caso de que no haya vulnerabilidades, ejecutamos npm publish.
