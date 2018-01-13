## ¿Qué es git?

* `Sistema de control de versión distribuido`

- Creado por Linus Torvalds

- Ligero (uso snapshots)

- Crear `branch`

![alt text](https://git-scm.com/book/en/v2/images/distributed.png "Diagrama control de versión distribuido")

## Ciclo de vida Git

1.Iniciar repositoro

* `Clonar` repositorio si ya existe

```git
git clone #urlAClonar
```

* o Iniciar repositorio local

```git
git init
```

2. Modificar y/o crear archivos

3. Agregar Archivos editados al area `staging`

* Agregar todos los archivos
  ```git
  git add .
  ```
* Agregar un archivo especifico
  ```git
  git add config.js
  ```

4. Hacer commit de archivos en `stagin`

```git
  git commit -m "Mensaje descriptivo de los cambios realizados"
```

5. Hacer `push` de los cambios al servidor de ser necesario

```git
git push origin master
```

![alt text](https://git-scm.com/figures/18333fig0201-tn.png "flujo básico git")

## Flujo de trabajo

1. Todo lo que existe dentro del `repositorio master` debe estar listo para producción

2. Hacer `fork` al `repositorio master`

3. Para trabajar en algo nuevo es necesario crear un `branch` de `master` con un nombre descriptivo

4. Hacer `commits` locales y regulares en el branch, hacer `push` a una branch

5. Cuando este listo para hacer `merge` al `repositorio principal` o se require ayuda o feedback se debe abrir un `pull request`

6. Despues de que los cambios sean revisados y aprovados en el `pull request` se hace `merge` al `repositorio master`

7. Al hacer merge se debe de enviar a producción lo antes posible

8. Hacer `pull` a los cambios en master y reiniciar el ciclo ( volver a 3)

## Glosario

* **Sistema de control de versión distribuido:** todos los equipos cuentan con una copia completa incluyendo el historial.

* **Branch:** git crea un nuevo puntero dirigido a un punto en especifico en el historial y permite crear una nueva historia a partir del mismo sin dañar, modificar o eliminar la linea original

* **Clonar:** Obtener una copia idéntica e independiente de un repositorio remoto en el equipo local

* **Stagin:** estado en el que se encuentra un archivo despues de ser editado pero antes de hacer el cambio permanente (`commit`)

* **Push:** Enviar todos los `commits`locales al repositorio remoto

* **Pull:** Obtener todos los commits remotos y hacer `merge` al branch actual

* **Repositorio Master:** Repositorio principal, siempre listo para lanzar a producción y no puede ser editado directamente

* **Fork:** Obtener una copia idéntica e independiente de un repositorio almacenado de manera remota, pero mantiene una referencia al repositorio principal

* **Commit:** Guardar los cambios realizados al doucmento el la BD de git local

* **Merge:** Forma de integrar cambios entre dos branch fusionando dos ramas

* **Rebase:** Forma de integrar cambios entre dos ramas, reorganizando los commits de una de ellas

* **Pull Request:** Es una petición que realiza el propietario de un `fork`al propietario del repositorio original para incorporar los commits que están en una rama particular del fork al repositorio principal

* **Upstreams:** Repositorios remotos de los cuales podemos obtener cambios

* **Fetch:** Accion de obtener los commits remotos de un upstream sin integrarlos a ningun branch
