# Ejercicio Git - 1 - Trabajo en local

Despliegue de Aplicaciones Web - Realizado por: Ángel Villabrille Fernández

[TOC]

## Cuestiones

1. Inicializa un nuevo repositorio Git en una carpeta llamada "forty" y agrega los archivos proporcionados en el aula virtual. Realiza el primer commit.

   ```bash
   mkdir forty
   cd forty
   git init
   git add .
   git commit -m "Primer commit"
   ```

   ![image-20241023085233922](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023085233922.png)

2. Renombra la rama master a main , si es necesario.

   ```bash
   git branch -M main
   ```

   ![image-20241023085349610](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023085349610.png)

3. Haz que los ficheros README.txt , LICENSE.txt , passwords.txt , y también todos los ficheros con extensión .md , sean ignorados por el control de versiones.

   ```bash
   git add .gitignore
   git commit -m "añadimos .gitignore"
   ```

   ![image-20241023091322581](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023091322581.png)

![image-20241023091503210](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023091503210.png)

4. Crea el archivo passwords.txt . Lista los archivos ignorados, comprueba que esté correcto.

   ```bash
   git ls-files --others -i --exclude-standard
   ```

   ![image-20241023092203034](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023092203034.png)

5. Crea una rama llamada "feature-content". Cambia, en la línea 3477, el font-size por 1.5em en el archivo main.css.

   ```bash
   git checkout -b feature-content
   git add main.css
   ```

   ![image-20241023093645605](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023093645605.png)

6. Elimina el archivo "passwords.txt" en la carpeta forty . Verifica el estado del repositorio. ¿Hay cambios pendientes?

   ```bash
   rm passwords.txt
   git status
   ```

   ![image-20241023093837286](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023093837286.png)

7. Crea un nuevo archivo llamado " about.html ", partiendo del archivo generic.html y agrégalo al repositorio.

   ```bash
   cp generic.html about.html
   git add about.html
   git commit -m "Añadir about.html"
   ```

   

8. Cambia a la rama main . Examina los logs del repositorio de forma gráfica.

   ```bash
   git checkout main
   git log --graph --oneline --all --decorate
   ```

   ![image-20241023094813136](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023094813136.png)

9. Modifica algo en el archivo generic.html , comprueba que hay cambios, y realiza otro commit . Examina los logs del repositorio de forma gráfica.

   ```bash
   git checkout feature-content
   git status
   git add .
   git commit -m "cambios en generic"
   ```

   ![image-20241023095200135](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023095200135.png)

   ![image-20241023095425104](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023095425104.png)

![image-20241023095235811](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023095235811.png)

![image-20241023095259507](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023095259507.png)

10. Modifica algo en el fichero elements.html . Confirma los cambios, pero no hagas commit. Mira el estado del repositorio.

    ```bash
    git checkout main
    git add .
    git status
    git log --oneline -graph -all --decorate
    ```

    ![image-20241023100332489](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023100332489.png)

![image-20241023100346552](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023100346552.png)

![image-20241023100359416](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023100359416.png)

![image-20241023100411015](C:\Users\alumno\AppData\Roaming\Typora\typora-user-images\image-20241023100411015.png)

11. Mira las diferencias de elements.html . Los cambios no nos gustan, deshaz los cambios de elements.html . Comprueba que no hay cambios pendientes.

    ```
    
    ```

13. f

    ```bash
    git checkout main
    git merge feature-content
    git log --oneline --graph -all --decorate
    ```

    

15. f

    ```bash
    git checkout main
    git merge hotfix
    git log --oneline -all --decorate --graph
    ```

16. f

    ```bash
    git log -n3
    ```

17.  f

    ```bash
    git tag v1.0
    git tag -l
    ```

    

