# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #5 выполнил(а):
- Уткин Никита Александрович
- РИ231113
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | * |
| Задание 2 | * | * |
| Задание 3 | * | * |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)


## Цель работы

Познакомиться с программными средствами для создания системы машинного обучения и ее интеграции в Unity.

## 1 Поиск агентом объекта на сцене

В созданной сцене по методичке шар начал двигаться.

![image](https://github.com/user-attachments/assets/056c4e0d-6c76-40e5-9917-7269019dda72)

![image](https://github.com/user-attachments/assets/79531627-afef-46fc-b96c-18872cbd6cf0)



После обучения на n = 3, 9, 27 моделях, результат в целом вышел удовлетворительный, он теперь понимал направление движения, но не всегда правильно работал, не могу сказать точно каким образом принимал решения.
## 2 Симулятор добычи ресурсов

Запустил проект, по методичке после действий начали работать, причем по сравнению с обученной в 1 задании моделью небо и земля, идеально, т.к. видимо модель там обучена очень сильно.

![image](https://github.com/user-attachments/assets/b992b49b-f63e-4479-af4e-1d0233b5b312)





## Задание 1. Найдите внутри C# скрипта “коэффициент корреляции” и сделать выводы о том, как он влияет на обучение модели

Ход работы:

public float forceMultiplier = 10;

rBody.AddForce(controlSignal * forceMultiplier);

Нашёл вот такой коэффициент, который контролирует силу, он даёт поправку для значений, не давая ей быть слишком маленькой и 1 -1.

## Задание 2. Изменить параметры файла yaml-агента и определить какие параметры и как влияют на обучение модели. Привести описание не менее трех параметров.
Ход работы:
- max_steps: 500000, - Максимальное кол-во шагов - очевидно чем выше значение - тем больше - тем лучше результат обучения.
  
- num_layers: 2, - Кол-во слоёв обучающей сети - увеличение числа увеличивает глубину обучения
  
- trainer_type: ppo, - это переменная определяющая какую модель обучения использует мл (с поддержкой)


## Задание 3. Приведите примеры, для каких игровых задачи и ситуаций могут использоваться примеры 1 и 2 с ML-Agent’ом. В каких случаях проще использовать ML-агент, а не писать программную реализацию решения?
Ход работы:
1) Можно использовать модель поиска объекта для наведения проджектайлов в играх, например представим игру типа touhou, в которой проджектайлы - это единственное о чем должен волноваться игрок. Он должен уворачиваться от них - таким образом подбив точность такой модели, немного уступая игроку в пространстве и скорости, можно использовать модель для управления такими частицами.

2) Вторую модель можно использовать в локациях, для поведения NPC, выполняющих функцию "оживления" сцены, или даже описывать катсцены, которые сейчас все рендерятся, с этой моделью. Или можно использовать можель для потенциальной игры, в которой игрок будет получать пути в зависимости от поведения NPC и\или влияния на него, то есть NPC будет создавать тропы открывающие новые возможности для игрока в зависимости от их решений

Суть в том, что можно использовать Модели для того чтобы описать процессы, которые будут влиять на игрока или игрок будет влиять на них, - контролируя параметры модели под ситуацию, думаю идея неплохая, да и скорее всего используется много где.


## Выводы

Изучил ML агента и интеграцию его в Юниити.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
