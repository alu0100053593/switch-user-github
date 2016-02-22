# Ejemplo de como cambiar en GitHub el usuario por defecto para un repo 

* Pseudo alumno `nausicachijiro` para probar [GitHub Classroom](https://classroom.github.com) como alumno
* He creado la clave `chuchu` con `ssh-keygen` y la he publicado en github 
* Añado una entrada como esta en `~/.ssh/config`

            Host github-nausica.com
            HostName github.com
            user git
            IdentityFile /Users/casiano/.ssh/chuchu
* El remote que nos da github del repo `git@github.com:nausicachijiro/testing.git`
debe ser cambiado de acuerdo a lo hecho en `~/.ssh/config`:

            $ git remote -v
            origin git@github-nausica.com:nausicachijiro/testing.git
* Para que los commits funcionen con la personalidad alternativa 
  debo anunciarle a git mi nuevo `user` y `email`

            git config user.name nausicachijiro
            git config user.email nausica.chijiro@gmail.com
