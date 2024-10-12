# C++ Podstawy.

Type: Review
Favorite: No

# Jak zainstalować kompilator?

- Kompilator jest potrzeby aby nasze programy w c++ się uruchamiały, zainstalujemy sobie kompilator **G++**
- Pobieramy instalator z https://github.com/msys2/msys2-installer/releases/download/2024-01-13/msys2-x86_64-20240113.exe
- Następnie uruchamiamy go. Pojawia się takie okno:

![image.png](image.png)

Klikamy  **Next** lub **Dalej**

![image.png](image%201.png)

Możemy zostawić **domyślny folder instalacji** następnie przechodzimy dalej.

![image.png](image%202.png)

Nic nie zmieniamy tutaj zostawiamy to i idziemy dalej.

![image.png](image%203.png)

Rozpocznie się instalacja kompilatora. Po zakończeniu klikamy dalej i gdy zobaczymy taki ekran.

 

![image.png](image%204.png)

Klikamy finish i kompilator jest praktycznie gotowy do użycia!

![image.png](image%205.png)

Otwiera się powysze okno wklejamy w nie:

```bash
pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain

```

![image.png](image%206.png)

Wyskakuje nam coś takiego klikamy ENTER.

![image.png](image%207.png)

Tutaj też potwierdzamy enterem. Czekamy na pełną instalacje. Pobieranie może trochę zająć max do 5 minut przy tragicznym internecie.

![image.png](image%208.png)

Coś podobnego pojawi się po poprawnej instalacji.

Musimy jeszcze dodać kompilator do zmiennej środowiskowej w pasku wyszukiwania systemu wpisujemy frazę: “zmienne środowiskowe” i wybieramy opcję z panelu sterowania ja mam po angielsku i u  mnie wygląda to tak:

![image.png](image%209.png)

Po otworzeniu się okna klikamy przycisk “zmienne środowiskowe”:

![image.png](image%2010.png)

Wybieramy zmienne systemowe “PATH” u mnie jest tego dużo więc musze przescroolować

![image.png](image%2011.png)

![image.png](image%2012.png)

Zaznaczamy path i klikamy EDIT (lub edytuj)

Wybieramy new lub nowa w nowo otwarym oknie i wpisujemy

![image.png](image%2013.png)

W polu tekstowym przy domyslnej instalacji wpisujemy
`C:\msys64\ucrt64\bin`

![image.png](image%2014.png)

Zatwierdzamy we wszystkich oknach klikając “OK” i zamykamy 1 okno.

Teraz mamy kompilator gotowy do użycia!

# Testowanie kompilatora i pierwszy program

- Uruchamiamy visual studio code, otwieramy nowy folder i tworzymy w nim plik o nazwie np: “test.cpp”.

```cpp
#include <iostream>

int main() {
    std::cout << "witaj swiecie!";
}
```

Umieszczamy w nim powyższą treść i klikamy F5. 

Vsc poprosi nas o wybranie debugera:

![image.png](image%2015.png)

Wybieramy 1 opcje (C++ (GDB/LLDB)

Następnie

![image.png](image%2016.png)

Wybieramy kompilator G++.

W zakładce terminal powinno po chwili pojawić się to:

![image.png](image%2017.png)

Jeśli widzimy napis witaj w świecie to jesteśmy gotowi do programowania w c++!
