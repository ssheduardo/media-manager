## Integrar manager media

A veces tenemos la necesidad de contar con una herramienta para poder gestionar archivos en nuestros proyectos, para ello podemos hacer uno de un componente llamado **media-manager**

Este repositorio que tengo, ya tiene integrado el paquete mencionado anteriormente.
> Nota: Ante todo tener en cuenta que debemos tener un virtualhost configurado correctamente para este nuevo proyecto.

### Instalación

Clonar el proyecto

```
git clone https://github.com/ssheduardo/media-manager.git
```

Instalamos nuevas dependencias
```
composer install
```

Posteriormente creamos nuestro enlace simbólico a la carpeta storage
```
php artisan storage:link
```
> Verificar que tenemos creado el archivo **.env** en caso no lo este, podemos copiar el que viene de prueba
```
cp .env.example .env
```

Y generamos nuestra **key**
```
php artisan key:generate
```

Por último corremos las migraciones por defecto.

```
php artisan migrate
```

Como último paso, solo nos queda registrarnos, hacer login.
Una vez verificado el usuario y redireccionado a la home, en el menú de la derecha veremos una opción llamada **Gestión de archivos**
