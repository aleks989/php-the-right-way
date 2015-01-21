---
isChild: true
title: Programske paradigme
anchor: programming_paradigms
---

## Programske paradigme {#programming_paradigms_title}

PHP je fleksibilan, dinamičan jezik koji podržava razne tehnike programiranja. Poslednjih godina se značajno razvio,
naročito dodatkom solidnog objektno-orijentisanog modela u verziji PHP 5.0 (2004), anonimnih funkcija i
namespace-ova u verziji PHP 5.3 (2009), kao i trait-ova u PHP 5.4 (2012).

### Objektno-orijentisano programiranje

PHP ima vrlo upotpunjen set osobina za objektno-orijentisano programiranje, uključujući podršku za klase, apstraktne
klase, interfejse, nasleđivanje, konstruktore, kloniranje, izuzetke i drugo.

* [Pročitajte o Objektno-orijentisanom PHP-u][oop]
* [Pročitajte o Trait-ovima][traits]

### Funkcionalno programiranje

PHP podržava funkcije prve klase, što znači da funkcija može biti dodeljena promenljivoj. I korisnički definisane i
ugrađene funkcije mogu biti referencirane promenljivom i pozvane dinamički. Funkcije se mogu prosleđivati kao argumenti
drugim funkcijama (osobina koja se naziva Funkcije višeg reda) i funkcija može vratiti druge funkcije.

Rekurzija, osobina koja omogućava funkciji da poziva samu sebe, se podržava u jeziku, ali se većina PHP koda
fokusira na iteracije.

Nove anonimne funkcije (sa podrškom za closures) su prisutne od verzije PHP 5.3 (2009).

PHP 5.4 je dodao mogućnost da se closures povežu sa domenom objekta i takođe poboljšao podršku za callables tako da se
one mogu koristiti naizmenično sa anonimnim funkcijama u skoro svim slučajevima.

* Nastavite sa čitanjem o [Funkcionalnom programiranju u PHP-u](/pages/Functional-Programming.html)
* [Pročitajte o anonimnim funkcijama][anonymous-functions]
* [Pročitajte o Closure klasi][closure-class]
* [Više detalja o Closures RFC][closures-rfc]
* [Pročitajte šta su Callables][callables]
* [Pročitajte o dinamičkim pozivima funkcija pomoću `call_user_func_array`][call-user-func-array]

### Meta programiranje

PHP podržava razne varijante meta programiranja preko mehanizama kao što su Reflection API i magičnih metoda (Magic
Methods). Postoji puno magičnih metoda, kao što su `__get()`, `__set()`, `__clone()`, `__toString()`, `__invoke()`, itd.
koje omogućavaju programerima da se uključe u ponašanje klase. Ruby programeri često izjavljuju da PHP-u nedostaje
`method_missing`, ali on postoji kao `__call()` i `__callStatic()`.

* [Pročitajte o magičnim metodama (Magic Methods)][magic-methods]
* [Pročitajte o Reflection][reflection]


[oop]: http://php.net/language.oop5
[traits]: http://php.net/language.oop5.traits
[anonymous-functions]: http://php.net/functions.anonymous
[closure-class]: http://php.net/class.closure
[closures-rfc]: https://wiki.php.net/rfc/closures
[callables]: http://php.net/language.types.callable
[call-user-func-array]: http://php.net/function.call-user-func-array
[magic-methods]: http://php.net/language.oop5.magic
[reflection]: http://php.net/intro.reflection
[overloading]: http://php.net/language.oop5.overloading

