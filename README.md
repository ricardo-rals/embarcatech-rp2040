# Embarcatech RP2040

Projetos de sistemas embarcados em C para o Raspberry Pi Pico e a placa BitDogLab, feitos durante a residência Embarcatech entre dezembro de 2024 e fevereiro de 2025.

Cada pasta era um repositório separado. Eles foram reunidos aqui com o histórico de commits original preservado.

| Projeto | O que faz | Conceitos |
| --- | --- | --- |
| [co2-detector](co2-detector) | Simula a detecção de CO2 em ambiente fechado e aciona um exaustor, com alerta em LED RGB, buzzer e display OLED | ADC, PWM, I2C |
| [conversores-AD](conversores-AD) | Joystick controla a intensidade de LEDs RGB e a posição de um quadrado no display SSD1306 | ADC, PWM, I2C |
| [comunicacao-serial-RP2040](comunicacao-serial-RP2040) | Controla LEDs comuns, matriz WS2812 e display SSD1306 a partir de botões e da serial | Serial USB, I2C, PIO |
| [ServoPWMController](ServoPWMController) | Posiciona um servo motor com PWM | PWM |
| [button-control-led](button-control-led) | Acende LEDs a partir de botões | GPIO |
| [traffic_light](traffic_light) | Simula um semáforo na BitDogLab | GPIO, temporizadores |
| [display_numbers](display_numbers) | Mostra números de 0 a 9 na matriz de LEDs, controlados por dois botões | GPIO, PIO |
| [led-matrix-5x5-animations](led-matrix-5x5-animations) | Animações na matriz de LEDs 5x5, feitas em grupo | PIO, WS2812 |
| [controle-de-pinos-GPIO-teclado-matricial](controle-de-pinos-GPIO-teclado-matricial) | LEDs e buzzer controlados por teclado matricial no Pico W | GPIO |
| [controle-de-pinos-GPIO-bitdolgab](controle-de-pinos-GPIO-bitdolgab) | Controle de periféricos da BitDogLab, feito em grupo | GPIO |
| [sos_blink](sos_blink) | Pisca SOS em código Morse num LED | GPIO, temporização |
| [conversion_units_embarcatech](conversion_units_embarcatech) | Conversor de unidades em C com testes, feito em grupo | C, CUnit |

## Como compilar

Cada projeto usa o Pico SDK com CMake. Com o SDK instalado e a variável `PICO_SDK_PATH` configurada:

```bash
cd co2-detector
mkdir build && cd build
cmake ..
make
```

Depois copie o arquivo `.uf2` gerado para o Pico em modo BOOTSEL.
