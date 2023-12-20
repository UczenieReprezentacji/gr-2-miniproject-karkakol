# NeRF: Neural Radiance Fields

Celem dzisiejszych zajęć jest poznawanie modelu NeRF oraz zrozumienie jego działania. Oprócz tego zaprezentowane zostaną techniki pozwalające na przyspieszenie działania modelu oraz zwiększenie jego jakości. Cała część teoretyczna znajduję się w notebooku [NeRF.ipynb](NeRF.ipynb). Zadania praktyczne znajdują się w notebooku [exercises.ipynb](exercises.ipynb).

Repozytorium zawiera pliki:
- NeRF.ipynb -- zawiera on część teoretyczną wyjaśniającą jak działa NeRF oraz Furier Feature
- fourier_feature_example.ipynb -- przerobiony notebook z publikacji [1] który pokaże użyteczność Furier Feature
- exercises.py -- plik z praktycznymi zadaniami do zrobienia
- requirements.txt -- zestaw potrzebnych bibliotek do uruchomienia kodu.
- elza -- zbiór zdjęć elzy potrzebny do notebooka exercises
- src -- zbiór materiałów audiowizualnych do notebooka NeRF

## Konfiguracja środowiska

Proszę o szczegółowy opis, jak powinno zostać skonfigurowane środowisko. Dla chętnych - można używać Dockera (nie jest to wymagane). Kod musi być reproduktywny. Należy zaznaczyć jaka wersja Pythona jest używana. Wszystkie wymagane paczki muszą mieć zaznaczoną wersję.

Przykład:

W trakcie tych ćwiczeń będziemy korzystać z notatników Jupyter Notebook. Aby przygotować środowisko, należy zainstalować niezbędne biblioteki z pliku `requirements.txt`. Zaleca się przygotowanie wcześniej wirtualnego środowiska:

Stwórz środowisko za pomocą `venv`:
```bash
$ python3.11 -m venv .venv
```
lub z użyciem `conda`:
```bash
$ conda create -n .venv python=3.11.5
```

zainstaluj niezbędne biblioteki:
```bash
$ source .venv/bin/activate
$ pip install -r requirements.txt
```


## Źródła:

Repozytorium zostało stworzone na podstawie:<br/> 

[1] https://www.matthewtancik.com/nerf (20.12.2023) <br/>
[2] https://dl.acm.org/doi/pdf/10.1145/3503250 (20.12.2023) <br/>
[3] https://towardsdatascience.com/nerf-representing-scenes-as-neural-radiance-fields-for-view-synthesis-ef1e8cebace4 (20.12.2023) <br/>
[4] https://bmild.github.io/fourfeat/ (20.12.2023) <br/>
[5] https://arxiv.org/pdf/2003.08934.pdf (20.12.2023) <br/>
