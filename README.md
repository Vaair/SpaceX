# SpaceX
Тестовое задание: 
Разработать приложение справочник по компании SpaceX на основе открытого API https://github.com/r-spacex/SpaceX-API/tree/master/docs/ 

В приложении должно быть два экрана. 

На первом экране необходимо отобразить список миссий (https://api.spacexdata.com/v4/launches). 
Условия: 
- список должен работать с пагинацией (размер страницы 10 элементов) 
- загружать запуски с начала 2021 года (date_utc) 
- сортировка в порядке убывания по дате запуска (date_utc) 
- в ячейке необходимо показать: 
        - иконку миссии (links.patch.small) 
        - наименование (name) 
        - количество повторных использований первой ступени (cores.flight) 
        - статус миссии (success) 
        - дата запуска в формате ДД-ММ-ГГГГ 

По тапу на ячейку должен открывать второй экран. 

На втором экране необходимо показать детали миссии. 
Условия: 
- на странице показать: 
        - наименование миссии 
        - логотип (links.patch.large) 
        - количество повторных использований первой ступени (cores.flight) 
        - статус миссии (success) 
        - детали (details) 
        - дата и время миссии в формате ЧЧ-ММ ДД-ММ-ГГГГ 
        - список экипажа: ФИО, агенство, статус (https://api.spacexdata.com/v4/crew) 

Требования для iOS: 
- использовать Swift 
- минимальная поддерживаемая версия iOS 12 
- плюсом будет следование Human Interface Guidlines при разработке UI https://developer.apple.com/design/human-interface-guidelines/ios/overview/themes/ 
- использовать паттерн проектирования MVVM, плюсом будет реализация навигации на одельном паттерне (на выбор) 
- UI должен быть реализован в коде приложения с использованием autolayout, плюсом будет использование библиотеки Stevia Layout https://github.com/freshOS/Stevia 
- не использовать специализированные библиотеки для картинок 
- сетевой стек построить на Alamofire+Moya 
- плюсом будет использование RxSwift
