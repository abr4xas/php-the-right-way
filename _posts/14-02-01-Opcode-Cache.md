---
title:   Caché Opcode
isChild: true
anchor:  opcode_cache
---

## Caché Opcode {#opcode_cache_title}

Cuando se ejecuta un archivo PHP, primero debe ser compilado en [opcodes](https://php-legacy-docs.zend.com/manual/php4/en/internals2.opcodes) (instrucciones en lenguaje de máquina para la CPU). Si el código fuente no ha cambiado, los opcodes serán los mismos, por lo que este paso de compilación se convierte en un desperdicio de recursos de la CPU.

Un caché de opcodes evita la compilación redundante al almacenar los opcodes en la memoria y reutilizarlos en llamadas sucesivas. Normalmente verifica la firma o el tiempo de modificación del archivo primero, en caso de que haya habido algún cambio.

Es probable que un caché de opcodes mejore significativamente la velocidad de tu aplicación. Desde PHP 5.5 hay uno incorporado: [Zend OPcache][opcache-book]. Dependiendo de tu paquete o distribución de PHP, normalmente está activado por defecto; revisa [opcache.enable](https://www.php.net/manual/opcache.configuration.php#ini.opcache.enable) y la salida de `phpinfo()` para asegurarte. Para versiones anteriores, hay una extensión de PECL.

Lee más sobre cachés de opcodes:

- [Zend OPcache][opcache-book] (incluido en PHP desde la versión 5.5)
- Zend OPcache (anteriormente conocido como Zend Optimizer+) ahora es [código abierto][Zend Optimizer+]
- [WinCache] (extensión para MS Windows Server)
- [lista de aceleradores PHP en Wikipedia][PHP_accelerators]
- [PHP Preloading] - PHP >= 7.4


[opcache-book]: https://www.php.net/book.opcache
[Zend Optimizer+]: https://github.com/zendtech/ZendOptimizerPlus
[WinCache]: https://www.iis.net/downloads/microsoft/wincache-extension
[PHP_accelerators]: https://wikipedia.org/wiki/List_of_PHP_accelerators
[PHP Preloading]: https://www.php.net/opcache.preloading
