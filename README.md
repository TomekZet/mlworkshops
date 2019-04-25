# Warsztaty z uczenia maszynowego
### WMI UAM 2019
### Tomasz Ziętkiewicz
#### Samsung R&D Poland

Cel warsztatów
==============
Celem warsztatów jest zapoznanie uczestników z narzędziami ciągłej integracji (Continous Integration).
Jednym z potencjalnych zastosowań tych narzędzi jest automatyzacja trenowania i ewaluacji systemów uczenia maszynowego.

W ramach warsztatów uczetnicy przygotują:
[1.](#docker) Skrypt budujący obraz Dockera, stanowiący środowisko do wywoływania skryptu z pkt. 2.
2. Skrypt obliczający metryki mierzące jakość systemu ropoznawania mowy
3. "Job" w systemie ciągłej integracji Jenkins służący do obliczania metryk za pomocą skryptu z punktu 1., uruchamiany w środowisku docker
4. Skrypt generujący wykresy na podstawie skumulowanych metryk obliczonych w punkcie 3.

Docker
======

Dostęp
======
Jenkins: http://tzietkiewicz.vm.wmi.amu.edu.pl:8080
logowanie: LDAP (jak w laboratoriach WMI)



Zasoby
=========

* [Jenkins pipelines](https://jenkins.io/doc/book/pipeline/)
* [Docker](https://docs.docker.com/get-started/)
* [Dockerfile](https://docs.docker.com/engine/reference/builder/)
* [Docker run](https://docs.docker.com/engine/reference/run/)


