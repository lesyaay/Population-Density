# Cinemas
Мой проект посвящён исследованию кинотеатров 2020-го года. Этот год особо интересен, потому что карантин сильно повлиял на работу многих кинотеатров. Однако, цель исследования шире: 
Я выясню, как каратнин повлиял на работу кинотеатров в России, выясню, какие самые популярные места в кинозалах, отмечу на карте Москвы все кинотеатры и сделаю мное другое.

Цель моего исследования — подробно разобраться во всех документально подтверждённых и зафиксированных катастрофах, произошедших в XXI веке, и рассмотреть наиболее значительные из них.
## Датасет
Датасет был выгружен с сайта (https://dano.hse.ru/data2022). Он содержит в себе информацию по заказам билетов в кино в 2020 году.
Основные параметры, которые я использую в своем исследовании:
1) Дата сеанса
2) Жанры (всего их 28)
3) Кол-во билетов в чеке
4) Комментарий по ряду и месту
5) Название кинотеатра
6) Широта положения кинотеатра
7) Долгота положения кинотеатра
8) Город кинотеатра

## Задачи
1. Построить карту кинотеатров Москвы
2. Построить график посещаемости кинотеатров за 2020 год
3. Построить диаграмму популярности жанров
4. Построить диаграмму, отражающую соотношение заказов с разным количеством билетов в них
5. Постоить диаграмму, отражающую самые популярные места в кинозале

## Результаты работы
В ходе исследования были составлены карты, графики и диаграммы:
<!DOCTYPE html>
<html>
<head>
    
    <meta http-equiv="content-type" content="text/html; charset=UTF-8" />
    
        <script>
            L_NO_TOUCH = false;
            L_DISABLE_3D = false;
        </script>
    
    <style>html, body {width: 100%;height: 100%;margin: 0;padding: 0;}</style>
    <style>#map {position:absolute;top:0;bottom:0;right:0;left:0;}</style>
    <script src="https://cdn.jsdelivr.net/npm/leaflet@1.9.3/dist/leaflet.js"></script>
    <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.js"></script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/leaflet@1.9.3/dist/leaflet.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css"/>
    <link rel="stylesheet" href="https://netdna.bootstrapcdn.com/bootstrap/3.0.0/css/bootstrap-glyphicons.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.2.0/css/all.min.css"/>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.css"/>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/python-visualization/folium/folium/templates/leaflet.awesome.rotate.min.css"/>
    
            <meta name="viewport" content="width=device-width,
                initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
            <style>
                #map_67f07251aafe8124cfcd2a4e05955538 {
                    position: relative;
                    width: 100.0%;
                    height: 100.0%;
                    left: 0.0%;
                    top: 0.0%;
                }
                .leaflet-container { font-size: 1rem; }
            </style>
        
</head>
<body>
    
    
            <div class="folium-map" id="map_67f07251aafe8124cfcd2a4e05955538" ></div>
        
</body>
<script>
    
    
            var map_67f07251aafe8124cfcd2a4e05955538 = L.map(
                "map_67f07251aafe8124cfcd2a4e05955538",
                {
                    center: [55.753215, 37.622504],
                    crs: L.CRS.EPSG3857,
                    zoom: 11,
                    zoomControl: true,
                    preferCanvas: false,
                }
            );

            

        
    
            var tile_layer_beae332aa00d60c219f7c15552873800 = L.tileLayer(
                "https://tile.openstreetmap.org/{z}/{x}/{y}.png",
                {"attribution": "\u0026copy; \u003ca href=\"https://www.openstreetmap.org/copyright\"\u003eOpenStreetMap\u003c/a\u003e contributors", "detectRetina": false, "maxNativeZoom": 19, "maxZoom": 19, "minZoom": 0, "noWrap": false, "opacity": 1, "subdomains": "abc", "tms": false}
            );
        
    
            tile_layer_beae332aa00d60c219f7c15552873800.addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var marker_e6152bbf10521621217cd1a8429e4724 = L.marker(
                [55.809469, 37.464571],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_1f4ebfb4b26c33d8d40a77568315cf2d = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e6152bbf10521621217cd1a8429e4724.setIcon(icon_1f4ebfb4b26c33d8d40a77568315cf2d);
        
    
        var popup_fb3399619e8e22de7afd6f584acd1705 = L.popup({"maxWidth": "100%"});

        
            
                var html_25c0346bc0e7c538c172faefe18ab09a = $(`<div id="html_25c0346bc0e7c538c172faefe18ab09a" style="width: 100.0%; height: 100.0%;">Каро 10 Щука</div>`)[0];
                popup_fb3399619e8e22de7afd6f584acd1705.setContent(html_25c0346bc0e7c538c172faefe18ab09a);
            
        

        marker_e6152bbf10521621217cd1a8429e4724.bindPopup(popup_fb3399619e8e22de7afd6f584acd1705)
        ;

        
    
    
            var marker_719b8ed96e1f417866d4cca5d5c00ea1 = L.marker(
                [55.753338, 37.587615],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_456038423d6b1a3174603012bcebf2eb = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_719b8ed96e1f417866d4cca5d5c00ea1.setIcon(icon_456038423d6b1a3174603012bcebf2eb);
        
    
        var popup_64528d0fde6de7594c0cc89d20955076 = L.popup({"maxWidth": "100%"});

        
            
                var html_ff51130ce5216292b7886654d243a3e3 = $(`<div id="html_ff51130ce5216292b7886654d243a3e3" style="width: 100.0%; height: 100.0%;">Каро 11 Октябрь</div>`)[0];
                popup_64528d0fde6de7594c0cc89d20955076.setContent(html_ff51130ce5216292b7886654d243a3e3);
            
        

        marker_719b8ed96e1f417866d4cca5d5c00ea1.bindPopup(popup_64528d0fde6de7594c0cc89d20955076)
        ;

        
    
    
            var marker_a5dac7e6b8a4141aaf97d8249ae237eb = L.marker(
                [55.757214, 37.658941],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_5ae37439db32500ff57a93835845992f = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_a5dac7e6b8a4141aaf97d8249ae237eb.setIcon(icon_5ae37439db32500ff57a93835845992f);
        
    
        var popup_6955ede7bf8db8d01423a4e487944f48 = L.popup({"maxWidth": "100%"});

        
            
                var html_123e2ead2ff4418e5dadeb55d78632cd = $(`<div id="html_123e2ead2ff4418e5dadeb55d78632cd" style="width: 100.0%; height: 100.0%;">Каро 7 Атриум</div>`)[0];
                popup_6955ede7bf8db8d01423a4e487944f48.setContent(html_123e2ead2ff4418e5dadeb55d78632cd);
            
        

        marker_a5dac7e6b8a4141aaf97d8249ae237eb.bindPopup(popup_6955ede7bf8db8d01423a4e487944f48)
        ;

        
    
    
            var marker_2b69400457fe8e8b2eb58622cc3e0b5d = L.marker(
                [55.913178, 37.585763],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_821d023391a30710aed7bf1da83b0948 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_2b69400457fe8e8b2eb58622cc3e0b5d.setIcon(icon_821d023391a30710aed7bf1da83b0948);
        
    
        var popup_e8e8dea0591830106557534ccbcf8083 = L.popup({"maxWidth": "100%"});

        
            
                var html_50fa6117bda12044693f0d2fd1bebab5 = $(`<div id="html_50fa6117bda12044693f0d2fd1bebab5" style="width: 100.0%; height: 100.0%;">Люксор Весна</div>`)[0];
                popup_e8e8dea0591830106557534ccbcf8083.setContent(html_50fa6117bda12044693f0d2fd1bebab5);
            
        

        marker_2b69400457fe8e8b2eb58622cc3e0b5d.bindPopup(popup_e8e8dea0591830106557534ccbcf8083)
        ;

        
    
    
            var marker_a46c4251dad07989e9eb948155c8b0cc = L.marker(
                [55.548599, 37.542392],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_12be05c8a8ff5402680ab2e43957ca88 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_a46c4251dad07989e9eb948155c8b0cc.setIcon(icon_12be05c8a8ff5402680ab2e43957ca88);
        
    
        var popup_427384a4680846f38cc22ac7dbb64dfd = L.popup({"maxWidth": "100%"});

        
            
                var html_3e697a4caa892abbbb8b10492354f6bc = $(`<div id="html_3e697a4caa892abbbb8b10492354f6bc" style="width: 100.0%; height: 100.0%;">Каро 8 Южное Бутово</div>`)[0];
                popup_427384a4680846f38cc22ac7dbb64dfd.setContent(html_3e697a4caa892abbbb8b10492354f6bc);
            
        

        marker_a46c4251dad07989e9eb948155c8b0cc.bindPopup(popup_427384a4680846f38cc22ac7dbb64dfd)
        ;

        
    
    
            var marker_041909b6b536e88347510c2eb6eb51aa = L.marker(
                [55.663019, 37.480993],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_ed67b5a820344ab75a452627e18f8988 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_041909b6b536e88347510c2eb6eb51aa.setIcon(icon_ed67b5a820344ab75a452627e18f8988);
        
    
        var popup_51ec5bcaa971b710ea2a516eb37629c1 = L.popup({"maxWidth": "100%"});

        
            
                var html_a93d8c8619396ffb999a4f17e36b2966 = $(`<div id="html_a93d8c8619396ffb999a4f17e36b2966" style="width: 100.0%; height: 100.0%;">Синема Стар Москва Юго-Западная</div>`)[0];
                popup_51ec5bcaa971b710ea2a516eb37629c1.setContent(html_a93d8c8619396ffb999a4f17e36b2966);
            
        

        marker_041909b6b536e88347510c2eb6eb51aa.bindPopup(popup_51ec5bcaa971b710ea2a516eb37629c1)
        ;

        
    
    
            var marker_caf483f26bdff154c6ad766ec80e7359 = L.marker(
                [55.790232, 37.530826],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_17f7cbd4a05ff9a74a8aa5cef6499874 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_caf483f26bdff154c6ad766ec80e7359.setIcon(icon_17f7cbd4a05ff9a74a8aa5cef6499874);
        
    
        var popup_8114400f2be4f03629e353f6444ecf99 = L.popup({"maxWidth": "100%"});

        
            
                var html_8a366ddf4041be663bdb5d15d99acc7e = $(`<div id="html_8a366ddf4041be663bdb5d15d99acc7e" style="width: 100.0%; height: 100.0%;">Каро Sky 17 Авиапарк</div>`)[0];
                popup_8114400f2be4f03629e353f6444ecf99.setContent(html_8a366ddf4041be663bdb5d15d99acc7e);
            
        

        marker_caf483f26bdff154c6ad766ec80e7359.bindPopup(popup_8114400f2be4f03629e353f6444ecf99)
        ;

        
    
    
            var marker_e310048ac1a6aef683e457fd34fd0d22 = L.marker(
                [55.839474, 37.493276],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_3bcd85d56fd8e9b7bcb5f9d25732a71e = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e310048ac1a6aef683e457fd34fd0d22.setIcon(icon_3bcd85d56fd8e9b7bcb5f9d25732a71e);
        
    
        var popup_6c086d76edbec988908791cf6c5d03a6 = L.popup({"maxWidth": "100%"});

        
            
                var html_91233085ae2613d86bbb7a5d678e21aa = $(`<div id="html_91233085ae2613d86bbb7a5d678e21aa" style="width: 100.0%; height: 100.0%;">Киномакс-Водный</div>`)[0];
                popup_6c086d76edbec988908791cf6c5d03a6.setContent(html_91233085ae2613d86bbb7a5d678e21aa);
            
        

        marker_e310048ac1a6aef683e457fd34fd0d22.bindPopup(popup_6c086d76edbec988908791cf6c5d03a6)
        ;

        
    
    
            var marker_0cee80bd8ac97131a5ce64ebccb093bf = L.marker(
                [55.7330384054911, 37.637394994526176],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_f43831ce83d0ef075bcd5e802f72d83c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_0cee80bd8ac97131a5ce64ebccb093bf.setIcon(icon_f43831ce83d0ef075bcd5e802f72d83c);
        
    
        var popup_5323c3339f3e7f43b17af0d1fc110bb3 = L.popup({"maxWidth": "100%"});

        
            
                var html_e59571d335126f27fad767683014f78e = $(`<div id="html_e59571d335126f27fad767683014f78e" style="width: 100.0%; height: 100.0%;">5 звезд на Павелецкой</div>`)[0];
                popup_5323c3339f3e7f43b17af0d1fc110bb3.setContent(html_e59571d335126f27fad767683014f78e);
            
        

        marker_0cee80bd8ac97131a5ce64ebccb093bf.bindPopup(popup_5323c3339f3e7f43b17af0d1fc110bb3)
        ;

        
    
    
            var marker_6667331b769c058c7e8171fdba09b4a1 = L.marker(
                [55.85883344761388, 37.39507957136891],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_4d706c40ddbadb9831206aca7353afc5 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_6667331b769c058c7e8171fdba09b4a1.setIcon(icon_4d706c40ddbadb9831206aca7353afc5);
        
    
        var popup_03f6b6a784cda0059df609ec97948e2f = L.popup({"maxWidth": "100%"});

        
            
                var html_0732ae86fd6d72d4bd165459b671f453 = $(`<div id="html_0732ae86fd6d72d4bd165459b671f453" style="width: 100.0%; height: 100.0%;">Кронверк Синема Вэйпарк</div>`)[0];
                popup_03f6b6a784cda0059df609ec97948e2f.setContent(html_0732ae86fd6d72d4bd165459b671f453);
            
        

        marker_6667331b769c058c7e8171fdba09b4a1.bindPopup(popup_03f6b6a784cda0059df609ec97948e2f)
        ;

        
    
    
            var marker_397c0b0d68dcfef77e8bbd83b5947c0a = L.marker(
                [55.7492601878281, 37.5399999682618],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_4180a29da9ceb3ae988020e1c4aaa3e7 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_397c0b0d68dcfef77e8bbd83b5947c0a.setIcon(icon_4180a29da9ceb3ae988020e1c4aaa3e7);
        
    
        var popup_1c2499097a818872966aa4472ac218dd = L.popup({"maxWidth": "100%"});

        
            
                var html_731ca7bd432d2ba0e6e07a4c363280f4 = $(`<div id="html_731ca7bd432d2ba0e6e07a4c363280f4" style="width: 100.0%; height: 100.0%;">КИНО ОККО Афимолл Сити</div>`)[0];
                popup_1c2499097a818872966aa4472ac218dd.setContent(html_731ca7bd432d2ba0e6e07a4c363280f4);
            
        

        marker_397c0b0d68dcfef77e8bbd83b5947c0a.bindPopup(popup_1c2499097a818872966aa4472ac218dd)
        ;

        
    
    
            var marker_4cbca0575f75b54a0c167d8a32479837 = L.marker(
                [55.8232147685953, 37.4976663887774],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_94c615535479444ed01bac99bc980209 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_4cbca0575f75b54a0c167d8a32479837.setIcon(icon_94c615535479444ed01bac99bc980209);
        
    
        var popup_b25916e955b00f011ad7b62323e09e2a = L.popup({"maxWidth": "100%"});

        
            
                var html_fa9592db503cfa9cc6732b60168f5e6d = $(`<div id="html_fa9592db503cfa9cc6732b60168f5e6d" style="width: 100.0%; height: 100.0%;">Синема Парк Метрополис на Войковской</div>`)[0];
                popup_b25916e955b00f011ad7b62323e09e2a.setContent(html_fa9592db503cfa9cc6732b60168f5e6d);
            
        

        marker_4cbca0575f75b54a0c167d8a32479837.bindPopup(popup_b25916e955b00f011ad7b62323e09e2a)
        ;

        
    
    
            var marker_e310fb2dff76e09aafe27c3c23878c65 = L.marker(
                [55.74456719660905, 37.62992663117871],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_c5693f092d31022d277120e3ecb2e1b5 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e310fb2dff76e09aafe27c3c23878c65.setIcon(icon_c5693f092d31022d277120e3ecb2e1b5);
        
    
        var popup_917d46fa44ff271b0cce758fffa922d3 = L.popup({"maxWidth": "100%"});

        
            
                var html_2c9792c7478031ae3fe7a53eed4f7b92 = $(`<div id="html_2c9792c7478031ae3fe7a53eed4f7b92" style="width: 100.0%; height: 100.0%;">5 звезд на Новокузнецкой</div>`)[0];
                popup_917d46fa44ff271b0cce758fffa922d3.setContent(html_2c9792c7478031ae3fe7a53eed4f7b92);
            
        

        marker_e310fb2dff76e09aafe27c3c23878c65.bindPopup(popup_917d46fa44ff271b0cce758fffa922d3)
        ;

        
    
    
            var marker_8a8208e826a3738f932e7a904cb9d15f = L.marker(
                [55.6857669, 37.854277000000025],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_9759e2400ea511ae4c77e69221a68109 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_8a8208e826a3738f932e7a904cb9d15f.setIcon(icon_9759e2400ea511ae4c77e69221a68109);
        
    
        var popup_23ccfa78aea82886c56ac6373538a50d = L.popup({"maxWidth": "100%"});

        
            
                var html_a242b6cd7d390999c1c7f1be7ec77b96 = $(`<div id="html_a242b6cd7d390999c1c7f1be7ec77b96" style="width: 100.0%; height: 100.0%;">Киномакс–Жулебино</div>`)[0];
                popup_23ccfa78aea82886c56ac6373538a50d.setContent(html_a242b6cd7d390999c1c7f1be7ec77b96);
            
        

        marker_8a8208e826a3738f932e7a904cb9d15f.bindPopup(popup_23ccfa78aea82886c56ac6373538a50d)
        ;

        
    
    
            var marker_3d9e4242b108a4f0fd32ed32745a3628 = L.marker(
                [55.6211864, 37.71377150000001],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_6bce34afdb6c146ce368eff696df6a22 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_3d9e4242b108a4f0fd32ed32745a3628.setIcon(icon_6bce34afdb6c146ce368eff696df6a22);
        
    
        var popup_8d9fcd89c9783aaf523b98c7e971e13e = L.popup({"maxWidth": "100%"});

        
            
                var html_763e7f3909d3a09d673a1ef703b060c6 = $(`<div id="html_763e7f3909d3a09d673a1ef703b060c6" style="width: 100.0%; height: 100.0%;">Киномакс–Титан</div>`)[0];
                popup_8d9fcd89c9783aaf523b98c7e971e13e.setContent(html_763e7f3909d3a09d673a1ef703b060c6);
            
        

        marker_3d9e4242b108a4f0fd32ed32745a3628.bindPopup(popup_8d9fcd89c9783aaf523b98c7e971e13e)
        ;

        
    
    
            var marker_610a40d923d98b7c2f3ab909e2ee8238 = L.marker(
                [55.611079, 37.606815],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_14e645c66ca68e2bd41169894148c70d = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_610a40d923d98b7c2f3ab909e2ee8238.setIcon(icon_14e645c66ca68e2bd41169894148c70d);
        
    
        var popup_8f27e019467510de5d78cd2769929afe = L.popup({"maxWidth": "100%"});

        
            
                var html_3d037468e4ee1018c9ded47911162b13 = $(`<div id="html_3d037468e4ee1018c9ded47911162b13" style="width: 100.0%; height: 100.0%;">Киномакс-Пражская</div>`)[0];
                popup_8f27e019467510de5d78cd2769929afe.setContent(html_3d037468e4ee1018c9ded47911162b13);
            
        

        marker_610a40d923d98b7c2f3ab909e2ee8238.bindPopup(popup_8f27e019467510de5d78cd2769929afe)
        ;

        
    
    
            var marker_ebf77fba9ac5041c317c05b695da187f = L.marker(
                [55.65964338228474, 37.74961602960343],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_0ef0bbc689e043fedd01a9008d48ec1c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_ebf77fba9ac5041c317c05b695da187f.setIcon(icon_0ef0bbc689e043fedd01a9008d48ec1c);
        
    
        var popup_a343e35fa8f3b3f6d670780f78e1cb1e = L.popup({"maxWidth": "100%"});

        
            
                var html_94e2b2879323588e6c94dc05492491a5 = $(`<div id="html_94e2b2879323588e6c94dc05492491a5" style="width: 100.0%; height: 100.0%;">Киномакс–Солярис</div>`)[0];
                popup_a343e35fa8f3b3f6d670780f78e1cb1e.setContent(html_94e2b2879323588e6c94dc05492491a5);
            
        

        marker_ebf77fba9ac5041c317c05b695da187f.bindPopup(popup_a343e35fa8f3b3f6d670780f78e1cb1e)
        ;

        
    
    
            var marker_69880bc633cf65c8fb0429739167b53d = L.marker(
                [55.6226598024446, 37.6060147583769],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_efe75df75611b5b18764c549094e11d2 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_69880bc633cf65c8fb0429739167b53d.setIcon(icon_efe75df75611b5b18764c549094e11d2);
        
    
        var popup_0230e5496c3ae013b9b2d2319c5be6b4 = L.popup({"maxWidth": "100%"});

        
            
                var html_594b4b314ebe33abd96e99914baa6a80 = $(`<div id="html_594b4b314ebe33abd96e99914baa6a80" style="width: 100.0%; height: 100.0%;">Синема Парк Глобал Сити на Южной</div>`)[0];
                popup_0230e5496c3ae013b9b2d2319c5be6b4.setContent(html_594b4b314ebe33abd96e99914baa6a80);
            
        

        marker_69880bc633cf65c8fb0429739167b53d.bindPopup(popup_0230e5496c3ae013b9b2d2319c5be6b4)
        ;

        
    
    
            var marker_035f6d799556f703f839449dfc7390e3 = L.marker(
                [55.687051, 37.603918],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_aaec3a374e765a94074c461c051adbec = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_035f6d799556f703f839449dfc7390e3.setIcon(icon_aaec3a374e765a94074c461c051adbec);
        
    
        var popup_e346d1535f0f8bc7b7ec671794fe1aaa = L.popup({"maxWidth": "100%"});

        
            
                var html_37c513bd39b338d504b137ba1090dd20 = $(`<div id="html_37c513bd39b338d504b137ba1090dd20" style="width: 100.0%; height: 100.0%;">Каро 6 Севастопольский</div>`)[0];
                popup_e346d1535f0f8bc7b7ec671794fe1aaa.setContent(html_37c513bd39b338d504b137ba1090dd20);
            
        

        marker_035f6d799556f703f839449dfc7390e3.bindPopup(popup_e346d1535f0f8bc7b7ec671794fe1aaa)
        ;

        
    
    
            var marker_0e81799d93dc4bf877c1884c24114c47 = L.marker(
                [55.66584, 37.627885],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_8dc7683cfdfdc205ba2f572c15c623c6 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_0e81799d93dc4bf877c1884c24114c47.setIcon(icon_8dc7683cfdfdc205ba2f572c15c623c6);
        
    
        var popup_1390be619e119a30a99a4230b0c50f4b = L.popup({"maxWidth": "100%"});

        
            
                var html_7b579d4f8b663ee2f47941e6b00a626f = $(`<div id="html_7b579d4f8b663ee2f47941e6b00a626f" style="width: 100.0%; height: 100.0%;">Люксор Гудзон</div>`)[0];
                popup_1390be619e119a30a99a4230b0c50f4b.setContent(html_7b579d4f8b663ee2f47941e6b00a626f);
            
        

        marker_0e81799d93dc4bf877c1884c24114c47.bindPopup(popup_1390be619e119a30a99a4230b0c50f4b)
        ;

        
    
    
            var marker_40cecfa6cfe7790ffde4b0dcc70ac80c = L.marker(
                [55.814477, 37.571157],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_ad816503804913192af95649baf780f5 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_40cecfa6cfe7790ffde4b0dcc70ac80c.setIcon(icon_ad816503804913192af95649baf780f5);
        
    
        var popup_133db6bc387521a92f20e604601832e3 = L.popup({"maxWidth": "100%"});

        
            
                var html_351bf71d4aae20c263572b2f929738bf = $(`<div id="html_351bf71d4aae20c263572b2f929738bf" style="width: 100.0%; height: 100.0%;">Москино Искра</div>`)[0];
                popup_133db6bc387521a92f20e604601832e3.setContent(html_351bf71d4aae20c263572b2f929738bf);
            
        

        marker_40cecfa6cfe7790ffde4b0dcc70ac80c.bindPopup(popup_133db6bc387521a92f20e604601832e3)
        ;

        
    
    
            var marker_17519fe76ab7f30ffef09602f74b656a = L.marker(
                [55.744977, 37.549866],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_0b9b73f30e18fa68324c3188aeebf84d = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_17519fe76ab7f30ffef09602f74b656a.setIcon(icon_0b9b73f30e18fa68324c3188aeebf84d);
        
    
        var popup_baf2bb4b8c8fab6321a5534f64500a34 = L.popup({"maxWidth": "100%"});

        
            
                var html_f4baf06b92798e77d2d8324b657b574b = $(`<div id="html_f4baf06b92798e77d2d8324b657b574b" style="width: 100.0%; height: 100.0%;">Пионер</div>`)[0];
                popup_baf2bb4b8c8fab6321a5534f64500a34.setContent(html_f4baf06b92798e77d2d8324b657b574b);
            
        

        marker_17519fe76ab7f30ffef09602f74b656a.bindPopup(popup_baf2bb4b8c8fab6321a5534f64500a34)
        ;

        
    
    
            var marker_6227213e379d1fa59023d8c698da04b8 = L.marker(
                [55.719828, 37.378191],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_c7d9b4e5d9256312aa987cc7bcfb34d3 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_6227213e379d1fa59023d8c698da04b8.setIcon(icon_c7d9b4e5d9256312aa987cc7bcfb34d3);
        
    
        var popup_44934b6b1bfe602a84e4676e3fcf3d71 = L.popup({"maxWidth": "100%"});

        
            
                var html_6eee8dd481a372e72d66e57a645f65bd = $(`<div id="html_6eee8dd481a372e72d66e57a645f65bd" style="width: 100.0%; height: 100.0%;">Каро 13 Кунцево</div>`)[0];
                popup_44934b6b1bfe602a84e4676e3fcf3d71.setContent(html_6eee8dd481a372e72d66e57a645f65bd);
            
        

        marker_6227213e379d1fa59023d8c698da04b8.bindPopup(popup_44934b6b1bfe602a84e4676e3fcf3d71)
        ;

        
    
    
            var marker_e396763bf7f13670e624b6bb7b6838f8 = L.marker(
                [55.97519732351029, 37.90684611314202],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a0589d19a31e72af6a52c72b7675925a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e396763bf7f13670e624b6bb7b6838f8.setIcon(icon_a0589d19a31e72af6a52c72b7675925a);
        
    
        var popup_a174660566a6a44727e77c5b7a0e240f = L.popup({"maxWidth": "100%"});

        
            
                var html_cc794a2e1ebdef284405e67287b23b38 = $(`<div id="html_cc794a2e1ebdef284405e67287b23b38" style="width: 100.0%; height: 100.0%;">Gagarin Cinema (Ивантеевка)</div>`)[0];
                popup_a174660566a6a44727e77c5b7a0e240f.setContent(html_cc794a2e1ebdef284405e67287b23b38);
            
        

        marker_e396763bf7f13670e624b6bb7b6838f8.bindPopup(popup_a174660566a6a44727e77c5b7a0e240f)
        ;

        
    
    
            var marker_37c9ac6f931995d91ba6288fd82d3852 = L.marker(
                [55.754722, 37.621389],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_71c1c4f10bcd57a21bee9b3bd6538db3 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_37c9ac6f931995d91ba6288fd82d3852.setIcon(icon_71c1c4f10bcd57a21bee9b3bd6538db3);
        
    
        var popup_929f2eeff0d3b9e7a7672b15b01d798c = L.popup({"maxWidth": "100%"});

        
            
                var html_b3f2d0fe3f438088a78b7028f6b84e35 = $(`<div id="html_b3f2d0fe3f438088a78b7028f6b84e35" style="width: 100.0%; height: 100.0%;">ГУМ Кинозал</div>`)[0];
                popup_929f2eeff0d3b9e7a7672b15b01d798c.setContent(html_b3f2d0fe3f438088a78b7028f6b84e35);
            
        

        marker_37c9ac6f931995d91ba6288fd82d3852.bindPopup(popup_929f2eeff0d3b9e7a7672b15b01d798c)
        ;

        
    
    
            var marker_fbeaece56c8a68a9984c74ee5b367c0d = L.marker(
                [55.705072, 37.639383],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_4d9aff330e082eaf0a1df5a0b9c2bfdd = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_fbeaece56c8a68a9984c74ee5b367c0d.setIcon(icon_4d9aff330e082eaf0a1df5a0b9c2bfdd);
        
    
        var popup_e337644a7e1314e18748e1b64251d732 = L.popup({"maxWidth": "100%"});

        
            
                var html_bc8c55ade08356d234083b35feba9dd3 = $(`<div id="html_bc8c55ade08356d234083b35feba9dd3" style="width: 100.0%; height: 100.0%;">Синема Парк Ривьера на Автозаводской</div>`)[0];
                popup_e337644a7e1314e18748e1b64251d732.setContent(html_bc8c55ade08356d234083b35feba9dd3);
            
        

        marker_fbeaece56c8a68a9984c74ee5b367c0d.bindPopup(popup_e337644a7e1314e18748e1b64251d732)
        ;

        
    
    
            var marker_2e568efeb111e1c517cbf06897c5d75b = L.marker(
                [55.86369830000277, 37.54592979999563],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_5daa28cd8264bd45f78055e957afeda1 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_2e568efeb111e1c517cbf06897c5d75b.setIcon(icon_5daa28cd8264bd45f78055e957afeda1);
        
    
        var popup_2e50f6d71a8ac776545e4e6885a809c3 = L.popup({"maxWidth": "100%"});

        
            
                var html_c45c06dafa108c592c8f5ba362803515 = $(`<div id="html_c45c06dafa108c592c8f5ba362803515" style="width: 100.0%; height: 100.0%;">Киномакс–XL</div>`)[0];
                popup_2e50f6d71a8ac776545e4e6885a809c3.setContent(html_c45c06dafa108c592c8f5ba362803515);
            
        

        marker_2e568efeb111e1c517cbf06897c5d75b.bindPopup(popup_2e50f6d71a8ac776545e4e6885a809c3)
        ;

        
    
    
            var marker_340e02e54889c616b20d0e09997ee1e8 = L.marker(
                [55.6399594, 37.7583009],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_c95ba9f28faf6b85a183d1d8d55115ca = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_340e02e54889c616b20d0e09997ee1e8.setIcon(icon_c95ba9f28faf6b85a183d1d8d55115ca);
        
    
        var popup_093ae297247e8cecd9200b918a2647b5 = L.popup({"maxWidth": "100%"});

        
            
                var html_11de4655435dba6df976cf86d61e7cb9 = $(`<div id="html_11de4655435dba6df976cf86d61e7cb9" style="width: 100.0%; height: 100.0%;">Pushka Братеево</div>`)[0];
                popup_093ae297247e8cecd9200b918a2647b5.setContent(html_11de4655435dba6df976cf86d61e7cb9);
            
        

        marker_340e02e54889c616b20d0e09997ee1e8.bindPopup(popup_093ae297247e8cecd9200b918a2647b5)
        ;

        
    
    
            var marker_258a615e662df78fd18ecd188d2bb421 = L.marker(
                [55.67796891373151, 37.46705064418029],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_aac8e98ce54b381f9d55705a2698fd12 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_258a615e662df78fd18ecd188d2bb421.setIcon(icon_aac8e98ce54b381f9d55705a2698fd12);
        
    
        var popup_5eabcb46f78c93862d83124074c18fab = L.popup({"maxWidth": "100%"});

        
            
                var html_2bcc10493785cb4fdd8889e2e5dfc572 = $(`<div id="html_2bcc10493785cb4fdd8889e2e5dfc572" style="width: 100.0%; height: 100.0%;">Формула Кино на Мичуринском</div>`)[0];
                popup_5eabcb46f78c93862d83124074c18fab.setContent(html_2bcc10493785cb4fdd8889e2e5dfc572);
            
        

        marker_258a615e662df78fd18ecd188d2bb421.bindPopup(popup_5eabcb46f78c93862d83124074c18fab)
        ;

        
    
    
            var marker_79a50e893b724f1acc4e089183ba5482 = L.marker(
                [55.710639, 37.674466],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_2f25ae6661ead836bbe7be08dde3ebe1 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_79a50e893b724f1acc4e089183ba5482.setIcon(icon_2f25ae6661ead836bbe7be08dde3ebe1);
        
    
        var popup_ad520c6c983f2b61d1af17a8b4744e12 = L.popup({"maxWidth": "100%"});

        
            
                var html_db507623a7d51c72d51c80ba948f8471 = $(`<div id="html_db507623a7d51c72d51c80ba948f8471" style="width: 100.0%; height: 100.0%;">Киномакс-Мозаика</div>`)[0];
                popup_ad520c6c983f2b61d1af17a8b4744e12.setContent(html_db507623a7d51c72d51c80ba948f8471);
            
        

        marker_79a50e893b724f1acc4e089183ba5482.bindPopup(popup_ad520c6c983f2b61d1af17a8b4744e12)
        ;

        
    
    
            var marker_715b6e14578894bad8c997b859ba28af = L.marker(
                [55.74738484542116, 37.70707635581971],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_e1b6cd5ea297166ad34598b730026bcd = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_715b6e14578894bad8c997b859ba28af.setIcon(icon_e1b6cd5ea297166ad34598b730026bcd);
        
    
        var popup_e8a9d4247421005b5689b18acef1aa50 = L.popup({"maxWidth": "100%"});

        
            
                var html_1e9161ea8fedd629c4c914fb70a1b5a1 = $(`<div id="html_1e9161ea8fedd629c4c914fb70a1b5a1" style="width: 100.0%; height: 100.0%;">Формула Кино Лефортово</div>`)[0];
                popup_e8a9d4247421005b5689b18acef1aa50.setContent(html_1e9161ea8fedd629c4c914fb70a1b5a1);
            
        

        marker_715b6e14578894bad8c997b859ba28af.bindPopup(popup_e8a9d4247421005b5689b18acef1aa50)
        ;

        
    
    
            var marker_6cdf1baea0a60aad7eb84591885def6c = L.marker(
                [55.91311067705894, 37.58443188115223],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_4d84fb57177fd9644bc37511ad5a03d0 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_6cdf1baea0a60aad7eb84591885def6c.setIcon(icon_4d84fb57177fd9644bc37511ad5a03d0);
        
    
        var popup_9a2d1b12b9682cfc43371e78d2b6f8df = L.popup({"maxWidth": "100%"});

        
            
                var html_d5f4604ccac6ebc71c7779d92d41116a = $(`<div id="html_d5f4604ccac6ebc71c7779d92d41116a" style="width: 100.0%; height: 100.0%;">Люксор Весна</div>`)[0];
                popup_9a2d1b12b9682cfc43371e78d2b6f8df.setContent(html_d5f4604ccac6ebc71c7779d92d41116a);
            
        

        marker_6cdf1baea0a60aad7eb84591885def6c.bindPopup(popup_9a2d1b12b9682cfc43371e78d2b6f8df)
        ;

        
    
    
            var marker_4e8a6e7797af53c041147e6f35c94178 = L.marker(
                [55.72789839669912, 37.4764491815348],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_078f0f63ae9439279d87bdd45025f3fb = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_4e8a6e7797af53c041147e6f35c94178.setIcon(icon_078f0f63ae9439279d87bdd45025f3fb);
        
    
        var popup_c13f0309e3033b65a7ad456e90784bca = L.popup({"maxWidth": "100%"});

        
            
                var html_96d266244ba8ca49e780bd0f4e9ec46f = $(`<div id="html_96d266244ba8ca49e780bd0f4e9ec46f" style="width: 100.0%; height: 100.0%;">Формула Кино на Кутузовском</div>`)[0];
                popup_c13f0309e3033b65a7ad456e90784bca.setContent(html_96d266244ba8ca49e780bd0f4e9ec46f);
            
        

        marker_4e8a6e7797af53c041147e6f35c94178.bindPopup(popup_c13f0309e3033b65a7ad456e90784bca)
        ;

        
    
    
            var marker_9d128503c8f56e3d55674ecf2b5a3cf4 = L.marker(
                [55.6066124133516, 37.53624485136743],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_9aa72c973ca8b18c3728e20980c82c04 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_9d128503c8f56e3d55674ecf2b5a3cf4.setIcon(icon_9aa72c973ca8b18c3728e20980c82c04);
        
    
        var popup_01879f9c89d822a6e67b75a4e1191cb7 = L.popup({"maxWidth": "100%"});

        
            
                var html_60eb3a2b79cbc4b4b3f8d75988414447 = $(`<div id="html_60eb3a2b79cbc4b4b3f8d75988414447" style="width: 100.0%; height: 100.0%;">Космик Ясенево</div>`)[0];
                popup_01879f9c89d822a6e67b75a4e1191cb7.setContent(html_60eb3a2b79cbc4b4b3f8d75988414447);
            
        

        marker_9d128503c8f56e3d55674ecf2b5a3cf4.bindPopup(popup_01879f9c89d822a6e67b75a4e1191cb7)
        ;

        
    
    
            var marker_325cc72e13478cda891e5a3f8c9e87fd = L.marker(
                [55.5830121280226, 37.5953712042298],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_5fb2df7575351676677d2a0a3e166ec7 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_325cc72e13478cda891e5a3f8c9e87fd.setIcon(icon_5fb2df7575351676677d2a0a3e166ec7);
        
    
        var popup_18b0e3a8118a1580344efd546281a2d9 = L.popup({"maxWidth": "100%"});

        
            
                var html_8458582e5c989ec413454cfa8285c580 = $(`<div id="html_8458582e5c989ec413454cfa8285c580" style="width: 100.0%; height: 100.0%;">Космик Аннино</div>`)[0];
                popup_18b0e3a8118a1580344efd546281a2d9.setContent(html_8458582e5c989ec413454cfa8285c580);
            
        

        marker_325cc72e13478cda891e5a3f8c9e87fd.bindPopup(popup_18b0e3a8118a1580344efd546281a2d9)
        ;

        
    
    
            var marker_d51593c93f670d5360cd60c8c5084e1b = L.marker(
                [55.7601567, 37.62461189999999],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_dded15a711b6a492c28332290e154766 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d51593c93f670d5360cd60c8c5084e1b.setIcon(icon_dded15a711b6a492c28332290e154766);
        
    
        var popup_ecff7a1125ca24e66b379eba8c54ecd6 = L.popup({"maxWidth": "100%"});

        
            
                var html_2e62bed07365a9129c485be9bd4c12bd = $(`<div id="html_2e62bed07365a9129c485be9bd4c12bd" style="width: 100.0%; height: 100.0%;">Формула Кино ЦДМ</div>`)[0];
                popup_ecff7a1125ca24e66b379eba8c54ecd6.setContent(html_2e62bed07365a9129c485be9bd4c12bd);
            
        

        marker_d51593c93f670d5360cd60c8c5084e1b.bindPopup(popup_ecff7a1125ca24e66b379eba8c54ecd6)
        ;

        
    
    
            var marker_82aa4c3460ddb168580dc3a376f0e843 = L.marker(
                [55.65596684085, 37.5414486229698],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_70583bde8945c3304c4b84ff5f4b0505 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_82aa4c3460ddb168580dc3a376f0e843.setIcon(icon_70583bde8945c3304c4b84ff5f4b0505);
        
    
        var popup_64c0b85154e752bd8b5a871f1363aaa6 = L.popup({"maxWidth": "100%"});

        
            
                var html_eea7770931060903204cd2470ae09832 = $(`<div id="html_eea7770931060903204cd2470ae09832" style="width: 100.0%; height: 100.0%;">Синема Парк на Калужской</div>`)[0];
                popup_64c0b85154e752bd8b5a871f1363aaa6.setContent(html_eea7770931060903204cd2470ae09832);
            
        

        marker_82aa4c3460ddb168580dc3a376f0e843.bindPopup(popup_64c0b85154e752bd8b5a871f1363aaa6)
        ;

        
    
    
            var marker_cb224ce8bb4ab7667749578b17be16ba = L.marker(
                [55.850661, 37.444295],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a29309c44f427244ff2550e6bd0812f9 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_cb224ce8bb4ab7667749578b17be16ba.setIcon(icon_a29309c44f427244ff2550e6bd0812f9);
        
    
        var popup_0aa735fdc414e45b294dfe2fe7c4d107 = L.popup({"maxWidth": "100%"});

        
            
                var html_b3506f2d1c3a5a65aff0ce4b2a6204ef = $(`<div id="html_b3506f2d1c3a5a65aff0ce4b2a6204ef" style="width: 100.0%; height: 100.0%;">Балтика</div>`)[0];
                popup_0aa735fdc414e45b294dfe2fe7c4d107.setContent(html_b3506f2d1c3a5a65aff0ce4b2a6204ef);
            
        

        marker_cb224ce8bb4ab7667749578b17be16ba.bindPopup(popup_0aa735fdc414e45b294dfe2fe7c4d107)
        ;

        
    
    
            var marker_c040d2ad9e911a22668cabf55b0f662d = L.marker(
                [55.689564, 37.602507],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_5dcb64e818bbad83fdfc2c5e184dd2df = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_c040d2ad9e911a22668cabf55b0f662d.setIcon(icon_5dcb64e818bbad83fdfc2c5e184dd2df);
        
    
        var popup_7ca779b078cb25b3672f72f94cba49a1 = L.popup({"maxWidth": "100%"});

        
            
                var html_64e9d53730287cee0a63bca835db554c = $(`<div id="html_64e9d53730287cee0a63bca835db554c" style="width: 100.0%; height: 100.0%;">Синема Стар на Академической</div>`)[0];
                popup_7ca779b078cb25b3672f72f94cba49a1.setContent(html_64e9d53730287cee0a63bca835db554c);
            
        

        marker_c040d2ad9e911a22668cabf55b0f662d.bindPopup(popup_7ca779b078cb25b3672f72f94cba49a1)
        ;

        
    
    
            var marker_d6e2793e1b3f82cecbae6e0dbf018ef5 = L.marker(
                [55.795361, 37.495424],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_4233c0b9f5c0fac1c81f7723f8cba188 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d6e2793e1b3f82cecbae6e0dbf018ef5.setIcon(icon_4233c0b9f5c0fac1c81f7723f8cba188);
        
    
        var popup_27740f6a3fd8345e06554387b652b050 = L.popup({"maxWidth": "100%"});

        
            
                var html_859b3ed1c484f800d179616da6170012 = $(`<div id="html_859b3ed1c484f800d179616da6170012" style="width: 100.0%; height: 100.0%;">Москино Юность</div>`)[0];
                popup_27740f6a3fd8345e06554387b652b050.setContent(html_859b3ed1c484f800d179616da6170012);
            
        

        marker_d6e2793e1b3f82cecbae6e0dbf018ef5.bindPopup(popup_27740f6a3fd8345e06554387b652b050)
        ;

        
    
    
            var marker_fce6e7050957e95265d4cb3c5fde7cfb = L.marker(
                [55.66354, 37.510919],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a2b88fbc1251942da94e934a15353e97 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_fce6e7050957e95265d4cb3c5fde7cfb.setIcon(icon_a2b88fbc1251942da94e934a15353e97);
        
    
        var popup_cf46c6c2c13b008f9a76f0e8dc70d6f3 = L.popup({"maxWidth": "100%"});

        
            
                var html_2d3a60fc13a809ec7280e8c5a7b217a7 = $(`<div id="html_2d3a60fc13a809ec7280e8c5a7b217a7" style="width: 100.0%; height: 100.0%;">Синема Стар на Ленинском</div>`)[0];
                popup_cf46c6c2c13b008f9a76f0e8dc70d6f3.setContent(html_2d3a60fc13a809ec7280e8c5a7b217a7);
            
        

        marker_fce6e7050957e95265d4cb3c5fde7cfb.bindPopup(popup_cf46c6c2c13b008f9a76f0e8dc70d6f3)
        ;

        
    
    
            var marker_e6d2f37ce1b1c320e12ea25db79f0891 = L.marker(
                [55.738591, 37.411005],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_bf43ca60d100e2df616b910cb013d58b = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e6d2f37ce1b1c320e12ea25db79f0891.setIcon(icon_bf43ca60d100e2df616b910cb013d58b);
        
    
        var popup_ebf93afd05b44fc954f52e2f94c29eed = L.popup({"maxWidth": "100%"});

        
            
                var html_69af28b67a789c670d13213ceb17c0ab = $(`<div id="html_69af28b67a789c670d13213ceb17c0ab" style="width: 100.0%; height: 100.0%;">Mori Cinema Кунцево</div>`)[0];
                popup_ebf93afd05b44fc954f52e2f94c29eed.setContent(html_69af28b67a789c670d13213ceb17c0ab);
            
        

        marker_e6d2f37ce1b1c320e12ea25db79f0891.bindPopup(popup_ebf93afd05b44fc954f52e2f94c29eed)
        ;

        
    
    
            var marker_cb5322e6c5051ae9008356780c25c8da = L.marker(
                [55.803484, 37.618767],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_1841793b55de242a5d3b4c55cd394cb4 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_cb5322e6c5051ae9008356780c25c8da.setIcon(icon_1841793b55de242a5d3b4c55cd394cb4);
        
    
        var popup_091ca219c6cb35cbeca18452d4c2bd61 = L.popup({"maxWidth": "100%"});

        
            
                var html_21e65259e8fdb66f6602a9189123d94a = $(`<div id="html_21e65259e8fdb66f6602a9189123d94a" style="width: 100.0%; height: 100.0%;">Каро 4 на Шереметьевской</div>`)[0];
                popup_091ca219c6cb35cbeca18452d4c2bd61.setContent(html_21e65259e8fdb66f6602a9189123d94a);
            
        

        marker_cb5322e6c5051ae9008356780c25c8da.bindPopup(popup_091ca219c6cb35cbeca18452d4c2bd61)
        ;

        
    
    
            var marker_d35a8799dc910dec5b8cd54403c4b247 = L.marker(
                [55.87606599999435, 37.3320360000107],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_823cd0a2c1f9de65a35b6a46d6df6d28 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d35a8799dc910dec5b8cd54403c4b247.setIcon(icon_823cd0a2c1f9de65a35b6a46d6df6d28);
        
    
        var popup_64a7b43486531377b60ca06de49093e2 = L.popup({"maxWidth": "100%"});

        
            
                var html_074df534bf8254f5e1b272eae0591b24 = $(`<div id="html_074df534bf8254f5e1b272eae0591b24" style="width: 100.0%; height: 100.0%;">Отрада</div>`)[0];
                popup_64a7b43486531377b60ca06de49093e2.setContent(html_074df534bf8254f5e1b272eae0591b24);
            
        

        marker_d35a8799dc910dec5b8cd54403c4b247.bindPopup(popup_64a7b43486531377b60ca06de49093e2)
        ;

        
    
    
            var marker_186f3e5b4b54a2703c9785ba7a586371 = L.marker(
                [55.612025999997655, 37.73258489998853],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_d014fed5d9c955536d2375e1939a124a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_186f3e5b4b54a2703c9785ba7a586371.setIcon(icon_d014fed5d9c955536d2375e1939a124a);
        
    
        var popup_171143fdc4b9907ebd6b306c9e727330 = L.popup({"maxWidth": "100%"});

        
            
                var html_7871edd45a3f1d55ffefe69b157a4e47 = $(`<div id="html_7871edd45a3f1d55ffefe69b157a4e47" style="width: 100.0%; height: 100.0%;">Кронверк Синема Облака</div>`)[0];
                popup_171143fdc4b9907ebd6b306c9e727330.setContent(html_7871edd45a3f1d55ffefe69b157a4e47);
            
        

        marker_186f3e5b4b54a2703c9785ba7a586371.bindPopup(popup_171143fdc4b9907ebd6b306c9e727330)
        ;

        
    
    
            var marker_f23f07e534a07b5bf704824aa600d89f = L.marker(
                [55.820606, 37.388137],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_d5d46fa8d3755da0d1252c61112ada3e = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_f23f07e534a07b5bf704824aa600d89f.setIcon(icon_d5d46fa8d3755da0d1252c61112ada3e);
        
    
        var popup_fd01ca63bdc6e9552d80c149eb4409ac = L.popup({"maxWidth": "100%"});

        
            
                var html_ba4e649c244d43129c73a60d853d41fd = $(`<div id="html_ba4e649c244d43129c73a60d853d41fd" style="width: 100.0%; height: 100.0%;">Каро Vegas 22</div>`)[0];
                popup_fd01ca63bdc6e9552d80c149eb4409ac.setContent(html_ba4e649c244d43129c73a60d853d41fd);
            
        

        marker_f23f07e534a07b5bf704824aa600d89f.bindPopup(popup_fd01ca63bdc6e9552d80c149eb4409ac)
        ;

        
    
    
            var marker_c853fe2a528948a4bfaedbd624161d4c = L.marker(
                [55.692467, 37.527663],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_3ca5e4084b0497f403fd416498d8934c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_c853fe2a528948a4bfaedbd624161d4c.setIcon(icon_3ca5e4084b0497f403fd416498d8934c);
        
    
        var popup_5be59e06b054b93108b5fd6d18aa94a9 = L.popup({"maxWidth": "100%"});

        
            
                var html_7d846c073774cb86d8d813d4c4a6c616 = $(`<div id="html_7d846c073774cb86d8d813d4c4a6c616" style="width: 100.0%; height: 100.0%;">Каро 8 Капитолий Вернадского</div>`)[0];
                popup_5be59e06b054b93108b5fd6d18aa94a9.setContent(html_7d846c073774cb86d8d813d4c4a6c616);
            
        

        marker_c853fe2a528948a4bfaedbd624161d4c.bindPopup(popup_5be59e06b054b93108b5fd6d18aa94a9)
        ;

        
    
    
            var marker_363f3b8e9da4baffeb879d51fa82cdfe = L.marker(
                [55.7775434837405, 37.52310639259031],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_70a0b20d656fbc581ca9af139b65903f = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_363f3b8e9da4baffeb879d51fa82cdfe.setIcon(icon_70a0b20d656fbc581ca9af139b65903f);
        
    
        var popup_8ad494618a8fbcb9dc514c3c2470446f = L.popup({"maxWidth": "100%"});

        
            
                var html_9f01975abae44d39ca28862225c3ed0d = $(`<div id="html_9f01975abae44d39ca28862225c3ed0d" style="width: 100.0%; height: 100.0%;">Формула Кино на Полежаевской</div>`)[0];
                popup_8ad494618a8fbcb9dc514c3c2470446f.setContent(html_9f01975abae44d39ca28862225c3ed0d);
            
        

        marker_363f3b8e9da4baffeb879d51fa82cdfe.bindPopup(popup_8ad494618a8fbcb9dc514c3c2470446f)
        ;

        
    
    
            var marker_45c092ca38545bd71c1345c0bac4afab = L.marker(
                [56.339816, 38.124635],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_8a8b34da08df00ab0ca0cc56464a47e9 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_45c092ca38545bd71c1345c0bac4afab.setIcon(icon_8a8b34da08df00ab0ca0cc56464a47e9);
        
    
        var popup_bffca5f88409220d707507d64fc0eb42 = L.popup({"maxWidth": "100%"});

        
            
                var html_3b1edf5368dc9d1635c7f0353f4ee946 = $(`<div id="html_3b1edf5368dc9d1635c7f0353f4ee946" style="width: 100.0%; height: 100.0%;">Космик Капитолий</div>`)[0];
                popup_bffca5f88409220d707507d64fc0eb42.setContent(html_3b1edf5368dc9d1635c7f0353f4ee946);
            
        

        marker_45c092ca38545bd71c1345c0bac4afab.bindPopup(popup_bffca5f88409220d707507d64fc0eb42)
        ;

        
    
    
            var marker_529f86c3394c7998cfe5054e5974e10e = L.marker(
                [55.78162421676892, 37.71788245767209],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_ccd04809259f706b20f4f99cfc6a9f2b = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_529f86c3394c7998cfe5054e5974e10e.setIcon(icon_ccd04809259f706b20f4f99cfc6a9f2b);
        
    
        var popup_9a19c7842262ab2897a0548e6f3e06e5 = L.popup({"maxWidth": "100%"});

        
            
                var html_c7d63092d9a2b7f3a67df233f9ce7131 = $(`<div id="html_c7d63092d9a2b7f3a67df233f9ce7131" style="width: 100.0%; height: 100.0%;">Родина</div>`)[0];
                popup_9a19c7842262ab2897a0548e6f3e06e5.setContent(html_c7d63092d9a2b7f3a67df233f9ce7131);
            
        

        marker_529f86c3394c7998cfe5054e5974e10e.bindPopup(popup_9a19c7842262ab2897a0548e6f3e06e5)
        ;

        
    
    
            var marker_50a0fbee69ceaa6aa16dbceac9b13497 = L.marker(
                [55.759957, 37.656901],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_31e0058b3e961ecc8ac2cced2ef6d87f = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_50a0fbee69ceaa6aa16dbceac9b13497.setIcon(icon_31e0058b3e961ecc8ac2cced2ef6d87f);
        
    
        var popup_97267277f877c6945b1a0b0a2b34b403 = L.popup({"maxWidth": "100%"});

        
            
                var html_1b07aaf56841b3dbec1f02e7144e0722 = $(`<div id="html_1b07aaf56841b3dbec1f02e7144e0722" style="width: 100.0%; height: 100.0%;">Москино Звезда</div>`)[0];
                popup_97267277f877c6945b1a0b0a2b34b403.setContent(html_1b07aaf56841b3dbec1f02e7144e0722);
            
        

        marker_50a0fbee69ceaa6aa16dbceac9b13497.bindPopup(popup_97267277f877c6945b1a0b0a2b34b403)
        ;

        
    
    
            var marker_0954c1524905dcdd5b727299e4cc434c = L.marker(
                [55.708658, 37.622141],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_bf3c4cb27c0e7d53056fcddf6d3d1b34 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_0954c1524905dcdd5b727299e4cc434c.setIcon(icon_bf3c4cb27c0e7d53056fcddf6d3d1b34);
        
    
        var popup_d926cb2e306a87256ac14083335c6ade = L.popup({"maxWidth": "100%"});

        
            
                var html_4210f8fd12462e063061e67484faaca8 = $(`<div id="html_4210f8fd12462e063061e67484faaca8" style="width: 100.0%; height: 100.0%;">Синема Стар в ТРЦ Ереван Плаза</div>`)[0];
                popup_d926cb2e306a87256ac14083335c6ade.setContent(html_4210f8fd12462e063061e67484faaca8);
            
        

        marker_0954c1524905dcdd5b727299e4cc434c.bindPopup(popup_d926cb2e306a87256ac14083335c6ade)
        ;

        
    
    
            var marker_6b912490f2aabc104f7b55271985cabf = L.marker(
                [55.753966, 37.601627],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_018bc56df5f217aa30c2cf09b5ceaf3b = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_6b912490f2aabc104f7b55271985cabf.setIcon(icon_018bc56df5f217aa30c2cf09b5ceaf3b);
        
    
        var popup_d627220f8e3db97678a646b00ec26a5e = L.popup({"maxWidth": "100%"});

        
            
                var html_6845a631fd38065bc031575fb8403aa2 = $(`<div id="html_6845a631fd38065bc031575fb8403aa2" style="width: 100.0%; height: 100.0%;">Кинозал Домжур</div>`)[0];
                popup_d627220f8e3db97678a646b00ec26a5e.setContent(html_6845a631fd38065bc031575fb8403aa2);
            
        

        marker_6b912490f2aabc104f7b55271985cabf.bindPopup(popup_d627220f8e3db97678a646b00ec26a5e)
        ;

        
    
    
            var marker_7002fc9c77ff92a2f9305ca3cad61569 = L.marker(
                [55.612146, 37.606918],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_95b77a7235755fd8c873a8be7851ad1c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_7002fc9c77ff92a2f9305ca3cad61569.setIcon(icon_95b77a7235755fd8c873a8be7851ad1c);
        
    
        var popup_4a675c01f0a544abbcb37cac753797b1 = L.popup({"maxWidth": "100%"});

        
            
                var html_04e64a7d708a7bdd06ebeca970aaacc6 = $(`<div id="html_04e64a7d708a7bdd06ebeca970aaacc6" style="width: 100.0%; height: 100.0%;">Киномакс-Пражская</div>`)[0];
                popup_4a675c01f0a544abbcb37cac753797b1.setContent(html_04e64a7d708a7bdd06ebeca970aaacc6);
            
        

        marker_7002fc9c77ff92a2f9305ca3cad61569.bindPopup(popup_4a675c01f0a544abbcb37cac753797b1)
        ;

        
    
    
            var marker_10af96cca90518eab1a13d8c0020c844 = L.marker(
                [55.61991, 37.509873],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_b460a9b38d7846de5e64643c3c07bb02 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_10af96cca90518eab1a13d8c0020c844.setIcon(icon_b460a9b38d7846de5e64643c3c07bb02);
        
    
        var popup_dc564e04b1187f19830ff63a68e3e3b4 = L.popup({"maxWidth": "100%"});

        
            
                var html_a69633f99d1310d02ef374b72a9ee274 = $(`<div id="html_a69633f99d1310d02ef374b72a9ee274" style="width: 100.0%; height: 100.0%;">Каро 6 Теплый Стан</div>`)[0];
                popup_dc564e04b1187f19830ff63a68e3e3b4.setContent(html_a69633f99d1310d02ef374b72a9ee274);
            
        

        marker_10af96cca90518eab1a13d8c0020c844.bindPopup(popup_dc564e04b1187f19830ff63a68e3e3b4)
        ;

        
    
    
            var marker_d5b3d9dc5f6ee8eab2118453a353bb9a = L.marker(
                [55.651379, 37.612389],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_c4752e85e0f60774c9a411b0b6d5b267 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d5b3d9dc5f6ee8eab2118453a353bb9a.setIcon(icon_c4752e85e0f60774c9a411b0b6d5b267);
        
    
        var popup_561f853a4366f126bfcee9153a2ab1bf = L.popup({"maxWidth": "100%"});

        
            
                var html_2d96f9477a4002042235f96011678104 = $(`<div id="html_2d96f9477a4002042235f96011678104" style="width: 100.0%; height: 100.0%;">Каро 4 Ангара</div>`)[0];
                popup_561f853a4366f126bfcee9153a2ab1bf.setContent(html_2d96f9477a4002042235f96011678104);
            
        

        marker_d5b3d9dc5f6ee8eab2118453a353bb9a.bindPopup(popup_561f853a4366f126bfcee9153a2ab1bf)
        ;

        
    
    
            var marker_739a5a11da45134d912e897adf8c5d39 = L.marker(
                [55.909895, 37.540001],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_280cdc182087f70757c8d6ae14adaf7a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_739a5a11da45134d912e897adf8c5d39.setIcon(icon_280cdc182087f70757c8d6ae14adaf7a);
        
    
        var popup_e5b6b50e55b04481a3e302cb7a35f207 = L.popup({"maxWidth": "100%"});

        
            
                var html_264bf1f28bb8cbc6d224e32076ac042d = $(`<div id="html_264bf1f28bb8cbc6d224e32076ac042d" style="width: 100.0%; height: 100.0%;">Синема Стар Дмитровка</div>`)[0];
                popup_e5b6b50e55b04481a3e302cb7a35f207.setContent(html_264bf1f28bb8cbc6d224e32076ac042d);
            
        

        marker_739a5a11da45134d912e897adf8c5d39.bindPopup(popup_e5b6b50e55b04481a3e302cb7a35f207)
        ;

        
    
    
            var marker_302e4a466ba8663d9d5b4b0eae02afc6 = L.marker(
                [55.6542748798214, 37.8448880017114],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_8aa6a3509c20e7edbd10d51c680b6ae6 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_302e4a466ba8663d9d5b4b0eae02afc6.setIcon(icon_8aa6a3509c20e7edbd10d51c680b6ae6);
        
    
        var popup_ae6d4b6fd88c62ff98f31947c8f30523 = L.popup({"maxWidth": "100%"});

        
            
                var html_6451ee502648d4eccd93b3ee4d3b1cde = $(`<div id="html_6451ee502648d4eccd93b3ee4d3b1cde" style="width: 100.0%; height: 100.0%;">Синема Парк Мега Белая Дача</div>`)[0];
                popup_ae6d4b6fd88c62ff98f31947c8f30523.setContent(html_6451ee502648d4eccd93b3ee4d3b1cde);
            
        

        marker_302e4a466ba8663d9d5b4b0eae02afc6.bindPopup(popup_ae6d4b6fd88c62ff98f31947c8f30523)
        ;

        
    
    
            var marker_7b5332cf048f19725d1a476a10386652 = L.marker(
                [55.743996, 37.508179],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_9737ec8d1a6197bc29ddfadf5c659cb1 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_7b5332cf048f19725d1a476a10386652.setIcon(icon_9737ec8d1a6197bc29ddfadf5c659cb1);
        
    
        var popup_1f0915181bba930a9cecdbe49675abde = L.popup({"maxWidth": "100%"});

        
            
                var html_1ac2a4bf49efac0794c05c5e18ac34fa = $(`<div id="html_1ac2a4bf49efac0794c05c5e18ac34fa" style="width: 100.0%; height: 100.0%;">Синема Парк Филион на Багратионовской</div>`)[0];
                popup_1f0915181bba930a9cecdbe49675abde.setContent(html_1ac2a4bf49efac0794c05c5e18ac34fa);
            
        

        marker_7b5332cf048f19725d1a476a10386652.bindPopup(popup_1f0915181bba930a9cecdbe49675abde)
        ;

        
    
    
            var marker_f9f11ad9a27b400a9ea3c27e92460e11 = L.marker(
                [55.889881, 37.537676],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a1141e8c365b94ad890c86de30569887 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_f9f11ad9a27b400a9ea3c27e92460e11.setIcon(icon_a1141e8c365b94ad890c86de30569887);
        
    
        var popup_7ad8bf80efdc078776e1713fd402d577 = L.popup({"maxWidth": "100%"});

        
            
                var html_102834857f83e10fc8a5c40ad0853f60 = $(`<div id="html_102834857f83e10fc8a5c40ad0853f60" style="width: 100.0%; height: 100.0%;">Зиг Заг</div>`)[0];
                popup_7ad8bf80efdc078776e1713fd402d577.setContent(html_102834857f83e10fc8a5c40ad0853f60);
            
        

        marker_f9f11ad9a27b400a9ea3c27e92460e11.bindPopup(popup_7ad8bf80efdc078776e1713fd402d577)
        ;

        
    
    
            var marker_2c27f623a769c9526931502512e103af = L.marker(
                [55.714648, 37.883572],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_747aa43f3f5a7c685de2cbcf241cc4a6 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_2c27f623a769c9526931502512e103af.setIcon(icon_747aa43f3f5a7c685de2cbcf241cc4a6);
        
    
        var popup_11e75cbbb789ce40370675efacfb70c0 = L.popup({"maxWidth": "100%"});

        
            
                var html_1f7ef2071cb0b0b40a3366f01cf477b0 = $(`<div id="html_1f7ef2071cb0b0b40a3366f01cf477b0" style="width: 100.0%; height: 100.0%;">Silver Cinema</div>`)[0];
                popup_11e75cbbb789ce40370675efacfb70c0.setContent(html_1f7ef2071cb0b0b40a3366f01cf477b0);
            
        

        marker_2c27f623a769c9526931502512e103af.bindPopup(popup_11e75cbbb789ce40370675efacfb70c0)
        ;

        
    
    
            var marker_027a402820308cc06401ad8c5bc82844 = L.marker(
                [55.85275087112515, 38.44493108998813],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_81071069a20c64dec09021068a913302 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_027a402820308cc06401ad8c5bc82844.setIcon(icon_81071069a20c64dec09021068a913302);
        
    
        var popup_675b7f56ba925adefccce01c25b33822 = L.popup({"maxWidth": "100%"});

        
            
                var html_8221af003fd4bbd30edeb3556fe33048 = $(`<div id="html_8221af003fd4bbd30edeb3556fe33048" style="width: 100.0%; height: 100.0%;">Синема Сити (Ногинск)</div>`)[0];
                popup_675b7f56ba925adefccce01c25b33822.setContent(html_8221af003fd4bbd30edeb3556fe33048);
            
        

        marker_027a402820308cc06401ad8c5bc82844.bindPopup(popup_675b7f56ba925adefccce01c25b33822)
        ;

        
    
    
            var marker_d6afc31d46d85e76a4a16a841c8306d5 = L.marker(
                [55.7827070829488, 37.72038772209021],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_6049e7abd0c9e5318921cfa24f88a7ac = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d6afc31d46d85e76a4a16a841c8306d5.setIcon(icon_6049e7abd0c9e5318921cfa24f88a7ac);
        
    
        var popup_d79c65a8ddc4b2a041dcd2fc74426b5b = L.popup({"maxWidth": "100%"});

        
            
                var html_2b6d537a5e302e212c6126d2499a1ed3 = $(`<div id="html_2b6d537a5e302e212c6126d2499a1ed3" style="width: 100.0%; height: 100.0%;">Кронверк Синема Семеновский</div>`)[0];
                popup_d79c65a8ddc4b2a041dcd2fc74426b5b.setContent(html_2b6d537a5e302e212c6126d2499a1ed3);
            
        

        marker_d6afc31d46d85e76a4a16a841c8306d5.bindPopup(popup_d79c65a8ddc4b2a041dcd2fc74426b5b)
        ;

        
    
    
            var marker_46dc72654fd298e1894acd17af6a296d = L.marker(
                [55.921257, 37.99176030000001],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_aacb9a1abaac0b78edb900242ed178f9 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_46dc72654fd298e1894acd17af6a296d.setIcon(icon_aacb9a1abaac0b78edb900242ed178f9);
        
    
        var popup_db30f6ef9a94b4b658dc1d75825617ba = L.popup({"maxWidth": "100%"});

        
            
                var html_be0db8ec6614ecfa717b1224ccb542a6 = $(`<div id="html_be0db8ec6614ecfa717b1224ccb542a6" style="width: 100.0%; height: 100.0%;">5 звезд (Щелково)</div>`)[0];
                popup_db30f6ef9a94b4b658dc1d75825617ba.setContent(html_be0db8ec6614ecfa717b1224ccb542a6);
            
        

        marker_46dc72654fd298e1894acd17af6a296d.bindPopup(popup_db30f6ef9a94b4b658dc1d75825617ba)
        ;

        
    
    
            var marker_84889aac035d013a9762b7ed16c319fb = L.marker(
                [55.795433, 37.617141],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a61013c2f5f804981bc14bbbd85b6277 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_84889aac035d013a9762b7ed16c319fb.setIcon(icon_a61013c2f5f804981bc14bbbd85b6277);
        
    
        var popup_94554205f3e4d6cb7a85ccba0fbbffad = L.popup({"maxWidth": "100%"});

        
            
                var html_fbeb82bd8f7caa3513cc0712cf3c05ee = $(`<div id="html_fbeb82bd8f7caa3513cc0712cf3c05ee" style="width: 100.0%; height: 100.0%;">Синема Стар Марьина Роща</div>`)[0];
                popup_94554205f3e4d6cb7a85ccba0fbbffad.setContent(html_fbeb82bd8f7caa3513cc0712cf3c05ee);
            
        

        marker_84889aac035d013a9762b7ed16c319fb.bindPopup(popup_94554205f3e4d6cb7a85ccba0fbbffad)
        ;

        
    
    
            var marker_9b663302f5f702abb23d2b5692c82100 = L.marker(
                [55.861969, 37.676825],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_4f7475041db40b69348b39d2c2aeb328 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_9b663302f5f702abb23d2b5692c82100.setIcon(icon_4f7475041db40b69348b39d2c2aeb328);
        
    
        var popup_29e78353c870b90a05601a78068ba5cc = L.popup({"maxWidth": "100%"});

        
            
                var html_6add9610c935c0480ee368d5791214db = $(`<div id="html_6add9610c935c0480ee368d5791214db" style="width: 100.0%; height: 100.0%;">Москино Вымпел</div>`)[0];
                popup_29e78353c870b90a05601a78068ba5cc.setContent(html_6add9610c935c0480ee368d5791214db);
            
        

        marker_9b663302f5f702abb23d2b5692c82100.bindPopup(popup_29e78353c870b90a05601a78068ba5cc)
        ;

        
    
    
            var marker_1d9d931c76b8d4b78a8e9e8bc3c0b44c = L.marker(
                [56.303856, 38.133214],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_74e88b04a4ee91b68e3c88de29bdde1b = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_1d9d931c76b8d4b78a8e9e8bc3c0b44c.setIcon(icon_74e88b04a4ee91b68e3c88de29bdde1b);
        
    
        var popup_f6513423a6116d73186c8f28012efa5c = L.popup({"maxWidth": "100%"});

        
            
                var html_9138b7f2f74d8f5c123cd121ec192ea6 = $(`<div id="html_9138b7f2f74d8f5c123cd121ec192ea6" style="width: 100.0%; height: 100.0%;">Космик Счастливая семья (Сергиев Посад)</div>`)[0];
                popup_f6513423a6116d73186c8f28012efa5c.setContent(html_9138b7f2f74d8f5c123cd121ec192ea6);
            
        

        marker_1d9d931c76b8d4b78a8e9e8bc3c0b44c.bindPopup(popup_f6513423a6116d73186c8f28012efa5c)
        ;

        
    
    
            var marker_b2ce04cc559334cd0e393178e9b56f17 = L.marker(
                [55.8867579907734, 37.65942913128288],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_67735d26bfb1707aa49ec980dd39c4cd = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_b2ce04cc559334cd0e393178e9b56f17.setIcon(icon_67735d26bfb1707aa49ec980dd39c4cd);
        
    
        var popup_387679929785c01ec932f78050db61f7 = L.popup({"maxWidth": "100%"});

        
            
                var html_9e87fa8dec7f69268268e73c962e9583 = $(`<div id="html_9e87fa8dec7f69268268e73c962e9583" style="width: 100.0%; height: 100.0%;">Формула Кино Ладога</div>`)[0];
                popup_387679929785c01ec932f78050db61f7.setContent(html_9e87fa8dec7f69268268e73c962e9583);
            
        

        marker_b2ce04cc559334cd0e393178e9b56f17.bindPopup(popup_387679929785c01ec932f78050db61f7)
        ;

        
    
    
            var marker_2448ae1bb795ebbd772021c34522495f = L.marker(
                [55.799847586129, 37.4830365479264],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_324b3e0d912d3c4395c58e19886c966d = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_2448ae1bb795ebbd772021c34522495f.setIcon(icon_324b3e0d912d3c4395c58e19886c966d);
        
    
        var popup_0794f897dd3e3ea7030c36f2112bc76f = L.popup({"maxWidth": "100%"});

        
            
                var html_a0e819a685e15963b5a0124eae51a25c = $(`<div id="html_a0e819a685e15963b5a0124eae51a25c" style="width: 100.0%; height: 100.0%;">Синема Парк Пятая Авеню на Октябрьском Поле</div>`)[0];
                popup_0794f897dd3e3ea7030c36f2112bc76f.setContent(html_a0e819a685e15963b5a0124eae51a25c);
            
        

        marker_2448ae1bb795ebbd772021c34522495f.bindPopup(popup_0794f897dd3e3ea7030c36f2112bc76f)
        ;

        
    
    
            var marker_ba14ef3ff4acc6b022f464613eaaabf8 = L.marker(
                [55.606482441909, 37.4898321926866],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_fdbc1ba679d2999bac20016cbcf5433c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_ba14ef3ff4acc6b022f464613eaaabf8.setIcon(icon_fdbc1ba679d2999bac20016cbcf5433c);
        
    
        var popup_1b674fbc6aad445a7f29844ba7fd078d = L.popup({"maxWidth": "100%"});

        
            
                var html_3e63dc18e8d1007c3d7b988ff7a537a8 = $(`<div id="html_3e63dc18e8d1007c3d7b988ff7a537a8" style="width: 100.0%; height: 100.0%;">Синема Парк Мега Теплый Стан</div>`)[0];
                popup_1b674fbc6aad445a7f29844ba7fd078d.setContent(html_3e63dc18e8d1007c3d7b988ff7a537a8);
            
        

        marker_ba14ef3ff4acc6b022f464613eaaabf8.bindPopup(popup_1b674fbc6aad445a7f29844ba7fd078d)
        ;

        
    
    
            var marker_546dc4204c5d50b8bb15ac3f0e544dd2 = L.marker(
                [55.73631217631481, 37.594152981091725],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_2f1b7ea5d532bdde5425f8b8712935dc = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_546dc4204c5d50b8bb15ac3f0e544dd2.setIcon(icon_2f1b7ea5d532bdde5425f8b8712935dc);
        
    
        var popup_72b71de609989a85a25d29909dd48d8e = L.popup({"maxWidth": "100%"});

        
            
                var html_522ec68996a5b111b2319ff60a1a80e8 = $(`<div id="html_522ec68996a5b111b2319ff60a1a80e8" style="width: 100.0%; height: 100.0%;">Центр документального кино</div>`)[0];
                popup_72b71de609989a85a25d29909dd48d8e.setContent(html_522ec68996a5b111b2319ff60a1a80e8);
            
        

        marker_546dc4204c5d50b8bb15ac3f0e544dd2.bindPopup(popup_72b71de609989a85a25d29909dd48d8e)
        ;

        
    
    
            var marker_50134b83cbb8a543e99a8cf145c0d3d9 = L.marker(
                [55.606856, 37.536292],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_33034424b89f9d2ace219b906075954c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_50134b83cbb8a543e99a8cf145c0d3d9.setIcon(icon_33034424b89f9d2ace219b906075954c);
        
    
        var popup_e37035a1af3502794d12ae9dd7ca2e36 = L.popup({"maxWidth": "100%"});

        
            
                var html_45e5061ee5b6d2e19f1e2ea8ad66dc97 = $(`<div id="html_45e5061ee5b6d2e19f1e2ea8ad66dc97" style="width: 100.0%; height: 100.0%;">Космик Ясенево</div>`)[0];
                popup_e37035a1af3502794d12ae9dd7ca2e36.setContent(html_45e5061ee5b6d2e19f1e2ea8ad66dc97);
            
        

        marker_50134b83cbb8a543e99a8cf145c0d3d9.bindPopup(popup_e37035a1af3502794d12ae9dd7ca2e36)
        ;

        
    
    
            var marker_e363264389775ef49eed51c43b93d65c = L.marker(
                [55.818756, 37.636753],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_1c48a20c0bf4705dde2eb4deb3ed30cf = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e363264389775ef49eed51c43b93d65c.setIcon(icon_1c48a20c0bf4705dde2eb4deb3ed30cf);
        
    
        var popup_5062d86506ff84df8b888d429376093a = L.popup({"maxWidth": "100%"});

        
            
                var html_6ae60ac4d4fa59eda14a8530f7f1ee78 = $(`<div id="html_6ae60ac4d4fa59eda14a8530f7f1ee78" style="width: 100.0%; height: 100.0%;">Москино Космос</div>`)[0];
                popup_5062d86506ff84df8b888d429376093a.setContent(html_6ae60ac4d4fa59eda14a8530f7f1ee78);
            
        

        marker_e363264389775ef49eed51c43b93d65c.bindPopup(popup_5062d86506ff84df8b888d429376093a)
        ;

        
    
    
            var marker_1c2a6609b19c4349c86ae31965b1ebb5 = L.marker(
                [55.846052, 37.44284],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_2e424889583d0340f9a440c765406bba = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_1c2a6609b19c4349c86ae31965b1ebb5.setIcon(icon_2e424889583d0340f9a440c765406bba);
        
    
        var popup_e866a8c8156ff2cbae3af21ae9b10b1d = L.popup({"maxWidth": "100%"});

        
            
                var html_4cd470938b4950315f4e965e3e9e6521 = $(`<div id="html_4cd470938b4950315f4e965e3e9e6521" style="width: 100.0%; height: 100.0%;">Москино Полет</div>`)[0];
                popup_e866a8c8156ff2cbae3af21ae9b10b1d.setContent(html_4cd470938b4950315f4e965e3e9e6521);
            
        

        marker_1c2a6609b19c4349c86ae31965b1ebb5.bindPopup(popup_e866a8c8156ff2cbae3af21ae9b10b1d)
        ;

        
    
    
            var marker_c94675ee9b335401bd15b1090c82c9d5 = L.marker(
                [55.582986, 37.59524],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_860d9b78552879bcdde6da31f0fcb895 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_c94675ee9b335401bd15b1090c82c9d5.setIcon(icon_860d9b78552879bcdde6da31f0fcb895);
        
    
        var popup_862490f0602e9fad2b3a481ef694d791 = L.popup({"maxWidth": "100%"});

        
            
                var html_3c3ccbb097ffe612fad77f9a81c94a0a = $(`<div id="html_3c3ccbb097ffe612fad77f9a81c94a0a" style="width: 100.0%; height: 100.0%;">Космик Аннино</div>`)[0];
                popup_862490f0602e9fad2b3a481ef694d791.setContent(html_3c3ccbb097ffe612fad77f9a81c94a0a);
            
        

        marker_c94675ee9b335401bd15b1090c82c9d5.bindPopup(popup_862490f0602e9fad2b3a481ef694d791)
        ;

        
    
    
            var marker_0eb1ad39b62532cbb8aa5690fb8c7309 = L.marker(
                [55.710687, 37.6751],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_e18e0b0bf45658deb045436e38ae0ca8 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_0eb1ad39b62532cbb8aa5690fb8c7309.setIcon(icon_e18e0b0bf45658deb045436e38ae0ca8);
        
    
        var popup_3c4a71e3c14b8d3c19a9b180abd4b8aa = L.popup({"maxWidth": "100%"});

        
            
                var html_115537063a4ca2e7c3c45862bb9559e1 = $(`<div id="html_115537063a4ca2e7c3c45862bb9559e1" style="width: 100.0%; height: 100.0%;">Киномакс-Мозаика</div>`)[0];
                popup_3c4a71e3c14b8d3c19a9b180abd4b8aa.setContent(html_115537063a4ca2e7c3c45862bb9559e1);
            
        

        marker_0eb1ad39b62532cbb8aa5690fb8c7309.bindPopup(popup_3c4a71e3c14b8d3c19a9b180abd4b8aa)
        ;

        
    
    
            var marker_c30ffdb06f43132b538aa3108ac569a8 = L.marker(
                [55.856335, 37.653345],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_796b606b67ac5486e692b4fa5c8040ca = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_c30ffdb06f43132b538aa3108ac569a8.setIcon(icon_796b606b67ac5486e692b4fa5c8040ca);
        
    
        var popup_10666fcd62afd09564732573535f8438 = L.popup({"maxWidth": "100%"});

        
            
                var html_8359a71ed414a5df1ca3c669015e9ea5 = $(`<div id="html_8359a71ed414a5df1ca3c669015e9ea5" style="width: 100.0%; height: 100.0%;">Час Кино (Свиблово)</div>`)[0];
                popup_10666fcd62afd09564732573535f8438.setContent(html_8359a71ed414a5df1ca3c669015e9ea5);
            
        

        marker_c30ffdb06f43132b538aa3108ac569a8.bindPopup(popup_10666fcd62afd09564732573535f8438)
        ;

        
    
    
            var marker_31e54ddcd14918e00048b641e1ba4a34 = L.marker(
                [55.764408, 37.705591],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_8cb0ecc9a5023426c480b73300712c31 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_31e54ddcd14918e00048b641e1ba4a34.setIcon(icon_8cb0ecc9a5023426c480b73300712c31);
        
    
        var popup_2851e7cf39a5a949729cd544695237fe = L.popup({"maxWidth": "100%"});

        
            
                var html_19a9c7f954b6e43669f579c02b35598d = $(`<div id="html_19a9c7f954b6e43669f579c02b35598d" style="width: 100.0%; height: 100.0%;">Москино Спутник</div>`)[0];
                popup_2851e7cf39a5a949729cd544695237fe.setContent(html_19a9c7f954b6e43669f579c02b35598d);
            
        

        marker_31e54ddcd14918e00048b641e1ba4a34.bindPopup(popup_2851e7cf39a5a949729cd544695237fe)
        ;

        
    
    
            var marker_af0f3e2bb95f7cd550d40e9c0f010705 = L.marker(
                [55.621404, 37.713953],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_23b3b72038dd7c8bf322a59fb9bf35b5 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_af0f3e2bb95f7cd550d40e9c0f010705.setIcon(icon_23b3b72038dd7c8bf322a59fb9bf35b5);
        
    
        var popup_725619719a8ce721aa1ebde5aa9a3c5f = L.popup({"maxWidth": "100%"});

        
            
                var html_65eb18d847faae238191f5c3edbe4b23 = $(`<div id="html_65eb18d847faae238191f5c3edbe4b23" style="width: 100.0%; height: 100.0%;">Киномакс-Титан</div>`)[0];
                popup_725619719a8ce721aa1ebde5aa9a3c5f.setContent(html_65eb18d847faae238191f5c3edbe4b23);
            
        

        marker_af0f3e2bb95f7cd550d40e9c0f010705.bindPopup(popup_725619719a8ce721aa1ebde5aa9a3c5f)
        ;

        
    
    
            var marker_ecb48a7dd668df18a5dd2a04ec3ef49a = L.marker(
                [55.734497121927646, 37.67086862698363],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_f114e91ae0eb0d9ef9e8483d97758ee0 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_ecb48a7dd668df18a5dd2a04ec3ef49a.setIcon(icon_f114e91ae0eb0d9ef9e8483d97758ee0);
        
    
        var popup_a405c3515ff81693c3f88cf201e267bd = L.popup({"maxWidth": "100%"});

        
            
                var html_5cbde67d2d47bfd557a979b202dfd88b = $(`<div id="html_5cbde67d2d47bfd557a979b202dfd88b" style="width: 100.0%; height: 100.0%;">Победа</div>`)[0];
                popup_a405c3515ff81693c3f88cf201e267bd.setContent(html_5cbde67d2d47bfd557a979b202dfd88b);
            
        

        marker_ecb48a7dd668df18a5dd2a04ec3ef49a.bindPopup(popup_a405c3515ff81693c3f88cf201e267bd)
        ;

        
    
    
            var marker_524ce2f84b2ef982eb1ed525e5c98f58 = L.marker(
                [55.846051, 37.661055],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_54a56e39722878cb3764dac9a97a7cbd = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_524ce2f84b2ef982eb1ed525e5c98f58.setIcon(icon_54a56e39722878cb3764dac9a97a7cbd);
        
    
        var popup_bd912ecd90c440e4892f9b27910dcfaa = L.popup({"maxWidth": "100%"});

        
            
                var html_92fe72d4fd1dfe85ea03c22403c233b1 = $(`<div id="html_92fe72d4fd1dfe85ea03c22403c233b1" style="width: 100.0%; height: 100.0%;">Мираж Синема Европолис</div>`)[0];
                popup_bd912ecd90c440e4892f9b27910dcfaa.setContent(html_92fe72d4fd1dfe85ea03c22403c233b1);
            
        

        marker_524ce2f84b2ef982eb1ed525e5c98f58.bindPopup(popup_bd912ecd90c440e4892f9b27910dcfaa)
        ;

        
    
    
            var marker_aeafd8115f94804e2b30d085d416adc8 = L.marker(
                [55.799492657870736, 37.273697867736814],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_1668a2ddb53bdd89db3b69496fa4e4b8 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_aeafd8115f94804e2b30d085d416adc8.setIcon(icon_1668a2ddb53bdd89db3b69496fa4e4b8);
        
    
        var popup_4cb13a042fc199641b61f1be856c61f1 = L.popup({"maxWidth": "100%"});

        
            
                var html_013cecce3f9d81fe5a4d43718bfe6945 = $(`<div id="html_013cecce3f9d81fe5a4d43718bfe6945" style="width: 100.0%; height: 100.0%;">Киномакс Рига-молл</div>`)[0];
                popup_4cb13a042fc199641b61f1be856c61f1.setContent(html_013cecce3f9d81fe5a4d43718bfe6945);
            
        

        marker_aeafd8115f94804e2b30d085d416adc8.bindPopup(popup_4cb13a042fc199641b61f1be856c61f1)
        ;

        
    
    
            var marker_d518210191b9b0b6116a46e41ce489fb = L.marker(
                [55.63714362850061, 37.59914796857231],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_8e337331abeda095e0f41b91dd6a743d = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d518210191b9b0b6116a46e41ce489fb.setIcon(icon_8e337331abeda095e0f41b91dd6a743d);
        
    
        var popup_080e13a097838029159807444c29964e = L.popup({"maxWidth": "100%"});

        
            
                var html_2d9257667ca266b0d540b2f3791ad33e = $(`<div id="html_2d9257667ca266b0d540b2f3791ad33e" style="width: 100.0%; height: 100.0%;">Формула Кино Чертаново</div>`)[0];
                popup_080e13a097838029159807444c29964e.setContent(html_2d9257667ca266b0d540b2f3791ad33e);
            
        

        marker_d518210191b9b0b6116a46e41ce489fb.bindPopup(popup_080e13a097838029159807444c29964e)
        ;

        
    
    
            var marker_6bca72ef9de99ec8af038fa68f848788 = L.marker(
                [55.685927, 37.718601],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_6691cedb9798cb123fc2a06376895197 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_6bca72ef9de99ec8af038fa68f848788.setIcon(icon_6691cedb9798cb123fc2a06376895197);
        
    
        var popup_e36c375be0906e41bce394f172492668 = L.popup({"maxWidth": "100%"});

        
            
                var html_8afa01de33d4fba37e7b28191696531d = $(`<div id="html_8afa01de33d4fba37e7b28191696531d" style="width: 100.0%; height: 100.0%;">Москино Тула</div>`)[0];
                popup_e36c375be0906e41bce394f172492668.setContent(html_8afa01de33d4fba37e7b28191696531d);
            
        

        marker_6bca72ef9de99ec8af038fa68f848788.bindPopup(popup_e36c375be0906e41bce394f172492668)
        ;

        
    
    
            var marker_27020e98478d72b14f29d3307ab3b87b = L.marker(
                [55.653644, 37.620698],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_e499cdc442f097ef4a7cd2819a89f05c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_27020e98478d72b14f29d3307ab3b87b.setIcon(icon_e499cdc442f097ef4a7cd2819a89f05c);
        
    
        var popup_f42eebc41b37304055dad0c29300f6ee = L.popup({"maxWidth": "100%"});

        
            
                var html_cdaeb7e3a9431b842b5286906d631b86 = $(`<div id="html_cdaeb7e3a9431b842b5286906d631b86" style="width: 100.0%; height: 100.0%;">Киноквартал на Варшавке</div>`)[0];
                popup_f42eebc41b37304055dad0c29300f6ee.setContent(html_cdaeb7e3a9431b842b5286906d631b86);
            
        

        marker_27020e98478d72b14f29d3307ab3b87b.bindPopup(popup_f42eebc41b37304055dad0c29300f6ee)
        ;

        
    
    
            var marker_e12e9968b901081c665213d1c9e40fa5 = L.marker(
                [55.618062, 37.507526],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_0843219161511b2c6330754bac79361a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e12e9968b901081c665213d1c9e40fa5.setIcon(icon_0843219161511b2c6330754bac79361a);
        
    
        var popup_45ce9757e56c09b9f261cb6d63cf1a72 = L.popup({"maxWidth": "100%"});

        
            
                var html_72f1ffb50a5cd23b2def7419829b74f2 = $(`<div id="html_72f1ffb50a5cd23b2def7419829b74f2" style="width: 100.0%; height: 100.0%;">Синема Стар Принц Плаза</div>`)[0];
                popup_45ce9757e56c09b9f261cb6d63cf1a72.setContent(html_72f1ffb50a5cd23b2def7419829b74f2);
            
        

        marker_e12e9968b901081c665213d1c9e40fa5.bindPopup(popup_45ce9757e56c09b9f261cb6d63cf1a72)
        ;

        
    
    
            var marker_7e0df41a2cc5cfb05e7310234be32c96 = L.marker(
                [55.710923, 37.731341],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_fb5efdcf808398f86107e6c70a4cfc17 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_7e0df41a2cc5cfb05e7310234be32c96.setIcon(icon_fb5efdcf808398f86107e6c70a4cfc17);
        
    
        var popup_07d908015ad2aaddb588037b04561f6d = L.popup({"maxWidth": "100%"});

        
            
                var html_40b6a4fa6319e546d00c18326307f0b5 = $(`<div id="html_40b6a4fa6319e546d00c18326307f0b5" style="width: 100.0%; height: 100.0%;">Москино Молодежный</div>`)[0];
                popup_07d908015ad2aaddb588037b04561f6d.setContent(html_40b6a4fa6319e546d00c18326307f0b5);
            
        

        marker_7e0df41a2cc5cfb05e7310234be32c96.bindPopup(popup_07d908015ad2aaddb588037b04561f6d)
        ;

        
    
    
            var marker_94ae9a768161d9ad70a8ee60a13a980d = L.marker(
                [55.7446, 37.566102],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_637322be915e8c73026621d169639414 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_94ae9a768161d9ad70a8ee60a13a980d.setIcon(icon_637322be915e8c73026621d169639414);
        
    
        var popup_a9a15c8e69830a9bb20c9fe013947d69 = L.popup({"maxWidth": "100%"});

        
            
                var html_71cfe3d377bb06b3f77ccec9f2a0ea18 = $(`<div id="html_71cfe3d377bb06b3f77ccec9f2a0ea18" style="width: 100.0%; height: 100.0%;">Синема Парк Европейский</div>`)[0];
                popup_a9a15c8e69830a9bb20c9fe013947d69.setContent(html_71cfe3d377bb06b3f77ccec9f2a0ea18);
            
        

        marker_94ae9a768161d9ad70a8ee60a13a980d.bindPopup(popup_a9a15c8e69830a9bb20c9fe013947d69)
        ;

        
    
    
            var marker_739373e50bb3bfdd51cb562285b8bc77 = L.marker(
                [55.813093, 38.430482],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_b6434025c033fb6214f1a9e0e8165800 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_739373e50bb3bfdd51cb562285b8bc77.setIcon(icon_b6434025c033fb6214f1a9e0e8165800);
        
    
        var popup_8569838d69d1449c633d163cd7dab1c4 = L.popup({"maxWidth": "100%"});

        
            
                var html_2a14e0477af3babfa5a2066696126036 = $(`<div id="html_2a14e0477af3babfa5a2066696126036" style="width: 100.0%; height: 100.0%;">Галерея Кино</div>`)[0];
                popup_8569838d69d1449c633d163cd7dab1c4.setContent(html_2a14e0477af3babfa5a2066696126036);
            
        

        marker_739373e50bb3bfdd51cb562285b8bc77.bindPopup(popup_8569838d69d1449c633d163cd7dab1c4)
        ;

        
    
    
            var marker_936928cdfd634f55d1e910f304c00671 = L.marker(
                [55.5244942, 37.51751360000003],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a90dd522ff16f19d9478a67204df8075 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_936928cdfd634f55d1e910f304c00671.setIcon(icon_a90dd522ff16f19d9478a67204df8075);
        
    
        var popup_fbe86746ae605337c1efa3cce03decb7 = L.popup({"maxWidth": "100%"});

        
            
                var html_39a942352a091ec84410b0ee0811373d = $(`<div id="html_39a942352a091ec84410b0ee0811373d" style="width: 100.0%; height: 100.0%;">Синема Парк Бутово Молл</div>`)[0];
                popup_fbe86746ae605337c1efa3cce03decb7.setContent(html_39a942352a091ec84410b0ee0811373d);
            
        

        marker_936928cdfd634f55d1e910f304c00671.bindPopup(popup_fbe86746ae605337c1efa3cce03decb7)
        ;

        
    
    
            var marker_e38e642dd91da8b25f24f86a134afda6 = L.marker(
                [55.751817, 37.715999],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_53118069c67813fbc42964fa56803656 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e38e642dd91da8b25f24f86a134afda6.setIcon(icon_53118069c67813fbc42964fa56803656);
        
    
        var popup_b9df20d11dfdb7135579303f1b398ea3 = L.popup({"maxWidth": "100%"});

        
            
                var html_62827534d858830639d73db3f24c4bcb = $(`<div id="html_62827534d858830639d73db3f24c4bcb" style="width: 100.0%; height: 100.0%;">Москино Факел</div>`)[0];
                popup_b9df20d11dfdb7135579303f1b398ea3.setContent(html_62827534d858830639d73db3f24c4bcb);
            
        

        marker_e38e642dd91da8b25f24f86a134afda6.bindPopup(popup_b9df20d11dfdb7135579303f1b398ea3)
        ;

        
    
    
            var marker_d34789405854e9a100ec56f9160d444f = L.marker(
                [55.737252, 37.60957],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_ba0c343bb5c6b79175f91bb55d356024 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d34789405854e9a100ec56f9160d444f.setIcon(icon_ba0c343bb5c6b79175f91bb55d356024);
        
    
        var popup_38c5b3cd20906f72becff7fdf4449290 = L.popup({"maxWidth": "100%"});

        
            
                var html_5803ce69f9daa0b2349c9b8298135d6c = $(`<div id="html_5803ce69f9daa0b2349c9b8298135d6c" style="width: 100.0%; height: 100.0%;">Москино Музеон</div>`)[0];
                popup_38c5b3cd20906f72becff7fdf4449290.setContent(html_5803ce69f9daa0b2349c9b8298135d6c);
            
        

        marker_d34789405854e9a100ec56f9160d444f.bindPopup(popup_38c5b3cd20906f72becff7fdf4449290)
        ;

        
    
    
            var marker_0b01aa7fc757e754ae0942d0b1ba1649 = L.marker(
                [55.7058041577479, 37.38887436511232],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_dbd29860f33f587eac7b628b8e2e5a65 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_0b01aa7fc757e754ae0942d0b1ba1649.setIcon(icon_dbd29860f33f587eac7b628b8e2e5a65);
        
    
        var popup_6c00716316bf9b76ddd6ed18b4ee609b = L.popup({"maxWidth": "100%"});

        
            
                var html_3db2f868bfcdd58bd731bcb87f8d7292 = $(`<div id="html_3db2f868bfcdd58bd731bcb87f8d7292" style="width: 100.0%; height: 100.0%;">Формула Кино на Можайке</div>`)[0];
                popup_6c00716316bf9b76ddd6ed18b4ee609b.setContent(html_3db2f868bfcdd58bd731bcb87f8d7292);
            
        

        marker_0b01aa7fc757e754ae0942d0b1ba1649.bindPopup(popup_6c00716316bf9b76ddd6ed18b4ee609b)
        ;

        
    
    
            var marker_3ef83b0c2342eaa5ea043a64cb241b70 = L.marker(
                [55.74795848025167, 37.64495862158651],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_61c543c82146ca805b43afcc3e82c310 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_3ef83b0c2342eaa5ea043a64cb241b70.setIcon(icon_61c543c82146ca805b43afcc3e82c310);
        
    
        var popup_f472d0a7040eba17bb1fe6fc4477aa1e = L.popup({"maxWidth": "100%"});

        
            
                var html_2d0aff052ab0494e0958743d72b61d5c = $(`<div id="html_2d0aff052ab0494e0958743d72b61d5c" style="width: 100.0%; height: 100.0%;">Иллюзион</div>`)[0];
                popup_f472d0a7040eba17bb1fe6fc4477aa1e.setContent(html_2d0aff052ab0494e0958743d72b61d5c);
            
        

        marker_3ef83b0c2342eaa5ea043a64cb241b70.bindPopup(popup_f472d0a7040eba17bb1fe6fc4477aa1e)
        ;

        
    
    
            var marker_0648cea2fda56ca5a91ff9a69f49ce9d = L.marker(
                [55.7451258529324, 37.5499906428528],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_bc203f6e715a7400a6af81820a514a36 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_0648cea2fda56ca5a91ff9a69f49ce9d.setIcon(icon_bc203f6e715a7400a6af81820a514a36);
        
    
        var popup_857efacbba915c95cf7b3caf4392db90 = L.popup({"maxWidth": "100%"});

        
            
                var html_b6c699f9064609ab9059412ce86b0e84 = $(`<div id="html_b6c699f9064609ab9059412ce86b0e84" style="width: 100.0%; height: 100.0%;">Пионер</div>`)[0];
                popup_857efacbba915c95cf7b3caf4392db90.setContent(html_b6c699f9064609ab9059412ce86b0e84);
            
        

        marker_0648cea2fda56ca5a91ff9a69f49ce9d.bindPopup(popup_857efacbba915c95cf7b3caf4392db90)
        ;

        
    
    
            var marker_c08ca04b879d5cd1c855c813dfed45fc = L.marker(
                [55.811776, 37.830817],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_66ebb438642ec6745d7e90d943cdbea9 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_c08ca04b879d5cd1c855c813dfed45fc.setIcon(icon_66ebb438642ec6745d7e90d943cdbea9);
        
    
        var popup_e40956bc2151a8164689f63b1567c1db = L.popup({"maxWidth": "100%"});

        
            
                var html_10a5bcf64f2c8a23f9d2165ce61af46b = $(`<div id="html_10a5bcf64f2c8a23f9d2165ce61af46b" style="width: 100.0%; height: 100.0%;">ЦентрФильм на Щелковской</div>`)[0];
                popup_e40956bc2151a8164689f63b1567c1db.setContent(html_10a5bcf64f2c8a23f9d2165ce61af46b);
            
        

        marker_c08ca04b879d5cd1c855c813dfed45fc.bindPopup(popup_e40956bc2151a8164689f63b1567c1db)
        ;

        
    
    
            var marker_5c80a232a7d427b01b39d13ca345b720 = L.marker(
                [55.852797, 37.585774],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_30b9816a4fe166f28be4e1c6f488b9b2 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_5c80a232a7d427b01b39d13ca345b720.setIcon(icon_30b9816a4fe166f28be4e1c6f488b9b2);
        
    
        var popup_5565a88edd6c6712ed570f2c34807aba = L.popup({"maxWidth": "100%"});

        
            
                var html_3bbb643c3ae18e93cca95443eb883972 = $(`<div id="html_3bbb643c3ae18e93cca95443eb883972" style="width: 100.0%; height: 100.0%;">Алмаз Синема Алтуфьевский</div>`)[0];
                popup_5565a88edd6c6712ed570f2c34807aba.setContent(html_3bbb643c3ae18e93cca95443eb883972);
            
        

        marker_5c80a232a7d427b01b39d13ca345b720.bindPopup(popup_5565a88edd6c6712ed570f2c34807aba)
        ;

        
    
    
            var marker_6cf87bad854d90f69983ac8b4de5ea08 = L.marker(
                [55.623788, 37.422027],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_b57da0835e680dedb28c930e01ab2fb4 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_6cf87bad854d90f69983ac8b4de5ea08.setIcon(icon_b57da0835e680dedb28c930e01ab2fb4);
        
    
        var popup_01a12e9f022539803376a8d83fd7ea18 = L.popup({"maxWidth": "100%"});

        
            
                var html_e44e4d81dd4e53040d4119b48d0bf3fe = $(`<div id="html_e44e4d81dd4e53040d4119b48d0bf3fe" style="width: 100.0%; height: 100.0%;">Каро 8 Саларис</div>`)[0];
                popup_01a12e9f022539803376a8d83fd7ea18.setContent(html_e44e4d81dd4e53040d4119b48d0bf3fe);
            
        

        marker_6cf87bad854d90f69983ac8b4de5ea08.bindPopup(popup_01a12e9f022539803376a8d83fd7ea18)
        ;

        
    
    
            var marker_d65553773da945d55d69ae791941dc71 = L.marker(
                [55.649884, 37.596263],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a963e516ad87ca6dd6846b79bbedb4bf = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d65553773da945d55d69ae791941dc71.setIcon(icon_a963e516ad87ca6dd6846b79bbedb4bf);
        
    
        var popup_51c6d6a95d1cfb565d4437e4dfff81da = L.popup({"maxWidth": "100%"});

        
            
                var html_112f238775d1e23740187df06931d083 = $(`<div id="html_112f238775d1e23740187df06931d083" style="width: 100.0%; height: 100.0%;">Алмаз Синема Азовский</div>`)[0];
                popup_51c6d6a95d1cfb565d4437e4dfff81da.setContent(html_112f238775d1e23740187df06931d083);
            
        

        marker_d65553773da945d55d69ae791941dc71.bindPopup(popup_51c6d6a95d1cfb565d4437e4dfff81da)
        ;

        
    
    
            var marker_d6985a9818c0a6972816f81688acc819 = L.marker(
                [55.686098, 37.85378],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_f087d1fd98dab7be9c01ce3863bb4e32 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d6985a9818c0a6972816f81688acc819.setIcon(icon_f087d1fd98dab7be9c01ce3863bb4e32);
        
    
        var popup_4ec06dd10e6d447271434bb510c89b2b = L.popup({"maxWidth": "100%"});

        
            
                var html_fd7cb7831305fe40f5f0c18949167754 = $(`<div id="html_fd7cb7831305fe40f5f0c18949167754" style="width: 100.0%; height: 100.0%;">Киномакс-Жулебино</div>`)[0];
                popup_4ec06dd10e6d447271434bb510c89b2b.setContent(html_fd7cb7831305fe40f5f0c18949167754);
            
        

        marker_d6985a9818c0a6972816f81688acc819.bindPopup(popup_4ec06dd10e6d447271434bb510c89b2b)
        ;

        
    
    
            var marker_68f7d94a11f2a522f5a2a9eddeea8d23 = L.marker(
                [55.730973, 37.504834],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_3d4f2b7ebfc17b577df5aeac71fac91a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_68f7d94a11f2a522f5a2a9eddeea8d23.setIcon(icon_3d4f2b7ebfc17b577df5aeac71fac91a);
        
    
        var popup_0d632c3d53bda154301508c56d8dc3e2 = L.popup({"maxWidth": "100%"});

        
            
                var html_1b786a6b6e6e5590b0fcc1bc0453257a = $(`<div id="html_1b786a6b6e6e5590b0fcc1bc0453257a" style="width: 100.0%; height: 100.0%;">Поклонка</div>`)[0];
                popup_0d632c3d53bda154301508c56d8dc3e2.setContent(html_1b786a6b6e6e5590b0fcc1bc0453257a);
            
        

        marker_68f7d94a11f2a522f5a2a9eddeea8d23.bindPopup(popup_0d632c3d53bda154301508c56d8dc3e2)
        ;

        
    
    
            var marker_07b43472649bcfedf01730803fe315eb = L.marker(
                [55.682813, 37.5713],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_5ba2aac55dbc0a1d46d14ccd1d650b4b = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_07b43472649bcfedf01730803fe315eb.setIcon(icon_5ba2aac55dbc0a1d46d14ccd1d650b4b);
        
    
        var popup_b5f0135f5929ca6bc649fd0456b94362 = L.popup({"maxWidth": "100%"});

        
            
                var html_a41ce03149734bb800fb0089a4c0d226 = $(`<div id="html_a41ce03149734bb800fb0089a4c0d226" style="width: 100.0%; height: 100.0%;">Москино Салют</div>`)[0];
                popup_b5f0135f5929ca6bc649fd0456b94362.setContent(html_a41ce03149734bb800fb0089a4c0d226);
            
        

        marker_07b43472649bcfedf01730803fe315eb.bindPopup(popup_b5f0135f5929ca6bc649fd0456b94362)
        ;

        
    
    
            var marker_4e99524c2eef3fbbc589d523238863d9 = L.marker(
                [55.659796, 37.749704],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_671bae09eb1287c20aeb7fdfcd044b00 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_4e99524c2eef3fbbc589d523238863d9.setIcon(icon_671bae09eb1287c20aeb7fdfcd044b00);
        
    
        var popup_d85bb032ec7dd93140e79653470b8ae6 = L.popup({"maxWidth": "100%"});

        
            
                var html_be1187e38cc10e8ea12485340e970ac4 = $(`<div id="html_be1187e38cc10e8ea12485340e970ac4" style="width: 100.0%; height: 100.0%;">Киномакс-Солярис</div>`)[0];
                popup_d85bb032ec7dd93140e79653470b8ae6.setContent(html_be1187e38cc10e8ea12485340e970ac4);
            
        

        marker_4e99524c2eef3fbbc589d523238863d9.bindPopup(popup_d85bb032ec7dd93140e79653470b8ae6)
        ;

        
    
    
            var marker_54ae2abec00ee2af6c21ef5b1bee9f0f = L.marker(
                [55.781607, 37.717951],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_0198135d815c1f94f01efe124383831c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_54ae2abec00ee2af6c21ef5b1bee9f0f.setIcon(icon_0198135d815c1f94f01efe124383831c);
        
    
        var popup_9b45f16b4e85fec8a6ef2d8dc9b32d7f = L.popup({"maxWidth": "100%"});

        
            
                var html_986c9b3313a5e0b3029f48d12ad9ac49 = $(`<div id="html_986c9b3313a5e0b3029f48d12ad9ac49" style="width: 100.0%; height: 100.0%;">Родина</div>`)[0];
                popup_9b45f16b4e85fec8a6ef2d8dc9b32d7f.setContent(html_986c9b3313a5e0b3029f48d12ad9ac49);
            
        

        marker_54ae2abec00ee2af6c21ef5b1bee9f0f.bindPopup(popup_9b45f16b4e85fec8a6ef2d8dc9b32d7f)
        ;

        
    
    
            var marker_ad40816a4613b0fb154105caa95e13c8 = L.marker(
                [55.846113, 37.358211],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_b61f6f162ca37fa851cc1528b4cda144 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_ad40816a4613b0fb154105caa95e13c8.setIcon(icon_b61f6f162ca37fa851cc1528b4cda144);
        
    
        var popup_dfba99a9730a4d16acb86237c9d260df = L.popup({"maxWidth": "100%"});

        
            
                var html_e7b864408b9001ae94210a747512652c = $(`<div id="html_e7b864408b9001ae94210a747512652c" style="width: 100.0%; height: 100.0%;">Pushka Mitino</div>`)[0];
                popup_dfba99a9730a4d16acb86237c9d260df.setContent(html_e7b864408b9001ae94210a747512652c);
            
        

        marker_ad40816a4613b0fb154105caa95e13c8.bindPopup(popup_dfba99a9730a4d16acb86237c9d260df)
        ;

        
    
    
            var marker_1914a9b6a731f97b6323e17449d55e2d = L.marker(
                [55.880975, 37.450368],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_8b56678699e69a0f7a5643b5fe5572bc = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_1914a9b6a731f97b6323e17449d55e2d.setIcon(icon_8b56678699e69a0f7a5643b5fe5572bc);
        
    
        var popup_3eaf47b915f5f31a7541019b633b9961 = L.popup({"maxWidth": "100%"});

        
            
                var html_5b59227faa2f5750ba752a94c8bc6a8f = $(`<div id="html_5b59227faa2f5750ba752a94c8bc6a8f" style="width: 100.0%; height: 100.0%;">Киносфера IMAX</div>`)[0];
                popup_3eaf47b915f5f31a7541019b633b9961.setContent(html_5b59227faa2f5750ba752a94c8bc6a8f);
            
        

        marker_1914a9b6a731f97b6323e17449d55e2d.bindPopup(popup_3eaf47b915f5f31a7541019b633b9961)
        ;

        
    
    
            var marker_b896057d9e71b2be1906d802356d2537 = L.marker(
                [55.64983600776148, 37.77007254337764],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_7756e0f6bf319a773877c351a89b0adc = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_b896057d9e71b2be1906d802356d2537.setIcon(icon_7756e0f6bf319a773877c351a89b0adc);
        
    
        var popup_f42674dd093de2c0fc150ecdd9ef1fd6 = L.popup({"maxWidth": "100%"});

        
            
                var html_078d950ac8114bd49002be31f006aac0 = $(`<div id="html_078d950ac8114bd49002be31f006aac0" style="width: 100.0%; height: 100.0%;">Мираж Синема Mari</div>`)[0];
                popup_f42674dd093de2c0fc150ecdd9ef1fd6.setContent(html_078d950ac8114bd49002be31f006aac0);
            
        

        marker_b896057d9e71b2be1906d802356d2537.bindPopup(popup_f42674dd093de2c0fc150ecdd9ef1fd6)
        ;

        
    
    
            var marker_c4cd076aa9f957e22c08ca1ce81c83ff = L.marker(
                [55.898644, 37.629193],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_96d1ba4102b50d9d3b22c186bf43b9e5 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_c4cd076aa9f957e22c08ca1ce81c83ff.setIcon(icon_96d1ba4102b50d9d3b22c186bf43b9e5);
        
    
        var popup_8553b2f571fb424f4ebe012f004455c5 = L.popup({"maxWidth": "100%"});

        
            
                var html_252dc8b5d1d8bfa29caf18f03e26daca = $(`<div id="html_252dc8b5d1d8bfa29caf18f03e26daca" style="width: 100.0%; height: 100.0%;">Час Кино (Бибирево)</div>`)[0];
                popup_8553b2f571fb424f4ebe012f004455c5.setContent(html_252dc8b5d1d8bfa29caf18f03e26daca);
            
        

        marker_c4cd076aa9f957e22c08ca1ce81c83ff.bindPopup(popup_8553b2f571fb424f4ebe012f004455c5)
        ;

        
    
    
            var marker_e1076fe9996007f2a6688c086ca3f5b9 = L.marker(
                [55.888542, 37.588474],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_e705cd4c0a94e7df8bc70e7a57e39332 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e1076fe9996007f2a6688c086ca3f5b9.setIcon(icon_e705cd4c0a94e7df8bc70e7a57e39332);
        
    
        var popup_d0ba34f4773ed9eb61f7e4f7c952ff3c = L.popup({"maxWidth": "100%"});

        
            
                var html_d8eb0b0f69df4650cb36a8bb06974597 = $(`<div id="html_d8eb0b0f69df4650cb36a8bb06974597" style="width: 100.0%; height: 100.0%;">Каро 3 Алтуфьево</div>`)[0];
                popup_d0ba34f4773ed9eb61f7e4f7c952ff3c.setContent(html_d8eb0b0f69df4650cb36a8bb06974597);
            
        

        marker_e1076fe9996007f2a6688c086ca3f5b9.bindPopup(popup_d0ba34f4773ed9eb61f7e4f7c952ff3c)
        ;

        
    
    
            var marker_7da318ef8af798493492d52b8cd8e97c = L.marker(
                [55.737569, 37.716596],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_084556c499740ce34ec98b26e0726b92 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_7da318ef8af798493492d52b8cd8e97c.setIcon(icon_084556c499740ce34ec98b26e0726b92);
        
    
        var popup_5d196215a4b7b0f255a77548e3221926 = L.popup({"maxWidth": "100%"});

        
            
                var html_78625f8f4583e9a7bf5bffa16ac4db6a = $(`<div id="html_78625f8f4583e9a7bf5bffa16ac4db6a" style="width: 100.0%; height: 100.0%;">Олимпик Синема</div>`)[0];
                popup_5d196215a4b7b0f255a77548e3221926.setContent(html_78625f8f4583e9a7bf5bffa16ac4db6a);
            
        

        marker_7da318ef8af798493492d52b8cd8e97c.bindPopup(popup_5d196215a4b7b0f255a77548e3221926)
        ;

        
    
    
            var marker_92761b738c8d1745ea100ffcabc4cb16 = L.marker(
                [55.607489, 37.532367],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_d9842115087660987ab58787449b40ac = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_92761b738c8d1745ea100ffcabc4cb16.setIcon(icon_d9842115087660987ab58787449b40ac);
        
    
        var popup_6cd16317a18c6de18b803eff12ff6f16 = L.popup({"maxWidth": "100%"});

        
            
                var html_09b9c80aac968a548f5353e39d64a702 = $(`<div id="html_09b9c80aac968a548f5353e39d64a702" style="width: 100.0%; height: 100.0%;">Киноквартал в Ясенево</div>`)[0];
                popup_6cd16317a18c6de18b803eff12ff6f16.setContent(html_09b9c80aac968a548f5353e39d64a702);
            
        

        marker_92761b738c8d1745ea100ffcabc4cb16.bindPopup(popup_6cd16317a18c6de18b803eff12ff6f16)
        ;

        
    
    
            var marker_1c4c8440884d8dbc198fbc2a13b3439a = L.marker(
                [55.75979075291515, 37.65707114341777],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_058d47e914de982423bf3ebb36f1f911 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_1c4c8440884d8dbc198fbc2a13b3439a.setIcon(icon_058d47e914de982423bf3ebb36f1f911);
        
    
        var popup_a93d7166cd271c50c2fcfa025d410906 = L.popup({"maxWidth": "100%"});

        
            
                var html_10780ef80febf635fb83b3341a7f2158 = $(`<div id="html_10780ef80febf635fb83b3341a7f2158" style="width: 100.0%; height: 100.0%;">Москино Звезда</div>`)[0];
                popup_a93d7166cd271c50c2fcfa025d410906.setContent(html_10780ef80febf635fb83b3341a7f2158);
            
        

        marker_1c4c8440884d8dbc198fbc2a13b3439a.bindPopup(popup_a93d7166cd271c50c2fcfa025d410906)
        ;

        
    
    
            var marker_d772ec53785deee5800f1952160530b9 = L.marker(
                [55.574790548031466, 37.58001208305359],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_5605fed4a9198c7e3299104f5524035b = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d772ec53785deee5800f1952160530b9.setIcon(icon_5605fed4a9198c7e3299104f5524035b);
        
    
        var popup_1b978df8382eb1303e22759e84d77258 = L.popup({"maxWidth": "100%"});

        
            
                var html_4e6cbd550503aaa724ae55e017cc10de = $(`<div id="html_4e6cbd550503aaa724ae55e017cc10de" style="width: 100.0%; height: 100.0%;">Бульвар</div>`)[0];
                popup_1b978df8382eb1303e22759e84d77258.setContent(html_4e6cbd550503aaa724ae55e017cc10de);
            
        

        marker_d772ec53785deee5800f1952160530b9.bindPopup(popup_1b978df8382eb1303e22759e84d77258)
        ;

        
    
    
            var marker_f8d92f44d15139fe14cb790f62b702e3 = L.marker(
                [55.697490726724055, 37.50029079574836],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_36668957ae890cc9c84039e51b80e9d0 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_f8d92f44d15139fe14cb790f62b702e3.setIcon(icon_36668957ae890cc9c84039e51b80e9d0);
        
    
        var popup_adcc555af629f5403fc89a6f695c4260 = L.popup({"maxWidth": "100%"});

        
            
                var html_8b5001416fa7cc4cc5fc41c9042a2035 = $(`<div id="html_8b5001416fa7cc4cc5fc41c9042a2035" style="width: 100.0%; height: 100.0%;">Лорд</div>`)[0];
                popup_adcc555af629f5403fc89a6f695c4260.setContent(html_8b5001416fa7cc4cc5fc41c9042a2035);
            
        

        marker_f8d92f44d15139fe14cb790f62b702e3.bindPopup(popup_adcc555af629f5403fc89a6f695c4260)
        ;

        
    
    
            var marker_1c885c8ed7518acb54fdef19dd437b4f = L.marker(
                [55.682829, 37.571329],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_392f4e8018eaa6d84cd88facdb51b22f = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_1c885c8ed7518acb54fdef19dd437b4f.setIcon(icon_392f4e8018eaa6d84cd88facdb51b22f);
        
    
        var popup_9f89ecaff06030960daa24d3a7c81ccb = L.popup({"maxWidth": "100%"});

        
            
                var html_e46912eab8a9b3155c6cd30aaf7fef37 = $(`<div id="html_e46912eab8a9b3155c6cd30aaf7fef37" style="width: 100.0%; height: 100.0%;">Москино Салют</div>`)[0];
                popup_9f89ecaff06030960daa24d3a7c81ccb.setContent(html_e46912eab8a9b3155c6cd30aaf7fef37);
            
        

        marker_1c885c8ed7518acb54fdef19dd437b4f.bindPopup(popup_9f89ecaff06030960daa24d3a7c81ccb)
        ;

        
    
    
            var marker_2a260cbb74980426cd13e48b59c6109e = L.marker(
                [55.585281, 37.722897],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_9d2605d119037d2092a9f07b1eb16aba = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_2a260cbb74980426cd13e48b59c6109e.setIcon(icon_9d2605d119037d2092a9f07b1eb16aba);
        
    
        var popup_5e3891e026086ac7f7cef883bc92eaae = L.popup({"maxWidth": "100%"});

        
            
                var html_69463ca5d8ec9c59fdc0661dd55c4848 = $(`<div id="html_69463ca5d8ec9c59fdc0661dd55c4848" style="width: 100.0%; height: 100.0%;">КАРО 9 Вегас Каширский</div>`)[0];
                popup_5e3891e026086ac7f7cef883bc92eaae.setContent(html_69463ca5d8ec9c59fdc0661dd55c4848);
            
        

        marker_2a260cbb74980426cd13e48b59c6109e.bindPopup(popup_5e3891e026086ac7f7cef883bc92eaae)
        ;

        
    
    
            var marker_953ff7774dc7f7275851cfb6e1e4d62b = L.marker(
                [55.84025099999999, 37.49128199999996],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_091c3878c4abc6560289270abbe6111f = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_953ff7774dc7f7275851cfb6e1e4d62b.setIcon(icon_091c3878c4abc6560289270abbe6111f);
        
    
        var popup_d93a8bb3e35511af48a49e8e0d66f3e3 = L.popup({"maxWidth": "100%"});

        
            
                var html_49d6cfc0e4b7954632a032320afed2c0 = $(`<div id="html_49d6cfc0e4b7954632a032320afed2c0" style="width: 100.0%; height: 100.0%;">Киномакс–Водный</div>`)[0];
                popup_d93a8bb3e35511af48a49e8e0d66f3e3.setContent(html_49d6cfc0e4b7954632a032320afed2c0);
            
        

        marker_953ff7774dc7f7275851cfb6e1e4d62b.bindPopup(popup_d93a8bb3e35511af48a49e8e0d66f3e3)
        ;

        
    
    
            var marker_cf91925f0c01e247b04cf25ff59f2d7a = L.marker(
                [55.629965, 37.423851],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_fafc43b6f01d0b7e106654a9aab8ac64 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_cf91925f0c01e247b04cf25ff59f2d7a.setIcon(icon_fafc43b6f01d0b7e106654a9aab8ac64);
        
    
        var popup_e0c1bcb2f957cf313ba6b2f6fe7791b0 = L.popup({"maxWidth": "100%"});

        
            
                var html_5dfa5312e89e8e011bd3a148eceb4a03 = $(`<div id="html_5dfa5312e89e8e011bd3a148eceb4a03" style="width: 100.0%; height: 100.0%;">Синема Стар Москва Румянцево</div>`)[0];
                popup_e0c1bcb2f957cf313ba6b2f6fe7791b0.setContent(html_5dfa5312e89e8e011bd3a148eceb4a03);
            
        

        marker_cf91925f0c01e247b04cf25ff59f2d7a.bindPopup(popup_e0c1bcb2f957cf313ba6b2f6fe7791b0)
        ;

        
    
    
            var marker_21913479f467b36f25a61304e80d8a3b = L.marker(
                [55.863858, 37.545752],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_4121a01433ec60c761381c30eea1cccb = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_21913479f467b36f25a61304e80d8a3b.setIcon(icon_4121a01433ec60c761381c30eea1cccb);
        
    
        var popup_ad960065a403c44761137c30d15ad078 = L.popup({"maxWidth": "100%"});

        
            
                var html_16872924b09420ab0499a7b29009da65 = $(`<div id="html_16872924b09420ab0499a7b29009da65" style="width: 100.0%; height: 100.0%;">Киномакс-XL</div>`)[0];
                popup_ad960065a403c44761137c30d15ad078.setContent(html_16872924b09420ab0499a7b29009da65);
            
        

        marker_21913479f467b36f25a61304e80d8a3b.bindPopup(popup_ad960065a403c44761137c30d15ad078)
        ;

        
    
    
            var marker_e5453dee49459be977806f1b4e2d1f4a = L.marker(
                [55.8618488, 37.6765311],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_9e1656b0f06182e4b76da53345f8b32d = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e5453dee49459be977806f1b4e2d1f4a.setIcon(icon_9e1656b0f06182e4b76da53345f8b32d);
        
    
        var popup_ce3bab49c95370d29ffa0011b4b2dae6 = L.popup({"maxWidth": "100%"});

        
            
                var html_f90f9a484917a40f3b69cc330513399c = $(`<div id="html_f90f9a484917a40f3b69cc330513399c" style="width: 100.0%; height: 100.0%;">Москино Вымпел</div>`)[0];
                popup_ce3bab49c95370d29ffa0011b4b2dae6.setContent(html_f90f9a484917a40f3b69cc330513399c);
            
        

        marker_e5453dee49459be977806f1b4e2d1f4a.bindPopup(popup_ce3bab49c95370d29ffa0011b4b2dae6)
        ;

        
    
    
            var marker_1d3ae2e92ca59514932e8d320d833ad4 = L.marker(
                [55.8460347915779, 37.4429064095288],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_5afcf44e75c002b60bb01bebc7c2ed84 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_1d3ae2e92ca59514932e8d320d833ad4.setIcon(icon_5afcf44e75c002b60bb01bebc7c2ed84);
        
    
        var popup_21ea7ed120dac7bf0d3365f3077890c8 = L.popup({"maxWidth": "100%"});

        
            
                var html_b264d79d2960646e241320493bf0b131 = $(`<div id="html_b264d79d2960646e241320493bf0b131" style="width: 100.0%; height: 100.0%;">Москино Полет</div>`)[0];
                popup_21ea7ed120dac7bf0d3365f3077890c8.setContent(html_b264d79d2960646e241320493bf0b131);
            
        

        marker_1d3ae2e92ca59514932e8d320d833ad4.bindPopup(popup_21ea7ed120dac7bf0d3365f3077890c8)
        ;

        
    
    
            var marker_69529deed8a5d743d4d322aa37595a9c = L.marker(
                [55.81446, 37.57113490000006],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_9742aa95086a51beab90a303b92ace09 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_69529deed8a5d743d4d322aa37595a9c.setIcon(icon_9742aa95086a51beab90a303b92ace09);
        
    
        var popup_4fc6cad462b477089c60fa27c6737bba = L.popup({"maxWidth": "100%"});

        
            
                var html_39c9b35b3d7cda88d0b97daf115b89ae = $(`<div id="html_39c9b35b3d7cda88d0b97daf115b89ae" style="width: 100.0%; height: 100.0%;">Москино Искра</div>`)[0];
                popup_4fc6cad462b477089c60fa27c6737bba.setContent(html_39c9b35b3d7cda88d0b97daf115b89ae);
            
        

        marker_69529deed8a5d743d4d322aa37595a9c.bindPopup(popup_4fc6cad462b477089c60fa27c6737bba)
        ;

        
    
    
            var marker_236dd46ab7562f2f89b458dc7ffdaec0 = L.marker(
                [55.818714, 37.63678099999993],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_cdbaabea170afd579a844bea0bb76405 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_236dd46ab7562f2f89b458dc7ffdaec0.setIcon(icon_cdbaabea170afd579a844bea0bb76405);
        
    
        var popup_71dc44a914cef6818296e3d462e6d5b2 = L.popup({"maxWidth": "100%"});

        
            
                var html_e3f9a34090308163e1ff17d808e0b241 = $(`<div id="html_e3f9a34090308163e1ff17d808e0b241" style="width: 100.0%; height: 100.0%;">Москино Космос</div>`)[0];
                popup_71dc44a914cef6818296e3d462e6d5b2.setContent(html_e3f9a34090308163e1ff17d808e0b241);
            
        

        marker_236dd46ab7562f2f89b458dc7ffdaec0.bindPopup(popup_71dc44a914cef6818296e3d462e6d5b2)
        ;

        
    
    
            var marker_eaba8abda8d8d3d3ce5c260c19b368e8 = L.marker(
                [55.881176, 37.450124],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_d773c49d9836a1d9529e12d63a0957ce = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_eaba8abda8d8d3d3ce5c260c19b368e8.setIcon(icon_d773c49d9836a1d9529e12d63a0957ce);
        
    
        var popup_e0b4f69bec0bb431adec5f370fd5e08f = L.popup({"maxWidth": "100%"});

        
            
                var html_5a5a803f4ac7f54cb656db0987f033ad = $(`<div id="html_5a5a803f4ac7f54cb656db0987f033ad" style="width: 100.0%; height: 100.0%;">Киносфера IMAX</div>`)[0];
                popup_e0b4f69bec0bb431adec5f370fd5e08f.setContent(html_5a5a803f4ac7f54cb656db0987f033ad);
            
        

        marker_eaba8abda8d8d3d3ce5c260c19b368e8.bindPopup(popup_e0b4f69bec0bb431adec5f370fd5e08f)
        ;

        
    
    
            var marker_3d8071fd13acf1d0f2d230f98f83fb6a = L.marker(
                [55.852025, 37.647645],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_98902341bb4c8f89a2c5316667a4646a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_3d8071fd13acf1d0f2d230f98f83fb6a.setIcon(icon_98902341bb4c8f89a2c5316667a4646a);
        
    
        var popup_aa9880f8e652ef1a6eabe7a05fa9acd6 = L.popup({"maxWidth": "100%"});

        
            
                var html_85338596042f7a11880a8366298a11d7 = $(`<div id="html_85338596042f7a11880a8366298a11d7" style="width: 100.0%; height: 100.0%;">Москино Сатурн</div>`)[0];
                popup_aa9880f8e652ef1a6eabe7a05fa9acd6.setContent(html_85338596042f7a11880a8366298a11d7);
            
        

        marker_3d8071fd13acf1d0f2d230f98f83fb6a.bindPopup(popup_aa9880f8e652ef1a6eabe7a05fa9acd6)
        ;

        
    
    
            var marker_793b5507c951096b64ad222aba303056 = L.marker(
                [55.8632268609835, 37.60212927187979],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_af8f2ab573aef5720b2d18b9189e392f = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_793b5507c951096b64ad222aba303056.setIcon(icon_af8f2ab573aef5720b2d18b9189e392f);
        
    
        var popup_19a26dfe5b67423833e1b048c0c002ec = L.popup({"maxWidth": "100%"});

        
            
                var html_8dbbcbdaf2c877ddf8851b5c7a13e863 = $(`<div id="html_8dbbcbdaf2c877ddf8851b5c7a13e863" style="width: 100.0%; height: 100.0%;">Мираж Синема Отрадное</div>`)[0];
                popup_19a26dfe5b67423833e1b048c0c002ec.setContent(html_8dbbcbdaf2c877ddf8851b5c7a13e863);
            
        

        marker_793b5507c951096b64ad222aba303056.bindPopup(popup_19a26dfe5b67423833e1b048c0c002ec)
        ;

        
    
    
            var marker_a3fe80624b2a8c09aa14f7ab14252a51 = L.marker(
                [55.761473, 37.58374],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_69437edee3a05fa5a6209dba3ce58340 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_a3fe80624b2a8c09aa14f7ab14252a51.setIcon(icon_69437edee3a05fa5a6209dba3ce58340);
        
    
        var popup_bcbf4bf785a9f483df6c53d7e0edd6d0 = L.popup({"maxWidth": "100%"});

        
            
                var html_918ae062ac282f2004b91922533c315e = $(`<div id="html_918ae062ac282f2004b91922533c315e" style="width: 100.0%; height: 100.0%;">Большой планетарий Москвы</div>`)[0];
                popup_bcbf4bf785a9f483df6c53d7e0edd6d0.setContent(html_918ae062ac282f2004b91922533c315e);
            
        

        marker_a3fe80624b2a8c09aa14f7ab14252a51.bindPopup(popup_bcbf4bf785a9f483df6c53d7e0edd6d0)
        ;

        
    
    
            var marker_294e61ece7d84833813cff02cbf674a6 = L.marker(
                [55.7643799930778, 37.705563411033495],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_00704bdbac1053bc62923d5a693b8778 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_294e61ece7d84833813cff02cbf674a6.setIcon(icon_00704bdbac1053bc62923d5a693b8778);
        
    
        var popup_13c40c6a4068701987892d16be8f26ed = L.popup({"maxWidth": "100%"});

        
            
                var html_d2eba4a55c0dafaeb3f7f11004d6eeb6 = $(`<div id="html_d2eba4a55c0dafaeb3f7f11004d6eeb6" style="width: 100.0%; height: 100.0%;">Москино Спутник</div>`)[0];
                popup_13c40c6a4068701987892d16be8f26ed.setContent(html_d2eba4a55c0dafaeb3f7f11004d6eeb6);
            
        

        marker_294e61ece7d84833813cff02cbf674a6.bindPopup(popup_13c40c6a4068701987892d16be8f26ed)
        ;

        
    
    
            var marker_ded42c7bb6fd07a0ebe9e4bdcdf98774 = L.marker(
                [55.727775, 37.601591],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_21cd4fcd9ad3d679e780aa38631a4ef9 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_ded42c7bb6fd07a0ebe9e4bdcdf98774.setIcon(icon_21cd4fcd9ad3d679e780aa38631a4ef9);
        
    
        var popup_d5d439e57364831e4f5376ace53a6c88 = L.popup({"maxWidth": "100%"});

        
            
                var html_a9a8fd40e85c7651fd89dd4a3c6c162d = $(`<div id="html_a9a8fd40e85c7651fd89dd4a3c6c162d" style="width: 100.0%; height: 100.0%;">Garage Screen</div>`)[0];
                popup_d5d439e57364831e4f5376ace53a6c88.setContent(html_a9a8fd40e85c7651fd89dd4a3c6c162d);
            
        

        marker_ded42c7bb6fd07a0ebe9e4bdcdf98774.bindPopup(popup_d5d439e57364831e4f5376ace53a6c88)
        ;

        
    
    
            var marker_6b89de5c258d084a63d64c47b7c890b2 = L.marker(
                [55.852027, 37.647636000000034],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_c2a2a51af3e0762bff35f8e137eabe06 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_6b89de5c258d084a63d64c47b7c890b2.setIcon(icon_c2a2a51af3e0762bff35f8e137eabe06);
        
    
        var popup_366c90342b7ebde6b72501306913fba0 = L.popup({"maxWidth": "100%"});

        
            
                var html_d2a195bf69cee6797fada739c386e315 = $(`<div id="html_d2a195bf69cee6797fada739c386e315" style="width: 100.0%; height: 100.0%;">Москино Сатурн</div>`)[0];
                popup_366c90342b7ebde6b72501306913fba0.setContent(html_d2a195bf69cee6797fada739c386e315);
            
        

        marker_6b89de5c258d084a63d64c47b7c890b2.bindPopup(popup_366c90342b7ebde6b72501306913fba0)
        ;

        
    
    
            var marker_0ef99941bdabfce9c43332e431280e23 = L.marker(
                [55.995632006046606, 37.53694104943543],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_79e81a8842231a72d8054cdce6287bb1 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_0ef99941bdabfce9c43332e431280e23.setIcon(icon_79e81a8842231a72d8054cdce6287bb1);
        
    
        var popup_79962f6aff6a1c099ee788daaebd83f8 = L.popup({"maxWidth": "100%"});

        
            
                var html_6399fbd646a0bad4a7fc16fd595f7b52 = $(`<div id="html_6399fbd646a0bad4a7fc16fd595f7b52" style="width: 100.0%; height: 100.0%;">Magic Cinema</div>`)[0];
                popup_79962f6aff6a1c099ee788daaebd83f8.setContent(html_6399fbd646a0bad4a7fc16fd595f7b52);
            
        

        marker_0ef99941bdabfce9c43332e431280e23.bindPopup(popup_79962f6aff6a1c099ee788daaebd83f8)
        ;

        
    
    
            var marker_5bea2f52336de625db0cd4d20bf8c5de = L.marker(
                [55.7282789, 37.58448680000004],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_09a4e0f8197b750d3c45245b5eb1df48 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_5bea2f52336de625db0cd4d20bf8c5de.setIcon(icon_09a4e0f8197b750d3c45245b5eb1df48);
        
    
        var popup_5a65d2353bce578b96af6ea60a5c8506 = L.popup({"maxWidth": "100%"});

        
            
                var html_44a53f65ad1491f8c07f94bf73f93181 = $(`<div id="html_44a53f65ad1491f8c07f94bf73f93181" style="width: 100.0%; height: 100.0%;">Формула Кино Горизонт</div>`)[0];
                popup_5a65d2353bce578b96af6ea60a5c8506.setContent(html_44a53f65ad1491f8c07f94bf73f93181);
            
        

        marker_5bea2f52336de625db0cd4d20bf8c5de.bindPopup(popup_5a65d2353bce578b96af6ea60a5c8506)
        ;

        
    
    
            var marker_b5d84c01f729c2da6cc7af32c06e7039 = L.marker(
                [55.707294, 37.456828],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_639437535b822d72d3c2a721a9bd775a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_b5d84c01f729c2da6cc7af32c06e7039.setIcon(icon_639437535b822d72d3c2a721a9bd775a);
        
    
        var popup_044178da96918075e69e3e3b47fedbb8 = L.popup({"maxWidth": "100%"});

        
            
                var html_90ba5dff56db3150698dca611f27ccb5 = $(`<div id="html_90ba5dff56db3150698dca611f27ccb5" style="width: 100.0%; height: 100.0%;">Синема Стар Kvartal</div>`)[0];
                popup_044178da96918075e69e3e3b47fedbb8.setContent(html_90ba5dff56db3150698dca611f27ccb5);
            
        

        marker_b5d84c01f729c2da6cc7af32c06e7039.bindPopup(popup_044178da96918075e69e3e3b47fedbb8)
        ;

        
    
    
            var marker_57c6de48d482005baece92ebc687b7c3 = L.marker(
                [55.766212, 37.380875],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_bba4a92c3db22eb2bfdf8530390b3452 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_57c6de48d482005baece92ebc687b7c3.setIcon(icon_bba4a92c3db22eb2bfdf8530390b3452);
        
    
        var popup_20e79018862d9c13f49802de19d625c9 = L.popup({"maxWidth": "100%"});

        
            
                var html_b9a72fa94b53f9e269b2f7dd7f53150f = $(`<div id="html_b9a72fa94b53f9e269b2f7dd7f53150f" style="width: 100.0%; height: 100.0%;">Синема Стар в МТК ЕвроПарк</div>`)[0];
                popup_20e79018862d9c13f49802de19d625c9.setContent(html_b9a72fa94b53f9e269b2f7dd7f53150f);
            
        

        marker_57c6de48d482005baece92ebc687b7c3.bindPopup(popup_20e79018862d9c13f49802de19d625c9)
        ;

        
    
    
            var marker_854c0da365084f3d7f9e453bfb0cfbaf = L.marker(
                [55.697463, 37.500207],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_c462c98f69c73c87b76c9545e4fb4dfb = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_854c0da365084f3d7f9e453bfb0cfbaf.setIcon(icon_c462c98f69c73c87b76c9545e4fb4dfb);
        
    
        var popup_b1ebc7cf53c54cf8bed3f5c9eaa96cca = L.popup({"maxWidth": "100%"});

        
            
                var html_038baedbf32c9b926445d86057816665 = $(`<div id="html_038baedbf32c9b926445d86057816665" style="width: 100.0%; height: 100.0%;">Лорд</div>`)[0];
                popup_b1ebc7cf53c54cf8bed3f5c9eaa96cca.setContent(html_038baedbf32c9b926445d86057816665);
            
        

        marker_854c0da365084f3d7f9e453bfb0cfbaf.bindPopup(popup_b1ebc7cf53c54cf8bed3f5c9eaa96cca)
        ;

        
    
    
            var marker_a8d87f8effa857af92f045f0e4c40244 = L.marker(
                [55.875804, 37.665542],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_9756c2a2c62ac4464903b49d4d62f893 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_a8d87f8effa857af92f045f0e4c40244.setIcon(icon_9756c2a2c62ac4464903b49d4d62f893);
        
    
        var popup_1656c884980e2fe2bb77532430e165df = L.popup({"maxWidth": "100%"});

        
            
                var html_52175bec6dcc5a0237049d16fa23bf1a = $(`<div id="html_52175bec6dcc5a0237049d16fa23bf1a" style="width: 100.0%; height: 100.0%;">Pushka</div>`)[0];
                popup_1656c884980e2fe2bb77532430e165df.setContent(html_52175bec6dcc5a0237049d16fa23bf1a);
            
        

        marker_a8d87f8effa857af92f045f0e4c40244.bindPopup(popup_1656c884980e2fe2bb77532430e165df)
        ;

        
    
    
            var marker_b3329221cee105f85d7560e77fcc12e6 = L.marker(
                [55.6858620512187, 37.718590289384],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_68c78c65678b2cbf990852166396d51b = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_b3329221cee105f85d7560e77fcc12e6.setIcon(icon_68c78c65678b2cbf990852166396d51b);
        
    
        var popup_0e7253e6cee22118c7e9243f5dd6e938 = L.popup({"maxWidth": "100%"});

        
            
                var html_d4f6c202a8ebe5038815ef307723830f = $(`<div id="html_d4f6c202a8ebe5038815ef307723830f" style="width: 100.0%; height: 100.0%;">Москино Тула</div>`)[0];
                popup_0e7253e6cee22118c7e9243f5dd6e938.setContent(html_d4f6c202a8ebe5038815ef307723830f);
            
        

        marker_b3329221cee105f85d7560e77fcc12e6.bindPopup(popup_0e7253e6cee22118c7e9243f5dd6e938)
        ;

        
    
    
            var marker_cbbfadeebfc34dd0f1b5d758aaf3bb4c = L.marker(
                [55.75394300000039, 37.60158699999624],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_bc01a854e55628834b31d95778c25329 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_cbbfadeebfc34dd0f1b5d758aaf3bb4c.setIcon(icon_bc01a854e55628834b31d95778c25329);
        
    
        var popup_26b4f443a8607b8256b254e7685e2ecf = L.popup({"maxWidth": "100%"});

        
            
                var html_5d737cb046a761190713f7f46bcea8f0 = $(`<div id="html_5d737cb046a761190713f7f46bcea8f0" style="width: 100.0%; height: 100.0%;">Киноцентр «Домжур»</div>`)[0];
                popup_26b4f443a8607b8256b254e7685e2ecf.setContent(html_5d737cb046a761190713f7f46bcea8f0);
            
        

        marker_cbbfadeebfc34dd0f1b5d758aaf3bb4c.bindPopup(popup_26b4f443a8607b8256b254e7685e2ecf)
        ;

        
    
    
            var marker_f7ebcd7600dabaf5a2c793bc3eeb696e = L.marker(
                [55.737226, 37.609844],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_4b4ea552abff308643a91655d7598b97 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_f7ebcd7600dabaf5a2c793bc3eeb696e.setIcon(icon_4b4ea552abff308643a91655d7598b97);
        
    
        var popup_674a5722277e3592bf328bbe3a7c33b4 = L.popup({"maxWidth": "100%"});

        
            
                var html_6adad802d199ca74a1b40cf9261e78ce = $(`<div id="html_6adad802d199ca74a1b40cf9261e78ce" style="width: 100.0%; height: 100.0%;">Москино Музеон</div>`)[0];
                popup_674a5722277e3592bf328bbe3a7c33b4.setContent(html_6adad802d199ca74a1b40cf9261e78ce);
            
        

        marker_f7ebcd7600dabaf5a2c793bc3eeb696e.bindPopup(popup_674a5722277e3592bf328bbe3a7c33b4)
        ;

        
    
    
            var marker_dc4c7bf172446826956380697665dbe5 = L.marker(
                [55.749841, 37.802562],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_fb3b23cf9df5e7628fe3f3a9958dfd02 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_dc4c7bf172446826956380697665dbe5.setIcon(icon_fb3b23cf9df5e7628fe3f3a9958dfd02);
        
    
        var popup_c6d8c1f223880315cab25d75c343cdd1 = L.popup({"maxWidth": "100%"});

        
            
                var html_6e076c9e9754320705faeb3911390eb7 = $(`<div id="html_6e076c9e9754320705faeb3911390eb7" style="width: 100.0%; height: 100.0%;">Москино Березка</div>`)[0];
                popup_c6d8c1f223880315cab25d75c343cdd1.setContent(html_6e076c9e9754320705faeb3911390eb7);
            
        

        marker_dc4c7bf172446826956380697665dbe5.bindPopup(popup_c6d8c1f223880315cab25d75c343cdd1)
        ;

        
    
    
            var marker_8452c679d41ae30b3f38a27e82229054 = L.marker(
                [55.727775, 37.601591],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_2d9ee3ef0c0dfa54c46a8605eebf109c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_8452c679d41ae30b3f38a27e82229054.setIcon(icon_2d9ee3ef0c0dfa54c46a8605eebf109c);
        
    
        var popup_0de52b59eda8654f0d9ead7ee097b8a1 = L.popup({"maxWidth": "100%"});

        
            
                var html_2431ccfb4a88db86b5642a7c11e2e14a = $(`<div id="html_2431ccfb4a88db86b5642a7c11e2e14a" style="width: 100.0%; height: 100.0%;">Лекторий Музея Гараж</div>`)[0];
                popup_0de52b59eda8654f0d9ead7ee097b8a1.setContent(html_2431ccfb4a88db86b5642a7c11e2e14a);
            
        

        marker_8452c679d41ae30b3f38a27e82229054.bindPopup(popup_0de52b59eda8654f0d9ead7ee097b8a1)
        ;

        
    
    
            var marker_96bd976e9c3fb852c3040c1e3f69684f = L.marker(
                [55.908452, 36.86108009999998],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_89c3adfc8f11b03d4d9457d9471ed702 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_96bd976e9c3fb852c3040c1e3f69684f.setIcon(icon_89c3adfc8f11b03d4d9457d9471ed702);
        
    
        var popup_66e365104125c8cbadf3c34c7f884090 = L.popup({"maxWidth": "100%"});

        
            
                var html_cfe7f2b140d172dbd08fece9a07de2bd = $(`<div id="html_cfe7f2b140d172dbd08fece9a07de2bd" style="width: 100.0%; height: 100.0%;">Молодежный центр (Истра)</div>`)[0];
                popup_66e365104125c8cbadf3c34c7f884090.setContent(html_cfe7f2b140d172dbd08fece9a07de2bd);
            
        

        marker_96bd976e9c3fb852c3040c1e3f69684f.bindPopup(popup_66e365104125c8cbadf3c34c7f884090)
        ;

        
    
    
            var marker_5a915d1bf01ad3c5bbc8a6ac03c10b68 = L.marker(
                [55.770796, 37.609272],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a5342a8d54f8b126f6812e31e79de61e = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_5a915d1bf01ad3c5bbc8a6ac03c10b68.setIcon(icon_a5342a8d54f8b126f6812e31e79de61e);
        
    
        var popup_8881a77cfb6e2588e6058830daa2c017 = L.popup({"maxWidth": "100%"});

        
            
                var html_a7227531bd5332cab72f2d095da2ac88 = $(`<div id="html_a7227531bd5332cab72f2d095da2ac88" style="width: 100.0%; height: 100.0%;">Летний КАРО Эрмитаж</div>`)[0];
                popup_8881a77cfb6e2588e6058830daa2c017.setContent(html_a7227531bd5332cab72f2d095da2ac88);
            
        

        marker_5a915d1bf01ad3c5bbc8a6ac03c10b68.bindPopup(popup_8881a77cfb6e2588e6058830daa2c017)
        ;

        
    
    
            var marker_3b670be24a40da451812fed97e81440e = L.marker(
                [55.87579740383949, 37.66548408661652],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_94255df9debf94e4bff275bc27744543 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_3b670be24a40da451812fed97e81440e.setIcon(icon_94255df9debf94e4bff275bc27744543);
        
    
        var popup_0145b71be5d575863cb51a7aa44d9699 = L.popup({"maxWidth": "100%"});

        
            
                var html_30dc4c19bfe0490827ca4c3873dffeb6 = $(`<div id="html_30dc4c19bfe0490827ca4c3873dffeb6" style="width: 100.0%; height: 100.0%;">Pushka Бабушкинская</div>`)[0];
                popup_0145b71be5d575863cb51a7aa44d9699.setContent(html_30dc4c19bfe0490827ca4c3873dffeb6);
            
        

        marker_3b670be24a40da451812fed97e81440e.bindPopup(popup_0145b71be5d575863cb51a7aa44d9699)
        ;

        
    
    
            var marker_d662c246b290651fca06a5509a46730b = L.marker(
                [56.01164545080232, 37.84754594104447],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_757e713757f25e1f149d0a55027ffb13 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d662c246b290651fca06a5509a46730b.setIcon(icon_757e713757f25e1f149d0a55027ffb13);
        
    
        var popup_1cb5c4eeeeaa7d4d856f48fe6d47e3c1 = L.popup({"maxWidth": "100%"});

        
            
                var html_f430cddc33847a5b14a6ae67a9c72e1c = $(`<div id="html_f430cddc33847a5b14a6ae67a9c72e1c" style="width: 100.0%; height: 100.0%;">Облака (Пушкино)</div>`)[0];
                popup_1cb5c4eeeeaa7d4d856f48fe6d47e3c1.setContent(html_f430cddc33847a5b14a6ae67a9c72e1c);
            
        

        marker_d662c246b290651fca06a5509a46730b.bindPopup(popup_1cb5c4eeeeaa7d4d856f48fe6d47e3c1)
        ;

        
    
    
            var marker_75c46d96caf0c64cafb6532eada146ba = L.marker(
                [55.7663236608865, 37.38083208465582],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_776a830ef54e24d01c398a00e993224e = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_75c46d96caf0c64cafb6532eada146ba.setIcon(icon_776a830ef54e24d01c398a00e993224e);
        
    
        var popup_c7e809284fcdf43f26573bbf9a89a30c = L.popup({"maxWidth": "100%"});

        
            
                var html_558d40303aa262589665090558cd533b = $(`<div id="html_558d40303aa262589665090558cd533b" style="width: 100.0%; height: 100.0%;">Синема Стар Европарк</div>`)[0];
                popup_c7e809284fcdf43f26573bbf9a89a30c.setContent(html_558d40303aa262589665090558cd533b);
            
        

        marker_75c46d96caf0c64cafb6532eada146ba.bindPopup(popup_c7e809284fcdf43f26573bbf9a89a30c)
        ;

        
    
    
            var marker_b16a06a80bcfdef3a93b409a554ae808 = L.marker(
                [55.7953679084301, 37.4954219162737],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_5a0ca336b844575168a4732891619b0a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_b16a06a80bcfdef3a93b409a554ae808.setIcon(icon_5a0ca336b844575168a4732891619b0a);
        
    
        var popup_d2708d16e6bd9f378b6037920e1b3fdf = L.popup({"maxWidth": "100%"});

        
            
                var html_598e66dadbbda46e5cb5b8c72f32f7f7 = $(`<div id="html_598e66dadbbda46e5cb5b8c72f32f7f7" style="width: 100.0%; height: 100.0%;">Москино Юность</div>`)[0];
                popup_d2708d16e6bd9f378b6037920e1b3fdf.setContent(html_598e66dadbbda46e5cb5b8c72f32f7f7);
            
        

        marker_b16a06a80bcfdef3a93b409a554ae808.bindPopup(popup_d2708d16e6bd9f378b6037920e1b3fdf)
        ;

        
    
    
            var marker_635ac882a9ceaac66726ad9f9c804af3 = L.marker(
                [55.749862, 37.802572000000055],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_7997187c79860d3773ad5a2cae9b4ec0 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_635ac882a9ceaac66726ad9f9c804af3.setIcon(icon_7997187c79860d3773ad5a2cae9b4ec0);
        
    
        var popup_35fe1fa26c20754c1a317f6149cbb3e9 = L.popup({"maxWidth": "100%"});

        
            
                var html_e6048ec3d7e661036b35c22f557c27ba = $(`<div id="html_e6048ec3d7e661036b35c22f557c27ba" style="width: 100.0%; height: 100.0%;">Москино Березка</div>`)[0];
                popup_35fe1fa26c20754c1a317f6149cbb3e9.setContent(html_e6048ec3d7e661036b35c22f557c27ba);
            
        

        marker_635ac882a9ceaac66726ad9f9c804af3.bindPopup(popup_35fe1fa26c20754c1a317f6149cbb3e9)
        ;

        
    
    
            var marker_466420373cdc395f10e5aeef4002b3df = L.marker(
                [55.70634, 37.596246],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_16bf2bc95bd44b9fa3447db4c998d62f = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_466420373cdc395f10e5aeef4002b3df.setIcon(icon_16bf2bc95bd44b9fa3447db4c998d62f);
        
    
        var popup_2fdd5b8e834c26910de40bd91f282822 = L.popup({"maxWidth": "100%"});

        
            
                var html_d9cb22d4ef5d07a2816355f18ffb8c18 = $(`<div id="html_d9cb22d4ef5d07a2816355f18ffb8c18" style="width: 100.0%; height: 100.0%;">Автокино «Ленинский»</div>`)[0];
                popup_2fdd5b8e834c26910de40bd91f282822.setContent(html_d9cb22d4ef5d07a2816355f18ffb8c18);
            
        

        marker_466420373cdc395f10e5aeef4002b3df.bindPopup(popup_2fdd5b8e834c26910de40bd91f282822)
        ;

        
    
    
            var marker_874181c5de234dae7f9175a1fa1637e3 = L.marker(
                [55.663314, 37.65602],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_00e97866e23f0a1f4cc459a7cbff462f = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_874181c5de234dae7f9175a1fa1637e3.setIcon(icon_00e97866e23f0a1f4cc459a7cbff462f);
        
    
        var popup_1d46a66e00720d9953f2f8d149ec5016 = L.popup({"maxWidth": "100%"});

        
            
                var html_e82a9e7983df22df7bbb1f5cd30643a1 = $(`<div id="html_e82a9e7983df22df7bbb1f5cd30643a1" style="width: 100.0%; height: 100.0%;">Летний КАРО парк Садовники</div>`)[0];
                popup_1d46a66e00720d9953f2f8d149ec5016.setContent(html_e82a9e7983df22df7bbb1f5cd30643a1);
            
        

        marker_874181c5de234dae7f9175a1fa1637e3.bindPopup(popup_1d46a66e00720d9953f2f8d149ec5016)
        ;

        
    
    
            var marker_d83ce429510ccae91eedd84aa5270c33 = L.marker(
                [55.998678, 37.25807689999999],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_6c20670eb1ce6e849240b2c7e0108568 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_d83ce429510ccae91eedd84aa5270c33.setIcon(icon_6c20670eb1ce6e849240b2c7e0108568);
        
    
        var popup_ab1d782d2fc0bb6593f6b3760a8548d0 = L.popup({"maxWidth": "100%"});

        
            
                var html_bba3f8db14bfe24bc2cb164a8263b940 = $(`<div id="html_bba3f8db14bfe24bc2cb164a8263b940" style="width: 100.0%; height: 100.0%;">Автокинотеатр Синема Парк Зеленопарк (Зеленоград)</div>`)[0];
                popup_ab1d782d2fc0bb6593f6b3760a8548d0.setContent(html_bba3f8db14bfe24bc2cb164a8263b940);
            
        

        marker_d83ce429510ccae91eedd84aa5270c33.bindPopup(popup_ab1d782d2fc0bb6593f6b3760a8548d0)
        ;

        
    
    
            var marker_4c38df97afd739c5f5719e1bc711579c = L.marker(
                [55.751843, 37.71612200000004],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_855f40871666c9267904af967b4ef4b7 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_4c38df97afd739c5f5719e1bc711579c.setIcon(icon_855f40871666c9267904af967b4ef4b7);
        
    
        var popup_51f2139e56aff988364da7a6672fd051 = L.popup({"maxWidth": "100%"});

        
            
                var html_b49c211c5c65ba892de2f5b33e8dd949 = $(`<div id="html_b49c211c5c65ba892de2f5b33e8dd949" style="width: 100.0%; height: 100.0%;">Москино Факел</div>`)[0];
                popup_51f2139e56aff988364da7a6672fd051.setContent(html_b49c211c5c65ba892de2f5b33e8dd949);
            
        

        marker_4c38df97afd739c5f5719e1bc711579c.bindPopup(popup_51f2139e56aff988364da7a6672fd051)
        ;

        
    
    
            var marker_313b95ab13ae023f11132498403e23bc = L.marker(
                [55.73648, 37.593102],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_2995e67c3f3184663c88a70b886e2be8 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_313b95ab13ae023f11132498403e23bc.setIcon(icon_2995e67c3f3184663c88a70b886e2be8);
        
    
        var popup_be5a71c5506123513b52b12cf1072eb8 = L.popup({"maxWidth": "100%"});

        
            
                var html_cdb89add6ae1fe6e67654e34503b7533 = $(`<div id="html_cdb89add6ae1fe6e67654e34503b7533" style="width: 100.0%; height: 100.0%;">Центр документального кино</div>`)[0];
                popup_be5a71c5506123513b52b12cf1072eb8.setContent(html_cdb89add6ae1fe6e67654e34503b7533);
            
        

        marker_313b95ab13ae023f11132498403e23bc.bindPopup(popup_be5a71c5506123513b52b12cf1072eb8)
        ;

        
    
    
            var marker_87fb46906e8a8224c970c8d357cb8d55 = L.marker(
                [55.72728573240573, 37.60247525877492],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_51ff7681ecf97c536c45fcc26461cd96 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_87fb46906e8a8224c970c8d357cb8d55.setIcon(icon_51ff7681ecf97c536c45fcc26461cd96);
        
    
        var popup_49244835ed78072d2dadfc51951596f9 = L.popup({"maxWidth": "100%"});

        
            
                var html_128b94e0093a3b2804f156a5f3c8c4a4 = $(`<div id="html_128b94e0093a3b2804f156a5f3c8c4a4" style="width: 100.0%; height: 100.0%;">Garage Screen</div>`)[0];
                popup_49244835ed78072d2dadfc51951596f9.setContent(html_128b94e0093a3b2804f156a5f3c8c4a4);
            
        

        marker_87fb46906e8a8224c970c8d357cb8d55.bindPopup(popup_49244835ed78072d2dadfc51951596f9)
        ;

        
    
    
            var marker_2c5d4a3705d5f0cdbedeca4dc4f9c7a8 = L.marker(
                [55.68347, 37.550266],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a7f050ee3f36c30aafab7ae0bd98874c = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_2c5d4a3705d5f0cdbedeca4dc4f9c7a8.setIcon(icon_a7f050ee3f36c30aafab7ae0bd98874c);
        
    
        var popup_6a6123275c1e0896909aa99921fec98e = L.popup({"maxWidth": "100%"});

        
            
                var html_f6c2dd45cf82fbffdd3956c058884ca2 = $(`<div id="html_f6c2dd45cf82fbffdd3956c058884ca2" style="width: 100.0%; height: 100.0%;">АвтоКАРО под звездами: Черёмушки</div>`)[0];
                popup_6a6123275c1e0896909aa99921fec98e.setContent(html_f6c2dd45cf82fbffdd3956c058884ca2);
            
        

        marker_2c5d4a3705d5f0cdbedeca4dc4f9c7a8.bindPopup(popup_6a6123275c1e0896909aa99921fec98e)
        ;

        
    
    
            var marker_49557ee252c5d0b520ea90f3f53e54d9 = L.marker(
                [55.9199092952377, 37.7084542380982],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_dc7b9c6da448f4647f89a994ba5d0243 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_49557ee252c5d0b520ea90f3f53e54d9.setIcon(icon_dc7b9c6da448f4647f89a994ba5d0243);
        
    
        var popup_04c8f694b0b2f1e7d8f8aefcc5f6772c = L.popup({"maxWidth": "100%"});

        
            
                var html_4d07d8bc5d8658bf2a5a62a34207f958 = $(`<div id="html_4d07d8bc5d8658bf2a5a62a34207f958" style="width: 100.0%; height: 100.0%;">Мори Синема Мытищи</div>`)[0];
                popup_04c8f694b0b2f1e7d8f8aefcc5f6772c.setContent(html_4d07d8bc5d8658bf2a5a62a34207f958);
            
        

        marker_49557ee252c5d0b520ea90f3f53e54d9.bindPopup(popup_04c8f694b0b2f1e7d8f8aefcc5f6772c)
        ;

        
    
    
            var marker_de6defbba8ab215b41bcba11569f09a0 = L.marker(
                [55.73860551177134, 37.41065654237116],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_cf447e466e25796c0994b94c570501d4 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_de6defbba8ab215b41bcba11569f09a0.setIcon(icon_cf447e466e25796c0994b94c570501d4);
        
    
        var popup_2a444f9dc4e545a04aeb2bdb1a0e24ff = L.popup({"maxWidth": "100%"});

        
            
                var html_79fd3668affb97c738be0e92156478f9 = $(`<div id="html_79fd3668affb97c738be0e92156478f9" style="width: 100.0%; height: 100.0%;">Мори Синема Кунцево</div>`)[0];
                popup_2a444f9dc4e545a04aeb2bdb1a0e24ff.setContent(html_79fd3668affb97c738be0e92156478f9);
            
        

        marker_de6defbba8ab215b41bcba11569f09a0.bindPopup(popup_2a444f9dc4e545a04aeb2bdb1a0e24ff)
        ;

        
    
    
            var marker_ed63d9572ee8b3c9f0a5a3f3a7cb7e00 = L.marker(
                [55.66367143248922, 37.51138249206542],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_080f522c3810634f9d9347beb3df7f6e = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_ed63d9572ee8b3c9f0a5a3f3a7cb7e00.setIcon(icon_080f522c3810634f9d9347beb3df7f6e);
        
    
        var popup_3bb45af442c5cd2a412017082625bc81 = L.popup({"maxWidth": "100%"});

        
            
                var html_909c45d081ea834ec3e49ffb8b1cf108 = $(`<div id="html_909c45d081ea834ec3e49ffb8b1cf108" style="width: 100.0%; height: 100.0%;">Синема Стар на Ленинском</div>`)[0];
                popup_3bb45af442c5cd2a412017082625bc81.setContent(html_909c45d081ea834ec3e49ffb8b1cf108);
            
        

        marker_ed63d9572ee8b3c9f0a5a3f3a7cb7e00.bindPopup(popup_3bb45af442c5cd2a412017082625bc81)
        ;

        
    
    
            var marker_9fcc0ee86d8365aa648b97af15ead4eb = L.marker(
                [55.70876155381475, 37.62206527116393],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_285cfe6cdb2bc70005919eca3c535bc1 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_9fcc0ee86d8365aa648b97af15ead4eb.setIcon(icon_285cfe6cdb2bc70005919eca3c535bc1);
        
    
        var popup_51524b209cd0ae9a12419bb5ca243a29 = L.popup({"maxWidth": "100%"});

        
            
                var html_1fd384e713e136a991437b550bf2fbaa = $(`<div id="html_1fd384e713e136a991437b550bf2fbaa" style="width: 100.0%; height: 100.0%;">Синема Стар Ереван Плаза</div>`)[0];
                popup_51524b209cd0ae9a12419bb5ca243a29.setContent(html_1fd384e713e136a991437b550bf2fbaa);
            
        

        marker_9fcc0ee86d8365aa648b97af15ead4eb.bindPopup(popup_51524b209cd0ae9a12419bb5ca243a29)
        ;

        
    
    
            var marker_553fbf63c4cadca71e6eabfcb84d744f = L.marker(
                [55.81100700000019, 37.80090099999688],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_0920603875ff7154427069e2fe326bf7 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_553fbf63c4cadca71e6eabfcb84d744f.setIcon(icon_0920603875ff7154427069e2fe326bf7);
        
    
        var popup_a705f6e0eb46216a2af2181b1792462d = L.popup({"maxWidth": "100%"});

        
            
                var html_a112ed04d2d75b5da61415fd9bed7769 = $(`<div id="html_a112ed04d2d75b5da61415fd9bed7769" style="width: 100.0%; height: 100.0%;">Кино Окко Щелковский</div>`)[0];
                popup_a705f6e0eb46216a2af2181b1792462d.setContent(html_a112ed04d2d75b5da61415fd9bed7769);
            
        

        marker_553fbf63c4cadca71e6eabfcb84d744f.bindPopup(popup_a705f6e0eb46216a2af2181b1792462d)
        ;

        
    
    
            var marker_8cf05c4c6bfbe57216b84f57cc36ded0 = L.marker(
                [55.84627392055067, 37.358160144562135],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a1ffef9a29d7230db2b2f55d8e9ef6bb = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_8cf05c4c6bfbe57216b84f57cc36ded0.setIcon(icon_a1ffef9a29d7230db2b2f55d8e9ef6bb);
        
    
        var popup_d4eb7f38ec9c408cb38260eb1e214489 = L.popup({"maxWidth": "100%"});

        
            
                var html_7a8992f3f03443af4a260fd2ddc0b77b = $(`<div id="html_7a8992f3f03443af4a260fd2ddc0b77b" style="width: 100.0%; height: 100.0%;">Pushka Митино</div>`)[0];
                popup_d4eb7f38ec9c408cb38260eb1e214489.setContent(html_7a8992f3f03443af4a260fd2ddc0b77b);
            
        

        marker_8cf05c4c6bfbe57216b84f57cc36ded0.bindPopup(popup_d4eb7f38ec9c408cb38260eb1e214489)
        ;

        
    
    
            var marker_fbaca2c9ffa446f1b49fb59eb813d9c8 = L.marker(
                [55.6634943872094, 37.48149100859837],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_969ca31a6cb3b7f11556f616979450b1 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_fbaca2c9ffa446f1b49fb59eb813d9c8.setIcon(icon_969ca31a6cb3b7f11556f616979450b1);
        
    
        var popup_1ee195454789ab4db0c91327251f0d59 = L.popup({"maxWidth": "100%"});

        
            
                var html_bfb2bb9d06719f181184f212b0fb313a = $(`<div id="html_bfb2bb9d06719f181184f212b0fb313a" style="width: 100.0%; height: 100.0%;">Синема Стар Юго-Западная</div>`)[0];
                popup_1ee195454789ab4db0c91327251f0d59.setContent(html_bfb2bb9d06719f181184f212b0fb313a);
            
        

        marker_fbaca2c9ffa446f1b49fb59eb813d9c8.bindPopup(popup_1ee195454789ab4db0c91327251f0d59)
        ;

        
    
    
            var marker_2c113a55a2667117d4c2cf7bfbd00012 = L.marker(
                [55.73181031026812, 37.487754821777344],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_aaae6b047412413f286be6336e19cecd = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_2c113a55a2667117d4c2cf7bfbd00012.setIcon(icon_aaae6b047412413f286be6336e19cecd);
        
    
        var popup_783e2f842e4307ccc6a99738c6f5bd10 = L.popup({"maxWidth": "100%"});

        
            
                var html_64904bd72447312ffed5e2a3a50bb020 = $(`<div id="html_64904bd72447312ffed5e2a3a50bb020" style="width: 100.0%; height: 100.0%;">Времена года</div>`)[0];
                popup_783e2f842e4307ccc6a99738c6f5bd10.setContent(html_64904bd72447312ffed5e2a3a50bb020);
            
        

        marker_2c113a55a2667117d4c2cf7bfbd00012.bindPopup(popup_783e2f842e4307ccc6a99738c6f5bd10)
        ;

        
    
    
            var marker_189fdc3133bc97a1d03672ec10a71679 = L.marker(
                [55.731713, 37.487353],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_f3bd1ffdac1aa30f6490af81677b82ca = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_189fdc3133bc97a1d03672ec10a71679.setIcon(icon_f3bd1ffdac1aa30f6490af81677b82ca);
        
    
        var popup_c7b1acf6290d23a21b3d3c1535840e42 = L.popup({"maxWidth": "100%"});

        
            
                var html_b7800e3f620e408136e465927834bbe0 = $(`<div id="html_b7800e3f620e408136e465927834bbe0" style="width: 100.0%; height: 100.0%;">Времена года</div>`)[0];
                popup_c7b1acf6290d23a21b3d3c1535840e42.setContent(html_b7800e3f620e408136e465927834bbe0);
            
        

        marker_189fdc3133bc97a1d03672ec10a71679.bindPopup(popup_c7b1acf6290d23a21b3d3c1535840e42)
        ;

        
    
    
            var marker_a03c74a994ff84c20bedf47499cfc300 = L.marker(
                [55.8529850301203, 37.5856299698636],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_3a5564d488bead3c405a38911909de16 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_a03c74a994ff84c20bedf47499cfc300.setIcon(icon_3a5564d488bead3c405a38911909de16);
        
    
        var popup_54d3967dc8097ffd96c7e5be080e4246 = L.popup({"maxWidth": "100%"});

        
            
                var html_f6967754ecf2af4fe03944c364423941 = $(`<div id="html_f6967754ecf2af4fe03944c364423941" style="width: 100.0%; height: 100.0%;">Алмаз Синема Алтуфьевский</div>`)[0];
                popup_54d3967dc8097ffd96c7e5be080e4246.setContent(html_f6967754ecf2af4fe03944c364423941);
            
        

        marker_a03c74a994ff84c20bedf47499cfc300.bindPopup(popup_54d3967dc8097ffd96c7e5be080e4246)
        ;

        
    
    
            var marker_00013da97f727e4f5123f9f7c08c5d7a = L.marker(
                [55.79578699283469, 37.61686033558203],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_0d7f3508223799e4b56b89a9548a01f2 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_00013da97f727e4f5123f9f7c08c5d7a.setIcon(icon_0d7f3508223799e4b56b89a9548a01f2);
        
    
        var popup_c4231c9fe0af642f1efb2fb301747442 = L.popup({"maxWidth": "100%"});

        
            
                var html_2047877132e198f1211ab2fb7eddcb42 = $(`<div id="html_2047877132e198f1211ab2fb7eddcb42" style="width: 100.0%; height: 100.0%;">Синема Стар Марьина Роща</div>`)[0];
                popup_c4231c9fe0af642f1efb2fb301747442.setContent(html_2047877132e198f1211ab2fb7eddcb42);
            
        

        marker_00013da97f727e4f5123f9f7c08c5d7a.bindPopup(popup_c4231c9fe0af642f1efb2fb301747442)
        ;

        
    
    
            var marker_3a64e9f9c296ff0c981c662ec84960df = L.marker(
                [55.754697098266014, 37.621521400000006],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_f916229e4f159c26c46f088161ec677a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_3a64e9f9c296ff0c981c662ec84960df.setIcon(icon_f916229e4f159c26c46f088161ec677a);
        
    
        var popup_d5df389f22304dd66b39befb0c710258 = L.popup({"maxWidth": "100%"});

        
            
                var html_3bb2809eece30a1873a7a78fe3ce5354 = $(`<div id="html_3bb2809eece30a1873a7a78fe3ce5354" style="width: 100.0%; height: 100.0%;">Кинозал ГУМа</div>`)[0];
                popup_d5df389f22304dd66b39befb0c710258.setContent(html_3bb2809eece30a1873a7a78fe3ce5354);
            
        

        marker_3a64e9f9c296ff0c981c662ec84960df.bindPopup(popup_d5df389f22304dd66b39befb0c710258)
        ;

        
    
    
            var marker_0de6e90663513dd64c227a1a10120fd2 = L.marker(
                [55.61854815801913, 37.50704511719664],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_a22ef3ed02775203aef0f670d0ad98db = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_0de6e90663513dd64c227a1a10120fd2.setIcon(icon_a22ef3ed02775203aef0f670d0ad98db);
        
    
        var popup_a39f8d40228bae92fed987b867257ef2 = L.popup({"maxWidth": "100%"});

        
            
                var html_9797bdbf7bac97de6c7f328856b205d3 = $(`<div id="html_9797bdbf7bac97de6c7f328856b205d3" style="width: 100.0%; height: 100.0%;">Синема Стар Принц Плаза</div>`)[0];
                popup_a39f8d40228bae92fed987b867257ef2.setContent(html_9797bdbf7bac97de6c7f328856b205d3);
            
        

        marker_0de6e90663513dd64c227a1a10120fd2.bindPopup(popup_a39f8d40228bae92fed987b867257ef2)
        ;

        
    
    
            var marker_e7e1b9a8535035740e20a944ef6a04f5 = L.marker(
                [55.68979848459416, 37.60269286640937],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_0362f7eee7bb4bad67a95e18316b632d = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_e7e1b9a8535035740e20a944ef6a04f5.setIcon(icon_0362f7eee7bb4bad67a95e18316b632d);
        
    
        var popup_7a9b26cf2fe8875610e8c8fb54d0a3bc = L.popup({"maxWidth": "100%"});

        
            
                var html_4fd248d3be5ce6b970f77650a827db33 = $(`<div id="html_4fd248d3be5ce6b970f77650a827db33" style="width: 100.0%; height: 100.0%;">Синема Стар Рио на Академической</div>`)[0];
                popup_7a9b26cf2fe8875610e8c8fb54d0a3bc.setContent(html_4fd248d3be5ce6b970f77650a827db33);
            
        

        marker_e7e1b9a8535035740e20a944ef6a04f5.bindPopup(popup_7a9b26cf2fe8875610e8c8fb54d0a3bc)
        ;

        
    
    
            var marker_056c723320fdcb2aa8629d8d814efcda = L.marker(
                [55.79780599999999, 37.93847800000003],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_e67743387d67852d84d1ad55514efe99 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_056c723320fdcb2aa8629d8d814efcda.setIcon(icon_e67743387d67852d84d1ad55514efe99);
        
    
        var popup_6a3f44da0ddd8316571f86ca01d9ded8 = L.popup({"maxWidth": "100%"});

        
            
                var html_fb84e8137351d6686c481d626575784a = $(`<div id="html_fb84e8137351d6686c481d626575784a" style="width: 100.0%; height: 100.0%;">Prada 3D (Балашиха)</div>`)[0];
                popup_6a3f44da0ddd8316571f86ca01d9ded8.setContent(html_fb84e8137351d6686c481d626575784a);
            
        

        marker_056c723320fdcb2aa8629d8d814efcda.bindPopup(popup_6a3f44da0ddd8316571f86ca01d9ded8)
        ;

        
    
    
            var marker_05ad618c8dc388ba1b2ed680da5bb106 = L.marker(
                [55.909290781419024, 37.540605150787314],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_c4deb5990188f9bc6331256e290046e6 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_05ad618c8dc388ba1b2ed680da5bb106.setIcon(icon_c4deb5990188f9bc6331256e290046e6);
        
    
        var popup_148be3acff23b56c806ec0afdca558ca = L.popup({"maxWidth": "100%"});

        
            
                var html_10935ec350afb3e9d4d8daa7aba4f905 = $(`<div id="html_10935ec350afb3e9d4d8daa7aba4f905" style="width: 100.0%; height: 100.0%;">Синема Стар Дмитровка</div>`)[0];
                popup_148be3acff23b56c806ec0afdca558ca.setContent(html_10935ec350afb3e9d4d8daa7aba4f905);
            
        

        marker_05ad618c8dc388ba1b2ed680da5bb106.bindPopup(popup_148be3acff23b56c806ec0afdca558ca)
        ;

        
    
    
            var marker_a5afc16765938202e120ffd7b0abcd6c = L.marker(
                [55.574814, 37.580066],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_906d7f7ffbbee17e286db257e0e86783 = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_a5afc16765938202e120ffd7b0abcd6c.setIcon(icon_906d7f7ffbbee17e286db257e0e86783);
        
    
        var popup_7c30977ee454a5f00856331282ea0aa0 = L.popup({"maxWidth": "100%"});

        
            
                var html_c9c277ed6025bbb6da81f345ba78c863 = $(`<div id="html_c9c277ed6025bbb6da81f345ba78c863" style="width: 100.0%; height: 100.0%;">Бульвар</div>`)[0];
                popup_7c30977ee454a5f00856331282ea0aa0.setContent(html_c9c277ed6025bbb6da81f345ba78c863);
            
        

        marker_a5afc16765938202e120ffd7b0abcd6c.bindPopup(popup_7c30977ee454a5f00856331282ea0aa0)
        ;

        
    
    
            var marker_5967ccadefab92e949c4837e93582603 = L.marker(
                [55.639959, 37.758204],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_55996b042118f6d4ac7bdc8da10f563a = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_5967ccadefab92e949c4837e93582603.setIcon(icon_55996b042118f6d4ac7bdc8da10f563a);
        
    
        var popup_1bdb7afb8a99daa88061a895a0dddc2c = L.popup({"maxWidth": "100%"});

        
            
                var html_d7e913d90111175b898f0f7d6bf87532 = $(`<div id="html_d7e913d90111175b898f0f7d6bf87532" style="width: 100.0%; height: 100.0%;">Pushka в ТРК Ключевой</div>`)[0];
                popup_1bdb7afb8a99daa88061a895a0dddc2c.setContent(html_d7e913d90111175b898f0f7d6bf87532);
            
        

        marker_5967ccadefab92e949c4837e93582603.bindPopup(popup_1bdb7afb8a99daa88061a895a0dddc2c)
        ;

        
    
    
            var marker_84a895bdb9334197548a2a5b92c7b113 = L.marker(
                [55.891698, 37.748619],
                {}
            ).addTo(map_67f07251aafe8124cfcd2a4e05955538);
        
    
            var icon_df3dbde9b02885286d325ecb42ff94df = L.AwesomeMarkers.icon(
                {"extraClasses": "fa-rotate-0", "icon": "info-sign", "iconColor": "white", "markerColor": "gray", "prefix": "glyphicon"}
            );
            marker_84a895bdb9334197548a2a5b92c7b113.setIcon(icon_df3dbde9b02885286d325ecb42ff94df);
        
    
        var popup_b4b6602f9a645638400caafd31914c05 = L.popup({"maxWidth": "100%"});

        
            
                var html_8482913c7482f1a83101723050be7176 = $(`<div id="html_8482913c7482f1a83101723050be7176" style="width: 100.0%; height: 100.0%;">Глобал Синема XL </div>`)[0];
                popup_b4b6602f9a645638400caafd31914c05.setContent(html_8482913c7482f1a83101723050be7176);
            
        

        marker_84a895bdb9334197548a2a5b92c7b113.bindPopup(popup_b4b6602f9a645638400caafd31914c05)
        ;

        
    
</script>
</html>
