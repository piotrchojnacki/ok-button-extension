O co w tym chodzi?

Stworzyłem prosty dodatek do Firefox'a który po kliknięciu Alt+I klika w pierszy napotkany button z value="Ok".
Testowałem to dla strony page.html i działało.
Dla www.wp.pl już nie działało - nie ma tam raczej takiego przycisku.
Wydaje się, że może to pomóc w stworzeniu rozwiązania jakiego potrzebujesz.

Jest jeszcze kwestia IFrame - bym musiał mieć kod HTML stronki żeby zobaczyć co jest problemem.

Problemem do rozwiązania jest jeszcze zainstalowanie niepodpisanego dodatku.
Poniżej linki z opisem jak zainstalować dodatek:

Jak zainstalować (trzeba instalować co uruchomienie Firefoxa):
https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension

Jak zainstalować trwale (u mnie coś nie działało):
https://wiringbits.net/browser-extensions/2020/11/27/installing-unsigned-extensions-permanently-to-firefox.html

Tutaj jak podpisać i zainstalować (nie sprawdzałem czy działa):

Zainstalować node:
https://nodejs.org/en/download

Nastepnie:
https://github.com/mozilla/web-ext

Zainstalować web-ext:
npm install --global web-ext

Sprawdzić czy działa:
web-ext --version

Jeżeli nie to:
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

Jest trochę zabawy żeby podpisać:

1. Aby podpisać dodatek dla Firefoksa za pomocą narzędzia web-ext, możesz wykonać następujące kroki:

2. Upewnij się, że masz zainstalowane narzędzie web-ext. Możesz zainstalować je globalnie za pomocą narzędzia npm (Node Package Manager), wykonując polecenie:

	```npm install --global web-ext```

3. Przejdź do katalogu, w którym znajduje się kod źródłowy twojego rozszerzenia.

4. W terminalu lub wierszu poleceń uruchom polecenie web-ext sign. To polecenie podpisało dodatek, przygotowując go do instalacji w przeglądarce Firefox.

5. Narzędzie web-ext poprosi cię o zalogowanie się do konta Firefox Developer. Jeśli nie masz konta, musisz je utworzyć.

6. Postępuj zgodnie z instrukcjami na ekranie, aby zalogować się do konta Firefox Developer.

7. Wybierz profil, który chcesz użyć do podpisania dodatku. Jeśli nie masz jeszcze profilu podpisu, narzędzie web-ext automatycznie utworzy nowy profil dla ciebie.

8. Narzędzie web-ext przetworzy pliki rozszerzenia i wygeneruje podpisany plik XPI.

9. Po zakończeniu procesu narzędzie web-ext wyświetli informacje o podpisie i lokalizacji podpisanego pliku XPI.

10. Znajdź podpisany plik XPI w katalogu wynikowym i możesz go użyć do instalacji w przeglądarce Firefox.

11. Podpisywanie dodatków za pomocą narzędzia web-ext wykorzystuje konto Firefox Developer, co oznacza, że musisz mieć ważne konto, aby podpisać dodatek. Podpisywanie dodatków jest ważne, aby umożliwić ich instalację w przeglądarkach Firefox, które stosują restrykcje dotyczące podpisanych dodatków.
