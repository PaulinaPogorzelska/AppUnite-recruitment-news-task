# appunite-news-task

## Instalacja
Projekt został utworzony poprzez Vue-cli 3 w przypadku posiadania starszej wersji może być niezbędna deinstalacja jej i zastąpienie nową.
```
# delete old vue-cli
npm uninstall vue-cli -g
# install vue-cli3
npm install -g @vue/cli
```
Aby aplikacja działała poprawnie należy utworzyć plik .env w którym umieszczona zostanie wartość klucza.
```
VUE_APP_API_KEY= wartość_klucza
```
Aby uruchomić projekt należy wykonać poniżej przedstawiony krok 1) i 2).
### 1)Project setup
```
npm install
```

### 2)Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

## Opis rozwiązania
Zdarzają się zdublowane newsy występujące w bliskiej odległości zazwyczaj prawdopodobą przyczyną jest to że:
-w ten sposób są zbudowana jest baza danych (szczególnie w przypadku sortowania po popularności)
-są odpublikowane więcej niż raz na oryginalnych stronach (odnośniki do oryginalnej strony różnią się)

Więkoszość zdjęc na stronie głownej ma domyślnie wymiary 16x9, aby uzyskały te wymiary odgórnie prawdopodobnie należałoby na sztywno określić szerokość koszyka.

## Możliwości optymalizacji
Wybrałam drogę w której będzie można zaimlementować dwa filtry (ze względu na lepsze doświadczenie dla użytkownika i użyteczność przycisku clear filters, który w przypadku jednego filtra traci na znaczeniu). Do uzyskania tych filtrów należało ustalić daty. Druga droga posiadała gotowe sortowanie (a ponadto nie trzeba było w niej nawężać źródeł- co powoduje dodatkowe zapytania do bazy), co w mojej opini sprawia, że mogłaby być ona bardziej optymalna, jednakże kosztem pewnych fukcjonalności.

