# 🌀 Fan RPM Monitoring System / Система измерения оборотов вентилятора

📌 This is a hardware-software system built using **LabVIEW** and analog electronics to measure **fan speed (RPM)**, **current**, and **voltage**, without using built-in tachometers.  
📌 Это аппаратно-программная система, созданная с помощью **LabVIEW** и аналоговой схемотехники для измерения **частоты вращения вентилятора (об/мин)**, **тока** и **напряжения**, **без использования встроенных тахосистем**.

---

## 🔧 Features / Особенности

- **Tachometer-free rotation sensing** using a slit + photodiode & LED / Определение оборотов без тахометра: щель, фотодиод и светодиод
- **Fan speed control** via voltage regulation (transistor + slider) / Регулировка скорости через ползунок и транзистор
- **Voltage & current sensing** with an inline resistor / Измерение тока через резистор и расчет по закону Ома
- **Logging to `.log` file** with timestamped data / Запись данных в `.log` файл с метками времени
- **Clean session start** – new launch creates a new `.log` file / Каждый запуск программы создает новый лог, не дописывает старый
- **Graphical interface** with indicators and real-time charts / Графический интерфейс: индикаторы, графики, контроль



## ⚙️ System Setup / Аппаратная реализация

| Component | Purpose / Назначение |
|----------|----------------------|
| Photodiode ФД-303 | Rotation detection / Обнаружение вращения |
| Red LED | Light source / Источник света |
| Transistor КТ630Г | Voltage control / Управление напряжением |
| Resistor R2 | Current sensing / Измерение тока |
| PCI-1202LU | Data acquisition / Сбор данных |
| LabVIEW | Interface & logic / Интерфейс и логика |

🛠 Rotation is counted when the slot in the fan cover transmits light from the LED onto the photodiode, detecting a voltage surge.

🛠 Вращение засчитывается, когда прорезь в крышке вентилятора пропускает свет от светодиода на фотодиод, фиксируя всплеск напряжения.


## 💻 How to Run / Как запустить

1. Установите LabVIEW (2020+).
2. Подключите PCI-1202LU.
3. Откройте `Top7best.vi` в LabVIEW.
4. Убедитесь, что фотодиод и светодиод корректно установлены.
5. Запустите VI: вращение, ток и напряжение начнут логгироваться.
6. Данные автоматически сохраняются в `.log` файл в указанной директории.

---

1. Install LabVIEW (2020+).
2. Connect PCI-1202LU.
3. Open the `Top 7 best.vi` in LabVIEW.
4. Make sure that the photodiode and LED are correctly installed.
5. Start VI: rotation, current and voltage will start logging.
6. The data is automatically saved to a `.log` file in the specified directory.


![image](https://github.com/user-attachments/assets/2ecdcd48-6891-4ec7-979d-42e0b8b0299c)


## 📁 Пример содержимого `.log`:
![image](https://github.com/user-attachments/assets/8a7e850d-f8a7-4581-b726-7ab898c24b3a)


## 📚 Topics Covered / Используемые темы

- Analog electronics and circuitry / Аналоговая электроника и схемотехника 
- Work with physical sensors and transistors / Работа с физическими датчиками и транзисторами
- Programming in LabVIEW / Программирование в LabVIEW
- Data collection and logging / Сбор и логгирование данных
- Organization of operator interfaces / Организация интерфейсов оператора
---

🤝 Author | Автор Made with ❤️ by Ayi4ka in 2023 / Сделано с любовью — Айка в 2023 году
