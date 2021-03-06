# PHP LanguageCode library

[![Latest Stable Version](https://poser.pugx.org/josantonius/LanguageCode/v/stable)](https://packagist.org/packages/josantonius/LanguageCode) [![Latest Unstable Version](https://poser.pugx.org/josantonius/LanguageCode/v/unstable)](https://packagist.org/packages/josantonius/LanguageCode) [![License](https://poser.pugx.org/josantonius/LanguageCode/license)](LICENSE) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/5e3ca0b3edd2415d92d2262afb491d47)](https://www.codacy.com/app/Josantonius/PHP-LanguageCode?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Josantonius/PHP-LanguageCode&amp;utm_campaign=Badge_Grade) [![Total Downloads](https://poser.pugx.org/josantonius/LanguageCode/downloads)](https://packagist.org/packages/josantonius/LanguageCode) [![Travis](https://travis-ci.org/Josantonius/PHP-LanguageCode.svg)](https://travis-ci.org/Josantonius/PHP-LanguageCode) [![PSR2](https://img.shields.io/badge/PSR-2-1abc9c.svg)](http://www.php-fig.org/psr/psr-2/) [![PSR4](https://img.shields.io/badge/PSR-4-9b59b6.svg)](http://www.php-fig.org/psr/psr-4/) [![CodeCov](https://codecov.io/gh/Josantonius/PHP-LanguageCode/branch/master/graph/badge.svg)](https://codecov.io/gh/Josantonius/PHP-LanguageCode)

[English version](README.md)

Lista de 217 códigos de idioma: ISO 639-1.

---

- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Métodos disponibles](#métodos-disponibles)
- [Cómo empezar](#cómo-empezar)
- [Uso](#uso)
- [Listado en formato JSON](#listado-en-formato-json)
- [Tests](#tests)
- [Tareas pendientes](#-tareas-pendientes)
- [Contribuir](#contribuir)
- [Repositorio](#repositorio)
- [Licencia](#licencia)
- [Copyright](#copyright)

---

## Requisitos

Esta clase es soportada por versiones de **PHP 5.6** o superiores y es compatible con versiones de **HHVM 3.0** o superiores.

## Instalación 

La mejor forma de instalar esta extensión es a través de [Composer](http://getcomposer.org/download/).

Para instalar **PHP LanguageCode library**, simplemente escribe:

    $ composer require Josantonius/LanguageCode

El comando anterior sólo instalará los archivos necesarios, si prefieres **descargar todo el código fuente** puedes utilizar:

    $ composer require Josantonius/LanguageCode --prefer-source

También puedes **clonar el repositorio** completo con Git:

  $ git clone https://github.com/Josantonius/PHP-LanguageCode.git

O **instalarlo manualmente**:

Descargar [LanguageCode.php](https://raw.githubusercontent.com/Josantonius/PHP-LanguageCode/master/src/LanguageCode.php) y [anguageCodeCollection.php](https://raw.githubusercontent.com/Josantonius/PHP-LanguageCode/master/src/LanguageCodeCollection.php):

    $ wget https://raw.githubusercontent.com/Josantonius/PHP-LanguageCode/master/src/LanguageCode.php
    $ wget https://raw.githubusercontent.com/Josantonius/PHP-LanguageCode/master/src/LanguageCodeCollection.php

## Métodos disponibles

Métodos disponibles en esta biblioteca:

### - Obtener array con todos los códigos de idioma:

```php
LanguageCode::get();
```

**# Return** (array) → códigos y nombres de idiomas

### - Obtener el nombre del idioma desde código de idioma:

```php
LanguageCode::getLanguageFromCode($languageCode);
```

| Atributo | Descripción | Tipo | Requerido | Predeterminado
| --- | --- | --- | --- | --- |
| $languageCode | Código de idioma, e.g. 'es'. | string | Sí | |

**# Return** (tring|false) → nombre del país

### - Obtener código de idioma desde el nombre del idioma:

```php
LanguageCode::getCodeFromLanguage($languageName);
```

| Atributo | Descripción | Tipo | Requerido | Predeterminado
| --- | --- | --- | --- | --- |
| $languageName | Nombre de idioma, e.g. 'Spanish'. | string | Sí | |

**# Return** (tring|false) → código de idioma

## Cómo empezar

Para utilizar esta biblioteca con **Composer**:

```php
require __DIR__ . '/vendor/autoload.php';

use Josantonius\LanguageCode\LanguageCode;
```

Si la instalaste **manualmente**, utiliza:

```php
require_once __DIR__ . '/LanguageCode.php';
require_once __DIR__ . '/LanguageCodeCollection.php';

use Josantonius\LanguageCode\LanguageCode;
```

## Uso

Ejemplo de uso para esta biblioteca:

### - Obtener array con todos los códigos de idioma:

```php
LanguageCode::get();

/*
array(217) {
  ["aa"]=>
  string(4) "Afar"
  ["ab"]=>
  string(9) "Abkhazian"
  ["af"]=>
  string(9) "Afrikaans"
  ["am"]=>
  string(7) "Amharic"
  ["ar"]=>
  string(6) "Arabic"
  (...)
*/
```

### - Obtener el nombre del idioma desde código de idioma:

```php
LanguageCode::getLanguageFromCode('es'); // string(7) "Spanish"
```

### - Obtener código de idioma desde el nombre del idioma:

```php
LanguageCode::getCodeFromLanguage('spanish'); // string(2) "es"
```

## List in Json format

[Go to the resource](https://gist.github.com/Josantonius/b455e315bc7f790d14b136d61d9ae469).

## Tests 

Para ejecutar las [pruebas](tests) necesitarás [Composer](http://getcomposer.org/download/) y seguir los siguientes pasos:

    $ git clone https://github.com/Josantonius/PHP-LanguageCode.git
    
    $ cd PHP-LanguageCode

    $ composer install

Ejecutar pruebas unitarias con [PHPUnit](https://phpunit.de/):

    $ composer phpunit

Ejecutar pruebas de estándares de código [PSR2](http://www.php-fig.org/psr/psr-2/) con [PHPCS](https://github.com/squizlabs/PHP_CodeSniffer):

    $ composer phpcs

Ejecutar pruebas con [PHP Mess Detector](https://phpmd.org/) para detectar inconsistencias en el estilo de codificación:

    $ composer phpmd

Ejecutar todas las pruebas anteriores:

    $ composer tests

## ☑ Tareas pendientes

- [ ] Añadir nueva funcionalidad.
- [ ] Mejorar pruebas.
- [ ] Mejorar documentación.
- [ ] Refactorizar código para las reglas de estilo de código deshabilitadas. Ver [phpmd.xml](phpmd.xml) y [.php_cs.dist](.php_cs.dist).

## Contribuir

Si deseas colaborar, puedes echar un vistazo a la lista de
[issues](https://github.com/Josantonius/PHP-LanguageCode/issues) o [tareas pendientes](#-tareas-pendientes).

**Pull requests**

* [Fork and clone](https://help.github.com/articles/fork-a-repo).
* Ejecuta el comando `composer install` para instalar dependencias.
  Esto también instalará las [dependencias de desarrollo](https://getcomposer.org/doc/03-cli.md#install).
* Ejecuta el comando `composer fix` para estandarizar el código.
* Ejecuta las [pruebas](#tests).
* Crea una nueva rama (**branch**), **commit**, **push** y envíame un
  [pull request](https://help.github.com/articles/using-pull-requests).

## Repositorio

La estructura de archivos de este repositorio se creó con [PHP-Skeleton](https://github.com/Josantonius/PHP-Skeleton).

## Licencia

Este proyecto está licenciado bajo **licencia MIT**. Consulta el archivo [LICENSE](LICENSE) para más información.

## Copyright

2017 - 2018 Josantonius, [josantonius.com](https://josantonius.com/)

Si te ha resultado útil, házmelo saber :wink:

Puedes contactarme en [Twitter](https://twitter.com/Josantonius) o a través de mi [correo electrónico](mailto:hello@josantonius.com).