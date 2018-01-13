## ¿Qué es git?

* Sistema de control de versión distribuido, todos los equipos cuentan con una copia completa incluyendo el historial.

- Creado por Linus Torvalds

- Ligero (uso snapshots)

- Crear branch

![alt text](https://git-scm.com/book/en/v2/images/distributed.png "Diagrama control de versión distribuido")

## Ciclo de vida Git

1.Iniciar repositoro

* Clonar repositorio si ya existe

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

5. Hacer `push`de los cambios al servidor de ser necesario

```git
git push origin master
```

![alt text](https://git-scm.com/book/en/v2/images/areas.png "flujo básico git")

## Flujo de trabajo

1. Todo lo que existe dentro del `repositorio master` debe estar listo para producción

2. Hacer `fork` al `repositorio master`

3. Para trabajar en algo nuevo es necesario crear un `branch` de `master` con un nombre descriptivo

4. Hacer `commits` locales y regulares en el branch, hacer `push` a una branch

5. Cuando este listo para hacer `merge` al `repositorio principal` o se require ayuda o feedback se debe abrir un `pull request`

6. Despues de que los cambios sean revisados y aprovados en el `pull request` se hace `merge` al `repositorio master`

7. Al hacer merge se debe de enviar a producción lo antes posible

8. Hacer `pull` a los cambios en master y reiniciar el ciclo ( volver a 3)
