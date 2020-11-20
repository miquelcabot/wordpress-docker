# wordpress-docker

Wordpress desplegat a Docker. Versió "automàtica", amb el servidor web basat en la imatge `wordpress`.

Per posar en marxa:
```
docker-compose up -d
```

Per aturar:
```
docker-compose down
```

Per configurar a un servidor diferent de `localhost`, modificar el fitxer `www\wp-config.php`, afegint les línies:
```
DEFINE ['WP_HOME', '<url_del_servidor>'];
DEFINE ['WP_SITEURL , '<url_del_servidor>'];

$_SERVER ['HTTP_HOST'] = $_SERVER ['HTTP_X_FORWARDED_HOST'];
```