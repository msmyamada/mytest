---
description: Соответствие сочетаний клавиш для кода Visual Studio, Эмуляция Surface Duo и Samsung Galaxy сгиб, улучшения каскадных таблиц стилей и т. д.
title: Новые возможности DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 943eca7e73385513b264feb74ec37c450d5c5a2f
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004228"
---
# Новые возможности DevTools (Microsoft Edge 86)  

## Объявления из группы Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### Соответствие сочетаний клавиш в DevTools с кодом Visual Studio  

В Microsoft Edge 86 вы можете использовать сочетания клавиш в DevTools для сочетаний клавиш в [коде Visual Studio][VisualStudioCode]. 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Соответствие сочетаний клавиш в DevTools с кодом Visual Studio  
:::image-end:::  

Для активации этой функции перейдите в [раздел Настройка сочетаний клавиш в Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  

Например, с помощью сочетания клавиш можно приостановить или продолжить выполнение сценария в [Visual Studio][VisualStudioCodeShortcutsKeyboardWindows] `F5` .  В стиле **DevTools (по умолчанию)** это тот же ярлык в DevTools `F8` , но если вы выбрали стиль **кода Visual Studio** , это сочетание клавиш также будет использоваться `F5` .  

[#174309][CR174309] проблем с Chromium  

### Эмуляция Surface Duo и Samsung Galaxy сгиб  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio":::
   Экспериментальная функция  
:::image-end:::  

Теперь вы можете проверить внешний вид и функции вашего веб-сайта или приложения на двух новых устройствах:  [Surface Duo][MicrosoftSurfaceDevicesDuo] и [Samsung Galaxy сгиб][SamsungMobileGalaxyFold] в Microsoft Edge.  

Чтобы повысить качество веб-сайта или приложения для двойного экрана и складная устройств, используйте следующие возможности при [эмуляции устройства][DevtoolsDeviceModeIndex].  

*   [Объединение][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], которое появляется, когда ваш веб-сайт (или приложение \) отображается на обоих экранах.
*   [Отрисовка стыка][DualScreenIntroductionHowWorkSeam], то есть расстояния между двумя экранами.
*   [Включение API экспериментальной веб-платформы][DevtoolsExperimentalFeaturesEnableExperimentalApis] для доступа к новой [функции многофункционального экрана CSS][DualScreenWebCssMediaSpanning] и [API JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Эмуляция устройства для ИБП Surface Duo  
:::image-end:::  

Чтобы включить эту функцию, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок рядом с параметром **Эмуляция: поддержка двух режимов экрана**.  

Дополнительные сведения об этом эксперименте можно найти в разделе [Эмуляция: поддержка двух режимов экрана][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].  

Ошибка Chromium: [#1054281][CR1054281]  

### Усовершенствования каскадных наложений сетки CSS и новые возможности экспериментальной сетки  

Благодарим вас за позитивную обратную связь об улучшенных наложения сетки CSS.  Наложения сетки CSS теперь включены по умолчанию и не требуют включения эксперимента.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Наложение сетки CSS для `article` элемента  
:::image-end:::  

> [!NOTE]
> Дополнительные сведения о наложении сетки можно найти в статьях [функции отладки сетки каскадных стилей][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].  

Группа Microsoft Edge DevTools и группа "Chrome DevTools" совместно работают с дополнительными функциями.  Новые возможности включают в себя несколько наложений, которые сохраняются и настраиваются в новой области **макета** на панели " **элементы** ".  

Чтобы включить эту функцию, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок **включить новые функции отладки сетки CSS (параметры конфигурации, доступные в области Макет в элементах после перезапуска)**.  

Чтобы получить дополнительные сведения об этом эксперименте, перейдите к разделу [Включение новых функций отладки сетки каскадных стилей][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].  

Ошибка Chromium: [#1047356][CR1047356]  

### Таблица, скопированная из консоли сохраняет форматирование  

В Microsoft Edge 85 или более ранней версии форматирование скопированных данных `console.table` было разорвано.  При копировании результатов из API консоли [таблицы][DevtoolsConsoleApiTable] и вставке в нее сохраняется только текст таблицы.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Выходные данные API консоли в Microsoft Edge 85 или более ранней версии  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Выходные данные API консоли из Microsoft Edge 85 или более ранней версии, вставленные в код Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

В Microsoft Edge 86 или более поздней версии при копировании таблицы с **консоли**форматирование будет сохранено.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Выходные данные API консоли в Microsoft Edge 86 или более поздней версии  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Выходные данные API консоли из Microsoft Edge 86 или более поздней версии, вставленные в код Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Ошибка Chromium: [#1115011] [CR1115011]  

### Средство просмотра заказов исходного кода для упрощения тестирования специальных возможностей  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio":::
   Экспериментальная функция  
:::image-end:::  

Новый вспомогательный модуль специальных возможностей отображает порядок элементов в источнике.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Активация **порядка отображения исходного кода**  
:::image-end:::  

Эта функция упрощает тестирование того, как пользователи с помощью средства чтения с экрана и клавиатуры смогут работать на веб-сайте или в приложении.  Средства чтения с экрана и навигация с помощью клавиатуры зависят от содержимого, которое размещается в определенном порядке в исходном коде вашего веб-сайта или приложения, чтобы оно соответствовало отображаемой странице.  В средстве просмотра исходного порядка отображаются потенциальные отличия между обработанной страницей и исходным кодом.  

Чтобы включить эту функцию экспериментальных, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок **включить средство просмотра заказов исходным кодом**.  

Чтобы получить дополнительные сведения об этом эксперименте, перейдите в раздел [Включение средства просмотра заказов исходного кода][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].  

Ошибка Chromium: [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### Инструмент "выделение всех результатов поиска" в элементах  

В Microsoft Edge 84 и 85 первый результат поиска на панели **элементов** не выделяются.  Оставшиеся результаты поиска выделены правильно.  

Благодарим вас за отправку отзыва и помощь в улучшении Chromium.  В проекте Chromium Open-Source возникла ошибка, связанная с [не#1103316ой][CR1103316] отзыва.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Выделенный первый результат поиска на панели " **элементы** " в Microsoft Edge 84 или более поздней версии  
:::image-end:::  

Теперь проблема устранена во всех версиях Microsoft Edge.  

Ошибка Chromium: [#1103316][CR1103316]  

## Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Новая панель мультимедиа  

DevTools теперь отображает сведения о проигрывателях мультимедиа на панели " [мультимедиа][DevtoolsMediaIndex] ".  

Чтобы открыть новую панель **мультимедиа** , выполните указанные ниже действия.  

1.  Нажмите кнопку **Настройка и выберите DevTools** \ ( `...` \) > **другие инструменты**  >  **мультимедиа**.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/media-panel.msft.png":::
       Новая панель **мультимедиа**  
    :::image-end:::  

Перед новой панелью **мультимедиа** в DevTools сведения о регистрации и отладке видеопроигрывателей находятся в разделе " **последние игрока** ".  Чтобы открыть параметр " **недавние игрока** ", перейдите на `edge://media-internals` вкладку **игрока** и щелкните ее.  

Просматривайте содержимое в реальном времени и отучите возможные проблемы быстрее, в том числе в следующих примерах.  

*   Почему кадры удаляются?  
*   Почему JavaScript взаимодействует с проигрывателем непредсказуемым образом?  

### Захват снимков узлов с помощью контекстного меню панели элементов  

Теперь вы можете захватывать снимки узлов с помощью контекстного меню на панели " **элементы** ".  

Например, чтобы сделать снимок экрана оглавлением, наведите на него указатель мыши, откройте контекстное меню, а затем выберите пункт **захватить снимок экрана узла**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Снимок экрана захвата узлов  
:::image-end:::  

Ошибка Chromium: [#1100253][CR1100253]  

### Обновления средства устранения проблем  

Панель предупреждения "проблемы" на панели **консоли** теперь заменяется обычным сообщением.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Проблемы в сообщении консоли  
:::image-end:::  

Сторонние файлы cookie теперь по умолчанию скрыты в инструменте " **вопросы** ".  Чтобы просмотреть список проблем, установите флажок **Включить сторонние файлы cookie** .  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   флажок "вопросы и сторонние файлы cookie"  
:::image-end:::  

Проблемы с Chromium: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### Эмуляция отсутствующих локальных шрифтов  

Откройте [средство подготовки][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] и воспользуйтесь новым компонентом **Отключить локальные шрифты** для эмуляции отсутствующих `local()` источников в `@font-face` правилах.  

Например, если `Rubik` шрифт установлен на устройстве, а `@font-face src` правило использует его в качестве `local()` шрифта, Microsoft Edge использует локальный файл шрифта на устройстве.  

При включении функции **Отключить локальные шрифты** DevTools игнорирует `local()` шрифты и извлекает их из сети.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/disable-font.msft.png":::
   Эмуляция отсутствующих локальных шрифтов  
:::image-end:::  

При использовании двух разных копий одного и того же шрифта в процессе разработки (например, в приведенных ниже примерах).  

*   Локальный шрифт для средств разработки.  
*   Веб-шрифт для вашего кода.  

Используйте **функцию отключить локальные шрифты** , чтобы упростить выполнение описанных ниже задач.  

*   Отладка и оценка скорости загрузки и оптимизации веб-шрифтов.  
*   Проверьте точность `@font-face` правил CSS.  
*   Обнаружение различий между локальными версиями, установленными на устройстве, и веб-шрифтом.  

Ошибка Chromium: [#384968][CR384968]  

### Эмуляция неактивных пользователей  

[API обнаружения простоя][WebDevIdleDetection] позволяет разработчикам обнаруживать неактивные пользователи и реагировать на изменения состояния простоя.  Теперь вы можете использовать DevTools для эмуляции изменений состояния простоя в инструменте " **датчики** " и для состояния пользователя, и для состояния экрана вместо того, чтобы ждать изменения фактического состояния простоя.  Вы можете открыть инструмент **Sensors (датчики** ) из [ящика][DevtoolsCustomizeIndexDrawer].  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Эмуляция неактивных пользователей  
:::image-end:::  

Ошибка Chromium: [#1090802][CR1090802]  

### Предпочтительные эмуляции — сокращенные данные  

> [!NOTE]
> Чтобы включить эту функцию в Microsoft Edge 86, перейдите на вкладку `edge://flags#enable-experimental-web-platform-features` **экспериментальные веб-платформа** и включите этот флажок.  Параметр эмуляции отображается только в том случае, если включен флаг.  

Запрос " [предпочтительный"-][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] "мультимедиа" — это обнаружение параметров содержимого пользователя для уменьшения объема данных.  Если этот флажок установлен, пользователь получает содержимое страницы, которое использует меньшие данные.  

Теперь вы можете использовать DevTools для эмуляции `prefers-reduced-data` запроса мультимедиа.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Предпочтительные эмуляции — сокращенные данные  
:::image-end:::  

Ошибка Chromium: [#1096068][CR1096068]  

### Поддержка новых функций JavaScript  

DevTools теперь обладают улучшенными возможностями поддержки следующих функций языка JavaScript.  

| Функция языка JavaScript | Сведения |  
|:--- |:--- |  
| [Логические операторы присваивания][V8FeaturesLogicalAssignment] | DevTools теперь поддерживает логическое назначение с помощью новых операторов "" "" " `&&=` `||=` и" `??=` "" на панели " **консоль** " и " **источники** ".  |  
| Некачественная печать [числовых разделителей][V8FeaturesNumericSeparators] | Теперь DevTools правильно — печатает на панели « **источники** » числовые разделители.  |  

Проблемы с Chromium: [1086817][CR1086817], [1080569][CR1080569]  

### Lighthouse 6,2 на панели Lighthouse  

Панель **Lighthouse** теперь работает под управлением Lighthouse 6,2.  Полный список изменений можно найти в [заметках о выпуске Lighthouse][GithubGooglechromeLighthouseV620].  

Ошибка Chromium: [#772558][CR772558]  

### Устаревшие сведения о других источниках, перечисленные в области "работники службы"  

DevTools теперь предоставляет ссылку из области "работа с **сотрудниками** \" (панель**приложения** > область " **сотрудники** "), чтобы просмотреть полный список работников служб из других источников.  Чтобы получить доступ к списку, не открывая DevTools, перейдите на `edge://service-worker-internals/?devtools` .  

Ранее DevTools отображал список, вложенный в панель **приложения** , > области "работа с **сотрудниками службы** ".  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Ссылка на другие источники  
:::image-end:::  

Ошибка Chromium: [#807440][CR807440]  

### Отображение сводки о покрытии для отфильтрованных элементов  

DevTools сейчас пересчитайте и отобразите сводную информацию о покрытии динамическими.  Динамическое отображение инициируется, когда фильтры применяются в инструменте [Coverage][DevtoolsCoverageIndex] .  Перед тем, как средство **покрытия** всегда выводит сводку по всем сведениям о покрытии.  

На первой из приведенных ниже рисунков сводка первоначально отображается `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` и на второй из приведенных ниже рисунков показывается, `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` когда будет применена фильтрация CSS.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Сводка о покрытии  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Сводка покрытия для отфильтрованных элементов  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Ошибка Chromium: [#1061385][CR1090802]  

### Новый вид сведений о кадре на панели приложения  

DevTools теперь показывать подробное представление для каждого кадра.  Для доступа к нему выберите рамку в меню " **кадры** " на панели **приложения** .  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/frame-details.msft.png":::
   Новый подробный вид рамки на панели **приложения**  
:::image-end:::  

Ошибка Chromium: [#1093247][CR1093247]  

#### Сведения о кадре для открытых окон  

Теперь в дереве фреймов отображаются открытые окна и всплывающие окна.  Подробное представление открытых окон включает дополнительные сведения о безопасности.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/window-opener.msft.png":::
   Подробный обзор нового кадра для открытых окон  
:::image-end:::  

Ошибка Chromium: [#1107766] [CR1107766]  

#### Сведения о безопасности и изоляции  

В разделе сведения о кадре отображаются безопасный контекст, [Политика встраивания с Межисточниками (COEP)][WebDevCoopCoep], а также меж- [Openerная политика (Coop)][WebDevCoopCoep] .  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Сведения о безопасности и изоляции  
:::image-end:::  

В будущем группа Microsoft Edge DevTools и группа Chrome DevTools планирует добавить дополнительные сведения о безопасности в сведения о кадре.  

Ошибка Chromium: [#1051466][CR1051466]  

### Элементы и обновления панели сети  

#### Специальные возможности цвета в области "стили"  

DevTools теперь предлагает варианты цветов для текста с низким контрастом цвета.  

В примере ниже `h1` есть текст с низким контрастом.  Чтобы исправить ошибку, откройте окно выбора цвета `color` свойства в области **стили** .  После того как вы развернете раздел **коэффициент контрастности** , DevTools предоставляет варианты цветов AA и AAA.  Выберите предложенный цвет, чтобы применить его.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   Средство выбора цвета предлагает варианты цветов AA и AAA  
:::image-end:::  

Ошибка Chromium: [#1093227][CR1093227]  

#### Область "восстановить свойства" на панели "элементы"  

Область **свойств** будет возвращена.  Она была [признана устаревшей в Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  Группа Microsoft Edge DevTools и группа "Chrome DevTools" предназначены для планирования улучшений для проверки свойств элементов.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/properties-pane.msft.png":::
   Область " **Свойства** " на панели " **элементы** "  
:::image-end:::  

Ошибка Chromium:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### Автозаполнение настраиваемых шрифтов в области "стили"  

Импортированные фрагменты шрифта теперь добавляются в список автозавершения CSS при редактировании `font-family` свойства в области **стили** .  

Например, если `monospace` на локальном компьютере установлен настраиваемый шрифт, он отображается в списке завершения CSS. В предыдущих версиях Microsoft Edge шрифт не отображался.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Автозаполнение настраиваемых шрифтов  
:::image-end:::  

Ошибка Chromium: [#1106221] [CR1106221]  

#### Согласованное отображение типа ресурсов на панели "сеть"  

DevTools теперь будет отображать тот же тип ресурса, что и исходный, и добавляет `/ Redirect` к значению столбца **Type** , когда происходит перенаправление \ (код состояния HTTP 302 \).  

Ранее DevTools изменил тип на " `Other` иногда".  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Вывод типа ресурса перенаправления  
:::image-end:::  

Ошибка Chromium: [#997694][CR997694]  

#### Кнопки "очистить" на панелях "элементы" и "сеть"  

В следующих текстовых полях теперь есть кнопки " **очистить** ".  

*   Текстовые поля "фильтр" в области " **стили** " и на панели " **сеть** ".  
*   Текстовое поле "Поиск DOM" на панели " **элементы** ".  

Нажмите кнопку **очистить** , чтобы удалить введенный текст.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Кнопки "очистить" на панелях **элементов**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Кнопки "очистить" на панели "  **сеть** "  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Ошибка Chromium: [#1067184][CR1067184]  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge DevTools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Значок параметров DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Устаревшая область свойств на панели "элементы" — новые возможности DevTools (Microsoft Edge 84) | Документы Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS: новые возможности DevTools (Microsoft Edge 85) | Документы Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка сочетаний клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включите экспериментальные API — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка двух режимов экрана — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Включение средства просмотра заказов на исходный номер — экспериментальные функции | Документы Microsoft"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Эмуляция: поддержка двух режимов экрана — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на складная и устройствах с двумя экранами — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включите экспериментальные функции — экспериментальные функции | Документы Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Справочник по API для консоли "Таблица" | Документы Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг" — Справка по анализу производительности | Документы Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Просмотр и отладка сведений о проигрывателях мультимедиа | Документы Microsoft"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Работа с стыками — введение в работу с устройствами с двумя экранами | Документы Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Функция многоэкранной группировки с экрана в каскадных таблицах CSS | Документы Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API getWindowSegments JavaScript для устройств с двумя экранами | Документы Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительной версии Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Код Visual Studio "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новая поверхность Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: разрешение на настройку сочетаний клавиш и привязок клавиш | Ошибки Chromium"
[CR384968]: https://crbug.com/384968 "Параметр, позволяющий игнорировать локальные шрифты () | Ошибки Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии Lighthouse | Ошибки Chromium"  
[CR807440]: https://crbug.com/807440 "Блокировка хрома с большим количеством SWs | Ошибки Chromium"  
[CR997694]: https://crbug.com/997694 "Запросы XHR с состоянием 302 не отображаются в разделе \ "XHR \" на панели "сеть" | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "Инструменты сетки/гибкого бокса или таблицы CSS"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1054281]: https://crbug.com/1054281 "Запрос функции: DevTools должен эмулировать складная и устройства с двумя экранами | Ошибки Chromium"  
[CR1067184]: https://crbug.com/1067184 "Запрос компонента: очистить кнопку "фильтр" в элементах & сети — > фильтрах фильтров | Ошибки Chromium"  
[CR1068116]: https://crbug.com/1068116 "☂ "Доставка проблем" | Ошибки Chromium"  
[CR1080569]: https://crbug.com/1080569 "Acorn не поддерживает логические операторы присваивания | Ошибки Chromium"  
[CR1080589]: https://crbug.com/1080589 "Классификация проблем сторонним лицом или первым абонентом | Ошибки Chromium"  
[CR1086817]: https://crbug.com/1086817 "Acorn не поддерживает цифровые разделители | Ошибки Chromium"  
[CR1090802]: https://crbug.com/1090802 "Имитация изменений состояния простоя из API обнаружения в режиме ожидания | Ошибки Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools: Предложите наиболее близкий доступный цвет | Ошибки Chromium"  
[CR1093247]: https://crbug.com/1093247 "Вывод сведений о кадрах на панели приложения | Ошибки Chromium"  
[CR1094406]: https://crbug.com/1094406 "Разработчикам требуется средство просмотра заказов исходного кода на https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: поддерживает эмуляцию предпочтительных возможностей мультимедиа с данными Ошибки Chromium"  
[CR1096481]: https://crbug.com/1096481 "Расположение заголовков вопросов | Ошибки Chromium"  
[CR1100253]: https://crbug.com/1100253 "Клавиша "добавить узел снимка экрана" в контекстном меню элемента | Ошибки Chromium"  
[CR1103316]: https://crbug.com/1103316 "Поиск элементов не resolveNode (выделит текст и т. д.) при первом результатах поиска | Ошибки Chromium"  
[CR1103854]: https://crbug.com/1103854 "Отмена запутывания X-Client-значения данных в средствах разработчика | Ошибки Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "Добавить импортированные шрифты в Автозаполнение" семейство шрифтов "на панели" стили | "| Chromium ошибки "  
[CR1107766]: https://crbug.com/1107766 "Показать сведения о кадрах, созданных с помощью" Window. Open () "в дереве кадров | Chromium ошибки "  
[CR1115011]: https://crbug.com/1115011 "при копировании таблицы из консоли структура таблицы не сохраняется | Chromium ошибки "  
[CR1116085]: https://crbug.com/1116085 "Пожалуйста, вернитесь в инспектор свойств DevTools | Chromium ошибки "  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "предпочитать количество запросов мультимедиа на уровне 5 | Черновики редакторов рабочих групп W3C CSS"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/Lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Буферы протоколов | Разработчики Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy, сгиб | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Логическое назначение | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Число разделителей | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Создание изолированного веб-сайта \ "межисточник \" с помощью COOP и COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Обнаружение неактивных пользователей с помощью API обнаружения бездействия | Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Предотвращение несложных анимаций | Web. dev"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/08/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
