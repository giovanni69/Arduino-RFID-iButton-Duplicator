# Arduino-RFID-iButton-Duplicator
  Доработка проекта "Копировальщик ключей для домофона RFID с OLED дисплеем и хранением 8 ключей в памяти EEPROM"
  Автор: МЕХАТРОН DIY, AlexMalov, 2019 https://github.com/AlexMalov/EasyKeyDublicatorRFID_OLED/
  Аппаратная часть построена на Arduino Nano или Arduino Pro Mini
# Мои доработки
  1. Переназначил вывод генерации 125 кГц с вывода 11 на вывод 3 чтобы освободить шину SPI;
  2. Добавлена подержка работы с модулем MFRC522, модуль подключается по SPI шине к 11-12-13 пинам Arduino и позволяет копировать ключи Mifare Classic 1K 13.56Mhz;
  3. Написаны функции чтения и записи UID в брелок типа Mifare Zero, этого как правило достаточно для нормальной работы брелка;
  4. Добавил возможность принудительной очистки EEPROM, для этого перед вкл. прибора нужно зажать кнопку энкодера и неотпускать ее пока не засветится красный светодиод
  5. Также в место режима blueMode я сделал режим очистки и восстановления Mifare брелка, когда метка неопределяется и нечитается пробуем этот режим. Если кому то нужен режим blueMode, то просто раскоментируйте #define BLUE_MODE в начале кода;
