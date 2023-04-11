# Zkušenosti se Seeed Studio Xiao nRF52840 / Arduino Nano 33 BLE / Micro:Bit v2

1. Mít vždy připravené Raspberry PI s openocd a kabely s pogo piny na rychlé přemazání čipu (zatím využito asi 6x)
2. BLE je otravně složité, ale jde použít klasické nordic 1Mbit radio (nicméně Mbed-os ma zabraný handler přerušení, takže je potřeba extra thread na testování flagů, nebo eventy namapovat na softwarové přerušení)
3. Nekombinovat USB related headery (Mouse + Keyboard -> bod 1.)
4. Sračkové knihovny způsobují velice záhadné tuhnutí programů - knihovna pro Bosh akcelerometr opomněla u některých funkcí vracet návratové hodnoty a Mbed Os RTOS se z toho krapet zbláznil a zasekl
5. Nano 33 BLE Sense Rev.2 nemá snad jediný senzor stejný jako Rev.1 (pro případ, že nic nechce fungovat)
6. Údajně by mělo jít použít i st-link, ale zatím se to ukázalo být jako slepá ulička (win měl problémy s libusb, RPi taky nějak nefungovalo)
7. Exaple pro BLE HID mouse/keyboard fungoval s Adroidem, windows jej ignorovaly
8. Micro:bit desky (s nRF52833) je těžké zablokovat - mají vlastní debugger a v PlatformIO funguje na první dobrou. Na druhou stranu PIO při kompilaci cpe špatné definice (-D) a není pak "vidět" druhý port, případně špatný zdroj pro 32k a program "Mrzne" jelikož je RTC použito pro millis (použije se konfigurace pro krystal, ale microbit žádný na desce nemá)
