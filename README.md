# kws_project
Key Word Spotting
Project for DLA course at HSE

## Project structure
* `data/` contains train/val split on which I trained and evaluated.
* `models/` contains checkpoints that achieved adequate quality
* `main.ipynb` is where main work happened
* `report.pdf` is self-naming

## Main result
`models/student_08.pt` achieved 8.5-fold speedup and 10-fold memory reduction compared to baseline model (`models/baseline_best.pt`). Its quality (`5.3e-5`) is still adequate and satisfies the constraint (`< 5.5e-5`)

I tried following setups:
* Distillation (around 10 times)
* Quantization (qint8)
* Quantization (float16)
* Distillation + Quantization (qint8)

## Installation
Everything needed is in notebook, however you need to download data split and models so that it lies near notebook; for example in notebook you could use
```bash
!git clone https://github.com/ShamerD/kws_project.git
!mv kws_project/data/* .
!mv kws_project/models/* .
```
