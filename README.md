# v8Unpack, GCC edition
Добавлен проект CodeBlocks 13.12.
Для сборки требуется Boost.

## Fork of v8Unpack project by Denis Demidov (disa_da2@mail.ru)

[Original project HOME](https://www.assembla.com/spaces/V8Unpack/team)

[Original project svn repo](http://svn2.assembla.com/svn/V8Unpack/)

## Note

V8Unpack - a small console program  for rebuild/build configuration files [1C](http://1c.ru) such as *.cf *.epf *.erf
 
## Plaform 

Windows, POSIX

## Environment

Project for [codelite IDE](http://www.codelite.org/)  
Project for [Codeblocks IDE](http://codeblocks.org/)

## Build

Артефакты/релизы можно скачать с [build-server проекта](https://build.batanov.me/job/v8unpack-win/)

[Прямая ссылка на последнюю успешную сборку win32](https://build.batanov.me/view/e8-script/job/v8unpack-win/label=mingw32/lastSuccessfulBuild/artifact/bin/Release/*zip*/v8unpack.zip)

[Прямая ссылка на последнюю успешную сборку win64](https://build.batanov.me/view/e8-script/job/v8unpack-win/label=mingw64/lastSuccessfulBuild/artifact/bin/Release/*zip*/v8unpack.zip)

### Ubuntu/Debian

```
sudo apt-add-repository ppa:dmpas/e8
sudo apt-get update
sudo apt-get install v8unpack
```

### Fedora\Centos
```
cd /etc/yum.repos.d/
sudo wget http://download.opensuse.org/repositories/home:/pumbaEO/Fedora_22/home:pumbaEO.repo
sudo dnf install v8unpack
```


## Version 3.0

- Оптимизирована сборка .cf файла ключ -B[UILD]. В версии 2.0 сборка корневого контейнера происходила в оперативной памяти.
При сборке больших конфигураций это могло приводить к ошибке "segmentation fault". В версии 3.0 сборка корневого контейнера происходит 
динамически с сохранением элементов контейнера непосредственно в файл по мере их создания.
