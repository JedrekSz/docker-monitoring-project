# Containerized Infrastructure with Monitoring

## Opis projektu

Projekt prezentuje wdrożenie oraz monitorowanie aplikacji webowej w środowisku kontenerowym.
Zostało zbudowane środowisko wielokontenerowe z wykorzystaniem Docker Compose, obejmujące aplikację, bazę danych oraz system monitoringu.

<img width="1552" height="755" alt="image" src="https://github.com/user-attachments/assets/8093a060-53a1-4360-bebf-5e20d5e58c5c" />


## Architektura

* WordPress – aplikacja webowa
* MySQL – baza danych
* Prometheus – zbieranie metryk
* Node Exporter – metryki systemowe
* Grafana – wizualizacja i alerty

## Technologie

* Docker
* Docker Compose
* Prometheus
* Grafana
* Linux

## Funkcjonalności

* uruchomienie aplikacji w architekturze docker
* trwałe przechowywanie danych (Docker volumes)
* monitoring zasobów systemowych (CPU, RAM)
* dashboardy w Grafanie
* alerty na podstawie progów (np. wysokie użycie CPU)

## Uruchomienie

```bash
docker compose up -d
```

## Dostęp

* aplikacja: http://localhost:8080
* Grafana: http://localhost:3000
* Prometheus: http://localhost:9090

## Monitoring

Dane systemowe zbierane są przez Node Exporter i przetrzymywane w Prometheusie.
Grafana służy do wizualizacji metryk takich jak:

* użycie CPU
* użycie pamięci RAM
* ruch sieciowy
* wykorzystanie dysku

## Alerty

Skonfigurowano alert dla wysokiego użycia CPU.
