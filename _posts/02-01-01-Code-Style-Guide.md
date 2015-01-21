---
isChild: false
title: Vodič za stil kodiranja
anchor: code_style_guide
---

# Vodič za stil kodiranja {#code_style_guide}

PHP zajednica je velika i raznovrsna, i sastoji se od nebrojenih biblioteka, frejmvorkova i komponenti. Uobičajeno je da
PHP programeri izaberu nekoliko i iskombinuju ih u jedan projekat. Bitno je da se PHP kod pridržava (što je bliže
moguće) uobičajenom načinu kodiranja da bi se programerima olakšalo kombinovanje i uklapanje različitih biblioteka u
svoje projekte.

[Framework Interop Grupa][fig] je predložila i odobrila niz preporuka za stilove, poznatije kao [PSR-0][psr0],
[PSR-1][psr1] i [PSR-2][psr2]. Ne dozvolite da vas čudna imena zbune, ove preporuke su samo set pravila koja neki
projekti kao što su Drupal, Zend, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium, itd počinju da usvajaju. Možete ih
koristiti za vaše lične projekte, ili nastaviti u vašem ličnom stilu.

Idealno bi bilo da pišete PHP kod koji je u skladu sa poznatim standardom. Ovo može biti bilo koja kombinacija PSR-ova,
ili jedan od standarda kodiranja koji je propisao PEAR ili Zend. To podrazumeva da drugi programeri mogu lako da čitaju
i rade sa vašim kodom, a da su aplikacije koje implementiraju komponente konzistentne čak i pri radu sa dosta koda koji
je kreirala treća strana.

* [Pročitajte o PSR-0][psr0]
* [Pročitajte o PSR-1][psr1]
* [Pročitajte o PSR-2][psr2]
* [Pročitajte o PEAR standardima kodiranja][pear-cs]
* [Pročitajte o Zend standardima kodiranja][zend-cs]
* [Pročitajte o Symfony standardima kodiranja][symfony-cs]

Možete da koristite [PHP_CodeSniffer][phpcs] da proverite da li vam je kod u skladu sa bilo kojom od ovih preporuka, i
pluginove za tekst editore kao što je [Sublime Text 2][st-cs] da biste dobijali feedback u realnom vremenu.

Koristite [PHP Coding Standards Fixer][phpcsfixer] od Fabien Potencier-a da automatski modifikujete sintaksu vašeg koda
tako da odgovara ovim standardima, i tako izbegnete ručno ispravljanje svakog problema.

Engleski jezik se preporučuje za sva imena simbola i infrastrukturu koda. Komentari mogu biti napisani u bilo kom jeziku
koji poznaju sve sadašnje i buduće osobe koje će možda raditi na kodu.

[fig]: http://www.php-fig.org/
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[pear-cs]: http://pear.php.net/manual/en/standards.php
[zend-cs]: http://framework.zend.com/wiki/display/ZFDEV2/Coding+Standards
[symfony-cs]: http://symfony.com/doc/current/contributing/code/standards.html
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: http://cs.sensiolabs.org/
[phptools]: https://github.com/dericofilho/php.tools
[sublime-phpfmt]: https://github.com/dericofilho/sublime-phpfmt
