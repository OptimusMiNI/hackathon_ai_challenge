<h1>Sztuczna Inteligencja w Tworzeniu Dokumentacji</h1>

![Untitled (1)](https://github.com/OptimusMiNI/hackathon_ai_challenge/assets/110894357/ae85bb58-0f1a-4666-9dd7-11c552dd15b6)
Robimy parsing kodu i tworzymy drzewa w całym projekcie.
Następnie idziemy przez cały kod zaczynając od najgłębszych funkcji za pomocą drzew i rekurencyjnie wrzucamy kod do modelu code-t5+.
Otrzymujemy opisy funkcji i wrzucamy dalej ich dalej jako komentarze do następnej części kodu.

Drzewa robimy za pomocą <a href='https://tree-sitter.github.io/tree-sitter/'>tree-sitter</a>:
<br>
![Screenshot from 2023-12-10 10-57-02](https://github.com/OptimusMiNI/hackathon_ai_challenge/assets/110894357/9fa99d52-8723-408c-99dc-36ab32a84f66)
<br>

Przykład:
![ezgif com-gif-maker (2)](https://github.com/OptimusMiNI/hackathon_ai_challenge/assets/110894357/c811987b-ffbc-46d4-b735-11853f14a44f)

Następnie tworzymy plik na podstawie otrzymanych opisów wszystkich funkcji i części kodu otrzymanych z modelu code-t5+. Opcjonalnie tworzymy plik docs.config, który będzie opisywał ogólną strukturę naszego projektu.  Za pomocą tej konfiguracji sztuczna inteligencja będzie w stanie lepiej zrozumieć nasz projekt, będzie mogła zobaczyć strukturę modułów, wcześniejsze zatwierdzenia i tak dalej.
Przykład:
![Screenshot from 2023-12-10 12-37-12](https://github.com/OptimusMiNI/hackathon_ai_challenge/assets/110894357/26f244fc-f2c2-4602-bfaa-f7ae05a5fb8e)
...

Po tym wszystkim wysyłamy nasz plik i plik konfiguracyjny do czatu gpt, który pisze nam dużą szczegółową dokumentację na podstawie całego projektu (możesz wybrać rodzaj dokumentacji: dokumentacja dla programisty, dokumentacja dla klienta i tak dalej. .).  Dodać należy, że konieczne jest także opracowanie odpowiednich promptów, na podstawie których sztuczna inteligencja będzie tworzyć dokumentację.

Możliwa jest także automatyczna aktualizacja dokumentacji, wykonując te same czynności.



Dlaczego wybraliśmy model code-t-5+?
Bo jest najlepszym modelem dla kodu:
![image](https://github.com/OptimusMiNI/hackathon_ai_challenge/assets/110894357/3b4cf4a0-3f91-4d62-a972-57a965ab847f)


Mając dobrą dokumentację można szukać błędów w kodzie, szukać potrzebnych fragmentów kodu i w ogóle dużo łatwiej jest zrozumieć cały kod.



Yahor Lahunovich <br>
Maksim Razantsau <br>
Yauheni Butsialevich
