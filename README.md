# NeRF: Neural Radiance Fields

Celem dzisiejszych zajęć jest poznawanie modelu NeRF oraz zrozumienie jego działania. Oprócz tego zaprezentowane zostaną techniki pozwalające na przyspieszenie działania modelu oraz zwiększenie jego jakości. Cała część teoretyczna znajduję się w notebooku [NeRF.ipynb](NeRF.ipynb) i [fourier_feature_example.ipynb](fourier_feature_example.ipynb). Zadania praktyczne znajdują się w notebooku [exercises.ipynb](exercises.ipynb).

Aby skorzystać w pełni z tych zajęć polecamy iść według poniższej ścieżki:
1. Przeczytaj notebook [NeRF.ipynb](NeRF.ipynb), a następnie [fourier_feature_example.ipynb](fourier_feature_example.ipynb)
2. Wykonaj zadania z notebooka [exercises.ipynb](exercises.ipynb)
3. Uruchom NeRF na swoim komputerze

Repozytorium zawiera pliki:
- NeRF.ipynb -- zawiera on część teoretyczną wyjaśniającą jak działa NeRF oraz Furier Feature
- fourier_feature_example.ipynb -- plik pokazujący jak Furier Feature poprawia działanie sieci
- exercises.ipynb -- plik z praktycznymi zadaniami do zrobienia
- nerf_eval -- folder z kodem do uruchomienia NeRF wzięty z repozytorium [ailia-models [6]](https://github.com/axinc-ai/ailia-models/tree/master/neural_rendering/nerf)
- requirements.txt -- zestaw potrzebnych bibliotek do uruchomienia kodu.
- elza -- zbiór zdjęć Elzy potrzebny do notebooka exercises
- src -- zbiór materiałów audiowizualnych do notebooka NeRF

## Konfiguracja środowiska

W trakcie tych ćwiczeń będziemy korzystać z notatników Jupyter Notebook. Aby przygotować środowisko, należy zainstalować niezbędne biblioteki z pliku `requirements.txt`. Zaleca się przygotowanie wcześniej wirtualnego środowiska:

Propozycja jak można to zainstalować:

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

## Uruchomienie NeRF
Kod został wzięty z repozytorium [ailia-models [6]](https://github.com/axinc-ai/ailia-models/tree/master/neural_rendering/nerf) i został lekko przerobiony na potrzeby tych ćwiczeń. W celu uruchomienia NeRF należy wejść do folderu `nerf_eval` i uruchomić skrypt `nerf.py`. Model uruchamiany jest za pomocą ONNX Runtime.

Dla przykładowego obrazu, plik znajduje się w folderze w którym uruchamiamy skrypt.
``` bash
python nerf.py 
```

Kąt renderowania można ustawić za pomocą `--angle`. Zakres wynosi od 0 do 119.

``` bash
python nerf.py --angle 100
```

Współczynnik downsamplingu przyspieszający renderowanie, ustaw 4 lub 8 dla szybkiego podglądu. Domyślnie jest to 4.

``` bash
python nerf.py --render_factor 8
```

Architekturę modelu można podejrzeć na Netronie pod tym linkiem: https://netron.app/?url=https://storage.googleapis.com/ailia-models/nerf/nerf.opt.onnx.prototxt


## Źródła:

Repozytorium zostało stworzone na podstawie:<br/> 

[1] https://www.matthewtancik.com/nerf (20.12.2023) <br/>
[2] https://dl.acm.org/doi/pdf/10.1145/3503250 (20.12.2023) <br/>
[3] https://towardsdatascience.com/nerf-representing-scenes-as-neural-radiance-fields-for-view-synthesis-ef1e8cebace4 (20.12.2023) <br/>
[4] https://bmild.github.io/fourfeat/ (20.12.2023) <br/>
[5] https://arxiv.org/pdf/2003.08934.pdf (20.12.2023) <br/>
[6] https://github.com/axinc-ai/ailia-models/tree/master/neural_rendering/nerf (20.12.2023) <br/>
[7] https://github.com/ndahlquist/pytorch-fourier-feature-networks/blob/master/demo.ipynb (20.12.2023)
