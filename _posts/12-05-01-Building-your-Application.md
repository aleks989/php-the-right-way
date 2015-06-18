---
isChild: true
title: Izgradnja i isporučivanje vaše aplikacije
anchor: building_and_deploying_your_application
---

## Izgradnja i isporučivanje vaše aplikacije {#build_title}

Ako zateknete sebe da ručno radite promene šeme baze podataka ili ručno pokrećete testove pre nego što ažurirate svoje
fajlove (ručno), razmislite još jednom! Uz svaki dodatni zadatak koji se izvodi ručno potreban da razvijete novu verziju
aplikacije, šanse za potencijalno fatalne greške se povećavaju. Bez obzira da li se bavite jednostavnim ažuriranjem,
sveobuhvatnom izgradnjom procesa ili čak strategijom kontinuirane integracije, [build automation](http://en.wikipedia.org/wiki/Build_automation) je Vaš prijatelj.

Među zadacima koje biste možda želeli da automatizujete su:

* Upravljanje zavisnostima
* Kompilacija, minifikacija Vaše aktive
* Pokretanje testova
* Pravljenje dokumentacije
* Pakovanje
* Isporučivanje koda (Deployment)


### Alati za automatizaciju izgradnje

Alati za izgradnju mogu biti opisani kao skup skripti koje rukuju zajedničkim zadacima razvoja softvera. Alat za
zgradnju nije deo vašeg softvera, on deluje na vaš softver 'izvana'.

Postoji mnogo dostupnih alata otvorenog koda da vam pomogne sa automatizacijom, neki su napisani u PHP-u, drugi nisu.
To ne treba da vas sputava da ih koristite, ako više odgovaraju za određeni posao. Evo nekoliko primera:

[Phing](http://www.phing.info/) je najlakši način da počnete sa primenom automatizacije isporuivanja koda u svetu PHP-a. Pomoću Phing-a
možete da kontrolišete pakovanje, angažovanje(deployment) ili testiranje procesa unutar jednostavne XML build datoteke. Phing (koji se zasniva na [Apache Ant](http://ant.apache.org/)) obezbeđuje bogat set zadataka, obično potrebnih za instalaciju ili ažuriranje web aplikacija i može se proširiti dodatnim prilagođenim zadacima, pisanim u PHP-u.

[Capistrano](https://github.com/capistrano/capistrano/wiki) je sistem namenjen *srednjim-do-naprednim programerima* za
izvršavanje komandi na struktuiran, ponovljivi način na jednoj ili više udaljenih mašina. Prekonfigurisan je za primenu (deploying) na Ruby on Rails applikacijama, međutim ljudi **uspešno angažuju(deploying) PHP sisteme** sa njim. Uspešno korišćenje Capistrana zavisi od radnog iskustva sa Ruby i Rake.

Blog post Dejva Gardnera [PHP Deployment with Capistrano](http://www.davegardner.me.uk/blog/2012/02/13/php-deployment-with-capistrano/)
je dobra polazna tačka za PHP developere zainteresovane za Capistrano.

[Chef](http://www.opscode.com/chef/) je više od skeleta(framework) za primenu(deployment), to je veoma moćan Ruby baziran sistemski integracioni skelet(framework) koji ne samo da razvija(deploy) Vaše aplikacije već može da izgradi i celokupno serversko okruženje ili virtuelne kutije(virtual boxes).

Chef resursi za PHP developere:

* [Trodelna blog serija o angažovanju(deploying) LAMP applikacije sa Chef, Vagrant i EC2](http://www.jasongrimes.org/2012/06/managing-lamp-environments-with-chef-vagrant-and-ec2-1-of-3/)
* [Chef Kuvar koji instalira i konfiguriše PHP 5.3 i PEAR sistem za upravljane paketima](https://github.com/opscode-cookbooks/php)

Dalje čitanje:

* [Automatizujte Vaš projekat sa Apache Ant](http://net.tutsplus.com/tutorials/other/automate-your-projects-with-apache-ant/)
* [Maven](http://maven.apache.org/), build framework baziran na Ant-u i [kako ga koristiti sa PHP](http://www.php-maven.org/)

### Continuous Integration

> Kontinuirana integracija je praksa softverskog razvoja u kojoj članovi tima često integrišu svoj rad, uglavnom svaka
> osoba integriše najmanje jednom dnevno — što rezultira sa više integracija dnevno. Mnogi timovi nalaze da ovakav
> pristup vodi do značajnog smanjenja integracionih problema i omogućava timu da razvija kohezivni softver mnogo brže.

*-- Martin Fowler*

Postoje različiti načini za implementaciju kontinuirane integracije za PHP. Nedavno je [Travis CI](https://travis-ci.org/) uradio veliki posao čineći od kontinuirane integracije stvarnost čak i za male projekte. Travis CI je hosted servis kontinuirane integracije za open source zajednicu. Integrisan je sa GitHub-om i nudi prvoklasnu podršku za mnoge jezike, uključujući i PHP.

Dalje čitanje:

* [Continuous Integration with Jenkins](http://jenkins-ci.org/)
* [Continuous Integration with PHPCI](http://www.phptesting.org/)
* [Continuous Integration with Teamcity](http://www.jetbrains.com/teamcity/)
There are different ways to implement continuous integration for PHP. Recently [Travis CI] has done a great job of
making continuous integration a reality even for small projects. Travis CI is a hosted continuous integration service
for the open source community. It is integrated with GitHub and offers first class support for many languages including
PHP.

#### Further reading:

* [Continuous Integration with Jenkins][Jenkins]
* [Continuous Integration with PHPCI][PHPCI]
* [Continuous Integration with Teamcity][Teamcity]


[buildautomation]: http://en.wikipedia.org/wiki/Build_automation
[Phing]: http://www.phing.info/
[Apache Ant]: http://ant.apache.org/
[Capistrano]: https://github.com/capistrano/capistrano/wiki
[phpdeploy_capistrano]: http://www.davegardner.me.uk/blog/2012/02/13/php-deployment-with-capistrano/
[Chef]: http://www.opscode.com/chef/
[chef_vagrant_and_ec2]: http://www.jasongrimes.org/2012/06/managing-lamp-environments-with-chef-vagrant-and-ec2-1-of-3/
[Chef_cookbook]: https://github.com/opscode-cookbooks/php
[Chef_tutorial]: https://www.youtube.com/playlist?list=PLrmstJpucjzWKt1eWLv88ZFY4R1jW8amR
[apache_ant_tutorial]: http://net.tutsplus.com/tutorials/other/automate-your-projects-with-apache-ant/
[Travis CI]: https://travis-ci.org/
[Jenkins]: http://jenkins-ci.org/
[PHPCI]: http://www.phptesting.org/
[Teamcity]: http://www.jetbrains.com/teamcity/
[Deployer]: https://github.com/deployphp/deployer
