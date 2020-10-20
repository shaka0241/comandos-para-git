## Excluir archivos en un repo
Muchas veces nos podremos encontrar con archivos que no deseamos subir al repositorio y siempre debemos excluirlos hacer esto
Manualmente, a veces no es muy agradable, pero hay una forma de hacerlo que es automatizada.

Para excluir archivos y directorios debemos crear un archivo llamado:

.gitignore

Donde colocamos nombres de archivos y directorios a ser ignorados. 

Ejemplo:

# dependencies
/node_modules
/.pnp
.pnp.js

# testing
/coverage

# production
/build

# misc
.DS_Store
.env.local
.env.development.local
.env.test.local
.env.production.local

npm-debug.log*
yarn-debug.log*
yarn-error.log*


