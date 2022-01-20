# MD-Flash-Cart-4MB
Простейший перезаписываемый картридж для MegaDrive максимального объема 4МБайта (32Мбита), аппаратно совместимый с программатором FlashKit MD.

![MDFC4MB-github](https://user-images.githubusercontent.com/24475390/149984222-c1a1d27c-d783-4d6d-8eb3-69ddee26fa4a.jpg)

Предлагается авторский проект печатной платы в формате KiCad (содержащий готовую компиляцию в формат Gerber для отправки на производство), позволяющий изготовить картридж для игровой приставки Sega MegaDrive/Genesis, реализованный с учетом минимальной необходимости и достаточности схемотехнического решения с применением микросхемы флэш-памяти MXIC MX29L3211 (конструктивно возможно применение также и MX29LV320) в корпусе (P)SOP-44.

![MDFC4MB-PCB-github](https://user-images.githubusercontent.com/24475390/150021381-3bffb65b-c416-45cf-a307-c182a318816e.jpg)

Проект полностью протестирован на работоспособность. Помимо микросхемы памяти потребуется также интегральный стабилизатор напряжения AMS1117 на 3.3В (для обеспечения штатного питания данной микросхемы), а также шунтирующий конденсатор номиналом от 100нФ согласно документации (маркировка "104"). Конденсатор необходим для стабильной работы картриджа в приставке (для работы с программатором не обязателен). Стабилизатор можно заменить светодиодом в smd-корпусе (припаять к площадкам входа и выхода стабилизатора: правая и центральная - катодом к центральной). Светодиод при последовательном включении обеспечивает падение напряжения на нём около 1.6В (т.е. прямо то, что нужно) - приятным же бонусом в этом случае будет индикация "активности" картриджа, обусловленная различным током потребления микросхемы памяти в разных режимах и как следствие разной яркости и периодичности вспышек светодиода (в ждущем режиме малый ток - не светится совсем).

*PS.* Для работы с данным картриджем (его записи) необходима расширенная версия утилиты управления интерфейсом FlashKit MD: [Flashkit MD Plus](https://github.com/MiGeRA/FlashKit-MD-Plus) версии от 1.0.2.0 (время записи полного объема картриджа ~150сек).

*PPS.* Будучи полностю совместимым с программатором FlashKit MD и приставками, для которых он предназначен - данный картридж минимум втрое дешевле по сбестоимости чем функционально подобный [предлагает krikzz](https://krikzz.com/our-products/cartridges/flashkitmd.html) и вдвое чем [KY-tech](https://www.aliexpress.com/item/1005001465109297.html). С учетом применения микросхемы в "крупном корпусе" (P)SOP-44 требования к скиллованности пайки минимальны ;-)
