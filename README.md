# Warsztaty z uczenia maszynowego
### WMI UAM 2019
### Tomasz Ziętkiewicz
#### Samsung R&D Poland

Cel warsztatów
==============
Celem ierwszego spotkania z serii warsztatów jest zapoznanie uczestników z narzędziami ciągłej integracji (Continous Integration).
Jednym z potencjalnych zastosowań tych narzędzi jest automatyzacja trenowania i ewaluacji systemów uczenia maszynowego.

W ramach warsztatów uczetnicy przygotują:
1. "Job" w systemie ciągłej integracji Jenkins służący do obliczania metryk za pomocą skryptu z punktu 3. [[idz]](#1-jenkins)
2. Skrypt budujący obraz Dockera, stanowiący środowisko do wywoływania skryptu z pkt. 3. [[idz]](#2-docker)
3. Skrypt obliczający metryki mierzące jakość systemu ropoznawania mowy [[idz]](#3-metryki)
4. Skrypt generujący wykresy na podstawie skumulowanych metryk obliczonych w punkcie 4. [[idz]](#4-wykresy)

Zadania
=======

## 1. Jenkins
Jenkins to system ciągłej integracji napisany w języku Java, będący kontynuacją projektu Hudson.
Umożliwia on między innymi automatyczne budowanie, testowanie i wydawanie oprogramowania.
Działa jako aplikacja webowa z graficznym interfejsem umożliwiająca  łatwe zarządzanie i monitorowanie wykonywanych w niej zadań.m z

Dzięki stosowaniu narzędzi ciągłej integracji takich jak Jenkins zespoł pracujący nad danym projektem zyskuje:
 - wspólne środowisko do testowania zmian, replikowania błędów
 - łatwość monitorowania zmian zachodzących w oprogramowaniu
 - środowisko do integracji ze sobą części składowych (np. modułów, modeli) w jedną całość
 - możliwość automatyzacji zadań
 - środowisko, w którym można stworzyć prosty graficzny interfejs służący do uruchamiania pewnych zadań w sposób ineraktywny
 
Funkcjonalność Jenkinsa może być rozszerzana za pomocą licznych wtyczek (pluginów) oferujących bardzo szerokie możliwości dostosowaywania go do własnych potrzeb a także integracji z innymi narzędziami.
 
 ------------------------
 
 Dobrą praktyką jest przygotowanie środowiska ciągłej integracji przed rozpoczęciem prac nad właściwym zadaniem/projektem. Dzięki temu możemy od początku w zautomtyzowany sposób testować nasz program i śledzić generowane przez niego wyniki.
 
 Na drugim spotkaniu z serii warsztatów uczenia maszynowego zajmą się Państwo wytrenowaniem modelu rozpoznawania mowy. Przygotowany na tych zajęciach system ma w założeniu ułatwić Państwu ewaluację jakości tego modelu.

----------------------------------

Na początku przygotujemy Jenkinsowy projekt (w angielskie wersji "Job"). Docelowo będzie on pobierał wyniki rozpoznawania mowy z innego projektu i obliczał wartości metryki WER dla tych wyników.

Na początku zajmiemy się samą konfiguracją projektu, tak, żeby już w trakcie tworzeniu skryptu obliczającego metryki można było testować jego działanie w zewnętrznym środowisku jakim jest Jenkins.

0. Stwórz wydziałowe repozytorium GIT 

1. Zaloguj się na http://tzietkiewicz.vm.wmi.amu.edu.pl:8080 za pomcą konta wydziałowego (jak w laboratoriach WMI)

2. Utwórz nowy projekt

   Istnieje kilka rodzajów projektów w Jenkinsie.

   Po kliknięciu na "Nowy projekt" zobaczymy listę dostępnych rodzajów projektów.
   Nas interesuje projekt typu "Pipeline".

   Jako nazwę proszę wpisać "USERNAME-metrics", gdzie USERNAME proszę zastąpić swoją nazwą użytkownika
   
   

3. Zdefiniuj Pipeline

   Projekty typu Pipeline definiuje się w pliku Jenkinsfile za pomocą skryptu napisanego w jednym z dwóch dostępnych DSL (Domain Specific Language):
    - Scripted pipeline (podzbiór języka Groovy)
    - Declarative pipeline
   Pierwszy z nich daje większe możliwości, drugi jest łatwiejszy i bardziej przejrzysty, ale ma mniejszą siłę ekpresji.

   Fragmenty kodu można również generować za pomocą kreatora dostępnego pod linkiem "Pipeline syntax" na stronie projektu.

   Pisanie własnego Jenkinsfile warto zacząć od lektury https://jenkins.io/doc/book/pipeline/getting-started/




## 2. Docker

* [Docker](https://docs.docker.com/get-started/)
* [Dockerfile](https://docs.docker.com/engine/reference/builder/)
* [Docker run](https://docs.docker.com/engine/reference/run/)

### 3. Metryki


### 4. Wykresy




Zasoby
=========



