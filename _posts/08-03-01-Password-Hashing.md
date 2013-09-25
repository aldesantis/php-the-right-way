---
isChild: true
title:   Hashing delle password
---

## Hashing delle password {#hashing_delle_password_title}

Prima o poi chiunque crea un'applicazione PHP che richiede il login degli
utenti. Username e password vengono salvati nel database e usati successivamente
per autenticare gli utenti al login.

È importante effettuare un [_hashing_][3] appropriato delle password prima di salvarle. L'hashing delle password è una
funzione irreversibile che viene eseguita sulle password degli utenti. Essa produce una stringa a lunghezza fissa che non
può essere decriptata. Ciò significa che puoi confrontare l'hash con un altro per determinare se provengono tutti dalla
stessa stringa d'origine, ma non puoi determinare la stringa di origine. Se l'hashing delle password non viene effettuato
e il tuo database è letto da una persona non autorizzata, tutti gli account utente sono compromessi. Alcuni utenti
potrebbero (sfortunatamente) usare la stessa password per altri servizi. Dunque, è importante gestire la sicurezza
seriamente.


**Eseguire l'hashing con `password_hash`**

In PHP 5.5 è stata introdotta la funzione `password_hash`. In questo momento utilizza l'algoritmo BCrypt, che è il più potente
attualmente supportato da PHP. Sarà aggiornato in futuro per supportare altri algoritmi. La libreria `password_compat` è stata creata
per fornire compatibilità per PHP >= 5.3.7.

Nell'esempio sotto calcoliamo l'hash di una stringa, quindi confrontiamo l'hash con una nuova stringa. Poiché le nostre
stringhe di origine sono differenti ('secret-password' e 'bad-password') questo login fallirà.


{% highlight php %}
<?php
require 'password.php';

$passwordHash = password_hash('secret-password', PASSWORD_DEFAULT);

if (password_verify('bad-password', $passwordHash)) {
    // password corretta
} else {
    // password sbagliata
}
{% endhighlight %}

* [Impara a usare `password_hash`] [1]
* [`password_compat` per PHP  >= 5.3.7 && < 5.5] [2]
* [Impara l'uso della crittografia nell'hashing] [3]
* [RFC di `password_hash`] [4]

[1]: http://hp.net/manual/it/function.password-hash.php
[2]: https://github.com/ircmaxell/password_compat
[3]: http://it.wikipedia.org/wiki/Funzione_crittografica_di_hash
[4]: https://wiki.php.net/rfc/password_hash
