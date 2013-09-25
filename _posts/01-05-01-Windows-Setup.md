---
isChild: true
title: Configurazione Windows
---

## Configurazione Windows {#configurazione_windows_title}

Puoi installare PHP su Windows in diversi modi. Puoi scaricare i [binari][php-downloads] e, fino a poco tempo fa, potevi
usare un installer '.msi'. L'installer non è più disponibile e si ferma a PHP 5.3.0.

Per l'apprendimento e lo sviluppo locale puoi usare il webserver integrato in PHP 5.4 e superiori, in modo da non doverlo
configurare. Se preferisci un pacchetto "all-in-one" che include un webserver e MySQL, allora strumenti come
[Web Platform Installer][wpi], [Zend Server CE][zsce], [XAMPP][xampp] e [WAMP][wamp] ti aiuteranno a configurare un ambiente
di sviluppo Windows in men che non si dica. Detto questo, questi strumenti saranno diversi dall'ambiente di produzione,
quindi fai attenzione alle differenze se stai sviluppando su Windows ma pubblicando su Linux.

Se devi far girare un ambiente di produzione su Windows, allora IIS7 ti fornirà quello più stabile e performante. Puoi usare
[phpmanager][phpmanager] (un plugin GUI per IIS7) per rendere più semplice la configurazione e la gestione di PHP.
IIS7 integra già FastCGI, devi solo configurare PHP come handler. Per supporto e ulteriori informazioni, c'è
un'[area dedicata a PHP su iis.net][php-iis].

[php-downloads]: http://windows.php.net
[phpmanager]: http://phpmanager.codeplex.com/
[wpi]: http://www.microsoft.com/web/downloads/platform.aspx
[zsce]: http://www.zend.com/it/products/server-ce/
[xampp]: http://www.apachefriends.org/it/xampp.html
[wamp]: http://www.wampserver.com/
[php-iis]: http://php.iis.net/
