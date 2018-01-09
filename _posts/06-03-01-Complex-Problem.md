---
isChild: true
title: Složeniji problem
anchor: complex_problem
---

## Složeniji problem {#complex_problem_title}

Ako ste ikada čitali na temu Dependency Injection-a, onda ste se sigurno susretali sa izrazima *"Inverzija kontrole (Inversion of Control)"*
ili *"Princip inverzije zavisnosti (Dependency Inversion Principle)"*. Ovo su složeni problemi koje Dependency Injection rešava.

### Inverzija kontrole

Inversion of Control je kao što i sam naziv kaže, "zamena kontrole" sistema tako što držimo organizacioni kôd potpuno
odvojeno od naših objekata. U kontekstu Dependency Injection-a, ovo se odnosi na "popuštanje" zavisnosti tako što ih
kontrolišemo i instanciramo na drugom mestu u sistemu.

PHP frejmvorci su godinama implementirali Inverziju kontrole, međutim, postavlja se pitanje koji deo kontrole vi zamenjujete
i gde? Na primer, MVC frejmvorci obično na raspolaganje stavljaju super objekat ili osnovnu kontroler klasu koju ostali
kontroleri moraju da naslede da bi dobili pristup njenim zavisnostima. Ovo **jeste** Inverzija kontrole, međutim, umesto
da olabavi zavisnosti, ovaj metod ih jednostavno izmešta.

Dependency Injection nam omogućava da na elegantniji način rešimo ovaj problem tako što **ubacujemo** (injektujemo)
samo one zavisnosti koje su nam potrebne i kada su nam potrebne, umesto da ih hardkodujemo i direktno instanciramo.

### Dependency Inversion princip

Dependency Inversion princip se odnosi na slovo "D" u SOLID setu principa objektno-orijentisanog programiranja, koji glasi:
*"oslanjaj se na apstrakcije, a ne na konkretne implementacije"*. Jednostavno, ovo znači da naše zavisnosti treba da budu
interfejsi/ugovori ili apstraktne klase, a ne konkretne implementacije. Vrlo jednostavno možemo refaktorisati prethodni primer kako bi bio
u skladu sa ovim principom.

{% highlight php %}
<?php
namespace Database;

class Database
{
    protected $adapter;

    public function __construct(AdapterInterface $adapter)
    {
        $this->adapter = $adapter;
    }
}

interface AdapterInterface {}

class MysqlAdapter implements AdapterInterface {}
{% endhighlight %}

Postoji nekoliko prednosti toga što klasa `Database` sada zavisi od interfejsa umesto od konkretne implementacije.

Pretpostavimo da radite u timu, a vaš kolega radi na adapteru. U našem prvom primeru, morali bismo da čekamo na kolegu da završi adapter pre nego što
bismo mogli da mock-ujemo isti za potrebe unit testova. A sada kada je zavisnost u vidu interfejsa/ugovora, možemo bez problema da
mock-ujemo taj interfejs znajući da će naš kolega napraviti adapter u skladu sa tim ugovorom.

Još veći benefit ovog pristupa jeste to što je naš kôd mnogo skalabilniji. Ako posle nekog vremena odlučimo da pređemo na drugi tip baze podataka,
dovoljno je da napišemo adapter koji implementira postojeći interfejs i zatim ga koristimo kao dependency naše `Database` klase, pri čemu neće biti
potrebe za bilo kakvim dodatnim refaktorisanjem, jer smo sigurni da je adapter u skladu sa interfejsom.
