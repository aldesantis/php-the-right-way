---
title: Stile di codifica
---

# Stile di codifica  {#guida_allo_stile_di_codifica_title}

La comunità PHP è grande e diversificata, fatta di innumerevoli librerie, framework e componenti. È comune per gli
sviluppatori PHP scegliere diversi di questi e combinarli in un singolo progetto. È importante che il codice PHP aderisca
(il più fedelmente possibile) a uno stile di codifica comune per rendere facile agli sviluppatori mischiare e usare diverse
librerie nei loro progetti.

Il [Framework Interop Group][fig] (precedentemente noto come 'PHP Standards Group') ha proposto e approvato una serie di
raccomandazioni di stile, note come [PSR-0][psr0], [PSR-1][psr1], [PSR-2][psr2] e [PSR-3][psr3]. Non lasciarti confondere
dai nomi curiosi: queste raccomandazioni non sono che una lista di regole che alcuni progetti come Drupal, Zend, Symfony,
CakePHP, phpBB, AWS SDK, FuelPHP, Lithium etc. stanno iniziando ad adottare. Puoi usarle in uno dei tuoi progetti, o
continuare a usare il tuo stile personale.

Teoricamente dovresti scrivere codice PHP che aderisce ad uno o più di questi standard, in modo che altri sviluppatori
possano facilmente leggere e lavorare col tuo codice, e le applicazioni che implementano i componenti possano essere
consistenti anche quando lavorano con molto codice di terze parti. Queste prime poche raccomandazioni sono progettate per
essere una più estesa di quella precedente:

* [Leggi PSR-0][psr0]
* [Leggi PSR-1][psr1]
* [Leggi PSR-2][psr2]
* [Leggi PSR-3][psr3]
* [Leggi i PEAR Coding Standards][pear-cs]
* [Leggi i Zend Coding Standards][zend-cs]

Puoi usare [PHP_CodeSniffer][phpcs] per controllare che il codice rispetti queste raccomandazioni, e plugin per editor di
testo come [Sublime Text 2][st-cs] per avere feedback in tempo reale.

Usa il [PHP Coding Standards Fixer][phpcsfixer] di Fabien Potencier per modificare automaticamente la sintassi del tuo
codice in modo che sia conforme a questi standard, evitandoti di risolvere tutti i problemi manualmente.

La lingua inglese è preferita per tutti i nomi di simboli e infrastrutture del codice. I commenti possono essere scritti in
qualunque lingua purché facilmente comprensibili da tutte le parti presenti e future che dovranno lavorare sul codice.

[fig]: http://www.php-fig.org/
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[psr3]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-3-logger-interface.md
[pear-cs]: http://pear.php.net/manual/en/standards.php
[zend-cs]: http://framework.zend.com/wiki/display/ZFDEV2/Coding+Standards
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: http://cs.sensiolabs.org/
