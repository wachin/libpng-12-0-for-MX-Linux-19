# libpng-1.2.50-for-MX-Linux-19
Necesito crear el deb de libpng-1.2.50 para MX Linux 19 para poder instalar WPS Office 2016


He compilado libpng-1.2.50 en MX Linux 19

**Biblioteca instalada**

/usr/lib/libpng.so.3.50.0

**Enlaces creados**

libpng12.so enlaza a: /usr/lib/libpng.so.3.50.0
libpng12.so.0 enlaza a: /usr/lib/libpng.so.3.50.0


**Biblioteca instalada**

/usr/lib/libpng12.so.0.50.0


**Enlaces creados**

/usr/lib/libpng.so.3 enlaza a: /usr/lib/libpng12.so.0.50.0


**ENLACE A ENLACE**

/usr/lib/libpng.so enlaza a enlace: libpng12.so


**CREANDO LOS ENLACES SIMBÓLICOS**
Debo crear los siguientes enlaces en MX Linux 19 de 32 bits:


Razonamiento

He compilando libpng-1.2.50 desde código fuente en MX Linux 19 de 32 bits para poder instalar WPS Office 2016, las librerías se instalaron en:

/usr/lib

pero WPS  Office 2016 las busca en:

/usr/lib/i386-linux-gnu/

por esa razón debo allí crear los enlaces simbólicos hasta allí

Solución:

ln -s (Lugar donde existe físicamente el objetivo o blanco) (Destino, nombre del enlace simbólico a crear)

	sudo ln -s /usr/lib/libpng12.so.0.50.0 /usr/lib/i386-linux-gnu/libpng12.so





sudo ln -s /usr/lib/i386-linux-gnu/