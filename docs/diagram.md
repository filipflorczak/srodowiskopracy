# Schemat Przepływu Aplikacji

Poniższy diagram przedstawia główną ścieżkę użytkownika podczas sesji pracy w aplikacji.

```mermaid
graph TD
    A[Uruchomienie Aplikacji] --> B{Wybór Akcji}
    B --> C[Start Sesji Pomodoro]
    C --> D[Odliczanie: Praca 25 min]
    D --> E{Koniec Czasu?}
    E -- Tak --> F[Alarm i Wybór Przerwy]
    F --> G[Krótka Przerwa - 5 min]
    F --> H[Długa Przerwa - 15 min]
    G --> I[Moduł Ćwiczeń/Relaksu]
    H --> I
    I --> J{Koniec Przerwy?}
    J -- Tak --> B
    J -- Zakończ Dzień --> K[Podsumowanie Statystyk]
