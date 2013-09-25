---
isChild: true
title:   Interfaccia da linea di comando
---

## Interfaccia da linea di comando {#interfaccia_da_linea_di_comando_title}

PHP è stato creato principalmente per scrivere applicazioni Web, ma è anche utile nella creazione di programmi da linea
di comando (CLI - Command Line Interface). I programmi da linea di comando aiutano ad automatizzare compiti come il testing, la pubblicazione e
l'amministrazione dell'applicazione.

I programmi PHP da linea di comando sono potenti perché puoi usare il codice della tua applicazione direttamente, senza
dover creare una GUI sicura. Accertati solo di non mettere gli script CLI nella root pubblica!

Prova ad eseguire PHP dalla tua linea di comando:

{% highlight bash %}
> php -i
{% endhighlight %}

L'opzione `-i` visualizzerà la tua configurazione PHP proprio come la funzione [`phpinfo`][phpinfo].

L'opzione `-a` fornisce una shell interattiva, simile all'IRB di Ruby o alla shell interattiva di Python. Ci sono anche
altre [opzioni][cli-options] utili.

Scriviamo ora un semplice programma "Hello, $name". Per provarlo, crea un file chiamato `hello.php` come nell'esempio.

{% highlight php %}
<?php
if ($argc != 2) {
    echo "Utilizzo: php hello.php [nome].\n";
    exit(1);
}
$name = $argv[1];
echo "Hello, $name\n";
{% endhighlight %}

PHP imposta due variabili speciali a seconda degli argomenti con cui viene
eseguito il tuo script. [`$argc`][argc] è una variabile intera contenente il
*numero* degli argomenti e [`$argv`][argv] è un array contenente il *valore* di
ciascun argomento. Il primo argomento è sempre il nome del tuo file PHP, in
questo caso `hello.php`.

L'espressione `exit()` è usata con un numero diverso da zero per far sapere alla shell che l'esecuzione del comando è
fallita. Codici di uscita comunemente usati possono essere trovati [qui][exit-codes].

Per eseguire lo script sopra dalla linea di comando:

{% highlight bash %}
> php hello.php
Utilizzo: php hello.php [nome]
> php hello.php world
Hello, world
{% endhighlight %}

 * [Impara a eseguire PHP dalla linea di comando][php-cli]
 * [Impara a configurare Windows per l'esecuzione CLI][php-cli-windows]

[phpinfo]: http://php.net/manual/it/function.phpinfo.php
[cli-options]: http://www.php.net/manual/it/features.commandline.options.php
[argc]: http://php.net/manual/it/reserved.variables.argc.php
[argv]: http://php.net/manual/it/reserved.variables.argv.php
[php-cli]: http://php.net/manual/it/features.commandline.php
[php-cli-windows]: http://www.php.net/manual/it/install.windows.commandline.php
[exit-codes]: http://www.gsp.com/cgi-bin/man.cgi?section=3&topic=sysexits
