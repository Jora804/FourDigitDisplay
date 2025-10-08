# FourDigitDisplay

Библиотека для управления четырёхразрядными семисегментными дисплеями с общим катодом на Arduino.

## Возможности

- Отображение чисел на четырёхразрядном дисплее
- Управление отдельными сегментами
- Очистка дисплея
- Совместимость с большинством Arduino-плат

## Установка

### Через Library Manager
После публикации вы сможете найти библиотеку в Arduino IDE → Sketch → Include Library → Manage Libraries → FourDigitDisplay.

### Вручную
Скачайте репозиторий с [GitHub](https://github.com/Jora804/FourDigitDisplay.git) и скопируйте папку `FourDigitDisplay` в `libraries` вашего Arduino IDE.

## Пример использования

```cpp
#include <FourDigitDisplay.h>

FourDigitDisplay display(2,3,4,5,6,7,8,9);

void setup() {
  display.begin();
}

void loop() {
  for (int i = 0; i <= 9999; i++) {
    display.showNumber(i);
    delay(500);
  }
}
