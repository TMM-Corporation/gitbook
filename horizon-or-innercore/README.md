---
description: 'Тут публикуются овтеты на вопросы, связанные с InnerCore / Horizon'
---

# Horizon \| InnerCore

## How to install / remove a pack?

To install the pack, click the large + button and select the pack you are interested in.

To delete an already downloaded/not installed pack, you need to click on the park and a context menu will open, which has the following content:

* Add to favorites - mark as a favorite pack
* Clone - duplicates the pack completely with all worlds and mods
* Reinstall - completely reinstalls the package from the cache with the data saved
* Reinstall - completely reinstalls the package from the cache with the data saved
* Show information - opens a dialog box with information about the package, such as:
  * Title - The full name of the pack
  * Pack Description
  * Game - What game was created for
  * Version - The version of the current pack and the latest available version
  * State - pack status
    * Installed - pack is already installed
    * Pending - expected download and installation
    * NOT\_INSTALLED - not downloaded and not installed
  * Local directory -path to the pack from /sdcard/games/horizon/packs
  * External UUID - UUID of pack
  * Show change history button - opens the full change history
* Delete - completely deletes all pack data, including measures, resource packs, mods, etc.

## How to use the InnerCore pack?

There are 5 buttons in the main pack menu:

1. **Play** - the button in the center that starts the game
2. **Native mods** - button on the right side of the menu, manager of active mods for the game
3. **Mod manager** - your browser mods for the game
   1. Download mods - a tab where you can download any mods for the game
   2. My mods - tab of your installed mods
   3. Mod packs - ready-made modpack that are created by developers
   4. Updates - список модов у которых есть обновления
   5. Visit Website - opens a full-fledged site of mods for the game
4. **Settings and Links**
   1. InnerCore Pack Settings
      1. **Отключить экран загрузки** - отображение экрана загрузки модов, при включении на некоторых устройствах может ускорить загрузку
      2. **Режим разработчика** - полезно для создателей модов, включает в поддерживаемых модах режим отладки.
      3. **Ограничение обновлений по вермени** - количество обновлений модов в тик будет ограничено временем выполнения, иначе количеством обновленных объектов. Проще говоря сколько вызовов в тик могут делать моды.
      4. **Максимум обновлений в тик** - поднастройка _ограничения по времени_
      5. **Расширенные настройки приоритета потока** - более высокий приоритет серверного потока стабилизирует количество тиков в секудну TPS \(это означает более стабильную работу и время ответа\), однако это может вызывать фризы и просадку кадров в секуднку FPS
      6. **Приоритет серверного потока** - поднастройка _расширенной настройки приоритета потока_
      7. **Пороговый FPS** - пока FPS ниже этого порога, серверный поток будет работать на нижнем приоритете, иначе будет установлен верхний приоритет
      8. **Количество дополнительных потоков** - дополнительные потоки являются эксперементальной настройкой. На мощных устройствах может улучшить производительность при болшой нагрузке.
      9. **Приоритет дополнительных потоков** - поднастройка _количества дополнительных потоков._
      10. **Автосохранение** - позволяет сохранить данные мира и модов, если игра может резко завершить работу или некорректно
      11. **Период автосохранения** - время в секундах между запусками _автосохранения_
      12. **Включить Сокет-Сервер** - позволяет игрокам в локальной сети подключаться к вашему миру с использованием сокетов
      13. **Использовать нативный протокол** - выполнять подключение по нативному протоколу \(по умолчанию больший приоритет у протокола на основе _сокетов_\)
      14. **Форсировать Локальный Нативный Протокол** - _**для разработчиков!**_ Использовать нативный протокол для связи между локальным клиентом и сервером. Эта настройка нужна только для отладки модов и движка, **не используйте её для игры!**
   2. Гайды и ссылки - вкладка с ссылками и гайдами
   3. Благодарности - вкладка благодарностей разработчикам, тестировщикам, разработчикам модов
   4. О приложении

## Чем отличаются паки IC \| IC Test \| IC Legacy ?

**InnerCore** - _обычный_ пак, более стабильный и имеет последнюю версию Minecraft BE 1.16.201

**InnerCore Test** - это _тестовый_ пак имеет эксперементальные возможности. Более нестабилен. Имеет последнюю версию MCBE 1.16.201

**InnerCore Legacy** - это _старый_ пак имеющий Minecraft BE 1.11.4 который более не будет обновляться. Также поддержка некоторыми модами этой версии пака будет прекращена.

## Как поставить свой ресурспак, аддон, шейдеры?

Для ресурспаков \(resource\_pack\) - /sdcard/games/horizon/packs/&lt;имя пака&gt;/innercore/resource\_packs

Для аддонов \(behavior\_pack\) - /sdcard/games/horizon/packs/&lt;имя пака&gt;/innercore/behavior\_packs

Шейдеры - это тот же ресурспак

## Расположения

Миры находятся в папке `/sdcard/games/horizon/packs/<имя пака>/worlds`

Модпаки находятся в папке `/sdcard/games/horizon/packs/<имя пака>/modpacks`

Моды находятся в папке `/sdcard/games/horizon/packs/<имя пака>/innercore/mods`

## Зачем нужны папки/файлы

* В папке /sdcard/games/horizon/
  * behavior\_packs - Туда копируются все аддоны используемые паком, папка каждый раз очищается
  * resource\_packs - Туда копируются все ресурспаки используемые паком, папка каждый раз очищается
* В папке /sdcard/games/horizon/packs/&lt;имя пака&gt;/
  * assets - Здесь находятся все ресурсы приложения
  * innercore - данные пака InnerCore
  * java - Java составляющая данного пака
  * native - C++ / Нативная составляющая пака
  * native\_mods - папка для нативных модов
  * so - C++ Библиотекии используемые паком
  * .cached\_graphics - zip архив с ресурсами пака
  * .installation\_complete, .installation\_info, .installation\_started - файлы состояния установки
  * manifest.json - данные об паке
* В папке /sdcard/games/horizon/packs/&lt;имя пака&gt;/innercore
  * cache - кэш текстур для InnerCore
  * coreengine - исходные js файлы InnerCore
  * config.json - туда сохраняются все настройки InnerCore
  * furnace.json - содержит данные о горении предметов в тиках
  * inner-core.log - содержит лог innercore

