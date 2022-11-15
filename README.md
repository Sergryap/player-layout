## Библиотека для создания видеоплеера

Минимальный набор инструментов, который нужен для создания своего видеоплеера. Все элементы можно кастомизировать на свой вкус и цвет.


![max](https://user-images.githubusercontent.com/99894266/201955001-35ec4fc2-cf4b-4733-b657-6e308b00ae9f.gif)


## Как подключить

JS код поставляется в виде одного файла player.js, который можно скачать из этого репозитория.

Для работы он требует двух библиотек - jQuery и Playable. Пример подключения в браузере:

```html
<script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
<script src="https://unpkg.com/playable@2.10.3/dist/statics/playable.bundle.min.js"></script>
<script src="player.js"></script>
```

Для работы библиотека требует HTML разметки. Вот полный пример с минимальным количеством настроек:

```html
<div id="player" style="width: 800px; height: 600px;">
    <div class="js-video-container" style="width: 100%; height: 100%"></div>
</div>

<script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
<script src="https://unpkg.com/playable@2.10.3/dist/statics/playable.bundle.min.js"></script>
<script src="player.js"></script>

<script type="text/javascript">
  createPlayer({elementId: 'player'});
</script>
```
Этот код добавит на страницу плеер, который играет видео по этой [ссылке](https://dvmn.org/media/filer_public/78/db/78db3456-3fd3-4504-9ed9-d2d1fd843c0b/highest_peak.mp4).

Если хочется выбрать другое видео, с помощью аргумента `src` плееру можно указать какое видео проигрывать, ссылки обязаны заканчиваться расширением файла:

```html
<script type="text/javascript">
  createPlayer({
    elementId: 'player',
    src: 'https://dvmn.org/media/filer_public/d0/16/d016d9b8-4180-4bb9-ad83-0241f61627b8/samsung_demo_-_alive_in_color.mp4'
});
</script>
```

**Скрипт `player.js` нужно подключать строго после `<div>` с указанным elementId**
