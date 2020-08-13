# Felanmälan från IoT-system

## Scenario version 1
Felanmälningar från IoT-sensorer till fastighetssystemet.

1. Samtliga sensorer finns representerade i fastighetsystemet som fi2equipment-entiteter
1. IoT-systemet ansvarar för att översätta mätvärden/signaler från en sensor till ett larm-meddelande och en prioritet.
1. IoT-systemet skapar en felanmälan/arbetsorder i fastighetssystemet baserat på feltext, prioritet och fi2equipment-ID via ett POST-anrop till [fi2case](http://www.fastapi.se/apidocprop/v1_WP/ApiDatamodel/fi2case) med innehåll enligt [exempel](https://github.com/FAST2/iot-case-xml/blob/master/fi2case_POST.xml)
1. fastAPI-implementationen returnerar ID i version 1 enbart ID-värden för det fi2case och fi2order som skapats

----
## Version 2
1. Möjlighet för IoT-systemet att söka efter sensorer via lämplig typning i fastAPI. Detta för att underlätta koppling mellan sensor och ID-begrepp för fi2equipment

----
## Revisionshistorik
[Historik](https://github.com/FAST2/iot-case-xml/commits/master)
