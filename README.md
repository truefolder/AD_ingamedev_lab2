# Анализ данных в разработке игр
Отчет по лабораторной работе #2 выполнил(а):
- Бабаев Тимур Ахмадалиевич
- РИ-220912
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | - |
| Задание 2 | * | - |
| Задание 3 | * | - |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1. Выберите одну из компьютерных игр, приведите скриншот её геймплея и краткое описание концепта игры. Выберите одну из игровых переменных в игре (ресурсы, внутри игровая валюта, здоровье персонажей и т.д.), опишите её роль в игре, условия изменения / появления и диапазон допустимых значений. Постройте схему экономической модели в игре и укажите место выбранного ресурса в ней.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.  С помощью скрипта на языке Python заполните google-таблицу данными, описывающими выбранную игровую переменную в выбранной игре (в качестве таких переменных может выступать игровая валюта, ресурсы, здоровье и т.д.). Средствами google-sheets визуализируйте данные в google-таблице (постройте график, диаграмму и пр.) для наглядного представления выбранной игровой величины.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3. Настройте на сцене Unity воспроизведение звуковых файлов, описывающих динамику изменения выбранной переменной. Например, если выбрано здоровье главного персонажа вы можете выводить сообщения, связанные с его состоянием.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Научиться передавать в Unity данные из Google Sheets с помощью Python.

## Задание 1
### Выберите одну из компьютерных игр, приведите скриншот её геймплея и краткое описание концепта игры. Выберите одну из игровых переменных в игре (ресурсы, внутри игровая валюта, здоровье персонажей и т.д.), опишите её роль в игре, условия изменения / появления и диапазон допустимых значений. Постройте схему экономической модели в игре и укажите место выбранного ресурса в ней.

Для анализа я выбрал игру Stardew Valley.

Краткое описание концепта игры: "Stardew Valley" - это фермерская симуляция, в которой игрок унаследовал заброшенную ферму и должен восстановить её, развивая сельское хозяйство, заводя скот, сажая культуры и взаимодействуя с жителями местного городка.

Выбранная игровая переменная: Внутриигровая валюта (золото).

Роль в игре: Золото в Stardew Valley играет ключевую роль. Оно используется для покупки семян, инструментов, строительства новых построек, улучшения фермы, покупки скота, и для оплаты услуг в городе. Золото также может быть использовано для покупки редких предметов и участия в различных событиях в игре.

Условия изменения / появления: Золото можно заработать, продавая сельскохозяйственные продукты, рыбу, руду, а также выполняя задания от местных жителей и участвуя в различных ивентах. Игрок также может получать золото от продажи ресурсов и продукции в лавке городка.

Диапазон допустимых значений: Золото в Stardew Valley задаётся числом и может колебаться от 0 до 99 999 999. Если игрок заработает более 99 999 999 золота, игра отнимет 100 000 000 золота у игрока.

Схема экономической модели в игре "Stardew Valley":

Источники золота: Золото появляется в игре через следующие источники:
- Продажа сельскохозяйственных продуктов (семена, урожай, молоко, яйца, рыба и др.).
- Продажа руды и драгоценных камней.
- Выполнение заданий от жителей городка.
- Участие в событиях и фестивалях.

Расходы золота: Золото используется для следующих целей:

- Покупка семян и товаров для фермы.
- Покупка строительных материалов для улучшения и расширения фермы.
- Покупка животных и построек для фермы.
- Покупка инструментов и оружия.
- Участие в различных мероприятиях и покупка украшений для фермы.

Взаимодействие с экономикой: Игрок может влиять на экономику игры, выбирая, какие культуры выращивать, какие товары производить, и когда продавать их, чтобы максимизировать прибыль и развитие фермы.

## Задание 2
### С помощью скрипта на языке Python заполните google-таблицу данными, описывающими выбранную игровую переменную в выбранной игре (в качестве таких переменных может выступать игровая валюта, ресурсы, здоровье и т.д.). Средствами google-sheets визуализируйте данные в google-таблице (постройте график, диаграмму и пр.) для наглядного представления выбранной игровой величины.
Немного модифицировав код из примера я заполняю гугл таблицу исходя из простейшей экономической стратегии - игрок со стартовым балансом в 500 золота тратит половину на закупку семян и вспомогательных предметов, затем собирает урожай и продаёт его, тем самым утраивая свой баланс.
```python
import gspread
import numpy as np
gc = gspread.service_account(filename='stalwart-edge-361617-65c49b91499f.json')
sh = gc.open("dawsdasdas")
money = 500
i = 0
iters = 60
while i <= 100:
    i += 1
    if i == 0:
        continue
    else:
        if i % 2 != 0:
            money /= 2
        else:
            money = money * 3
        sh.sheet1.update(('A' + str(i)), str(i))
        sh.sheet1.update(('B' + str(i)), str(money).replace('.', ','))
        print(money)
```

Визуализация результата:

![image](https://github.com/truefolder/AD_ingamedev_lab2/assets/89926388/dddde6bc-ec91-4050-904e-9ba49fdc3a5b)


## Задание 3
### Настройте на сцене Unity воспроизведение звуковых файлов, описывающих динамику изменения выбранной переменной. Например, если выбрано здоровье главного персонажа вы можете выводить сообщения, связанные с его состоянием.
Так как выбранная мною стратегия не учитывает огромное количество факторов и способов заработка золота в игре, она стабильно растёт и её значение лишь увеличивается.
В игре есть достижения за заработанное золото, поэтому я решил выводить сообщения каждый раз когда игрок разблокирует подобное достижение в игре.
```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.Networking;
using SimpleJSON;

public class NewBehaviourScript : MonoBehaviour
{
    public AudioClip goodSpeak;
    public AudioClip normalSpeak;
    public AudioClip badSpeak;
    private AudioSource selectAudio; 
    private Dictionary<string, float> dataSet = new Dictionary<string, float>();
    private bool statusStart = false;
    private bool achieved15000, achieved50000, achieved250000, achieved1000000, achieved10000000;
    private int i = 1;

    // Start is called before the first frame update
    void Start()
    {
        StartCoroutine(GoogleSheets());
    }

    // Update is called once per frame
    void Update()
    {
        if (dataSet["Mon_" + i.ToString()] >= 15000 & statusStart == false & !achieved15000 & i != dataSet.Count)
        {
            StartCoroutine(PlaySelectAudioBad());
            achieved15000 = true;
            Debug.Log("Получено достижение Новичок за заработанные 15000 золота");
        }

        if (dataSet["Mon_" + i.ToString()] >= 50000 & !achieved50000 & statusStart == false & i != dataSet.Count)
        {
            StartCoroutine(PlaySelectAudioBad());
            achieved50000 = true;
            Debug.Log("Получено достижение Ковбой за заработанные 50000 золота");
        }

        if (dataSet["Mon_" + i.ToString()] >= 250000 & !achieved250000 & statusStart == false & i != dataSet.Count)
        {
            StartCoroutine(PlaySelectAudioNormal());
            achieved250000 = true;
            Debug.Log("Получено достижение Поселенец за заработанные 250000 золота");
        }
        if (dataSet["Mon_" + i.ToString()] >= 1000000 & !achieved1000000 & statusStart == false & i != dataSet.Count)
        {
            StartCoroutine(PlaySelectAudioGood());
            achieved1000000 = true;
            Debug.Log("Получено достижение Миллионер за заработанные 1000000 золота");
        }
        if (dataSet["Mon_" + i.ToString()] >= 10000000 & !achieved10000000 & statusStart == false & i != dataSet.Count)
        {
            StartCoroutine(PlaySelectAudioGood());
            achieved10000000 = true;
            Debug.Log("Получено достижение Легенда за заработанные 10000000 золота");
        }
        if (statusStart == false)
            i++;
    }
    IEnumerator GoogleSheets()
    {
        UnityWebRequest curentResp = UnityWebRequest.Get("https://sheets.googleapis.com/v4/spreadsheets/1ZcWzlSQokcC1ytHvr2yjkVhAq-21RjS3HtkTFi-OkaA/values/Лист1?key=AIzaSyCmFKpI7Jp0IKUlBNMk_tTrkoSD4i5cmF4");
        yield return curentResp.SendWebRequest();
        string rawResp = curentResp.downloadHandler.text;
        var rawJson = JSON.Parse(rawResp);
        foreach (var itemRawJson in rawJson["values"])
        {
            var parseJson = JSON.Parse(itemRawJson.ToString());
            var selectRow = parseJson[0].AsStringList;
            dataSet.Add(("Mon_" + selectRow[0]), float.Parse(selectRow[1]));
        }
    }

    IEnumerator PlaySelectAudioGood()
    {
        statusStart = true;
        selectAudio = GetComponent<AudioSource>();
        selectAudio.clip = goodSpeak;
        selectAudio.Play();
        yield return new WaitForSeconds(3);
        statusStart = false;
    }
    IEnumerator PlaySelectAudioNormal()
    {
        statusStart = true;
        selectAudio = GetComponent<AudioSource>();
        selectAudio.clip = normalSpeak;
        selectAudio.Play();
        yield return new WaitForSeconds(3);
        statusStart = false;
    }
    IEnumerator PlaySelectAudioBad()
    {
        statusStart = true;
        selectAudio = GetComponent<AudioSource>();
        selectAudio.clip = badSpeak;
        selectAudio.Play();
        yield return new WaitForSeconds(4);
        statusStart = false;
    }
}

```

Вывод с консоли:

![image](https://github.com/truefolder/AD_ingamedev_lab2/assets/89926388/cd2c04ec-4035-4ebf-af0c-3672e4eb0c1e)

## Выводы
Я научился взаимодействовать с API гугл таблиц, научился взаимодействовать с данными с помощью API и читать их из Unity, разработал простейшую экономическую стратегию для игры которую я взял для анализа.

| Plugin | README |
| ------ | ------ |
| GitHub | [plugins/github/README.md][PlGh] |
| Visual Studio| [plugins/visualstudio/README.md][PlGh] |
| Unity | [plugins/unity/README.md][PlMe] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
