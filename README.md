# Teclado


```bash
sudo pacman -Syu
```
```bash
sudo pacman -S --needed git python python-pip avr-gcc avr-libc arm-none-eabi-gcc arm-none-eabi-binutils dfu-programmer dfu-util avrdude clang
```
```bash
sudo pipx install qmk
```
```bash
qmk setup 
```
Posterior a instalar qmk y sus dependencias 

```bash
cd ~/qmk_firmware/keyboards
```
```bash
qmk new-keyboard
```

Rellenas los campos que te pida y tú microcontrolador, posterior a ello borras toda la info dentro del directorio de tu nuevo teclado, y copias la de este repo 

```bash
qmk compile -kb <tu_teclado> -km default
```
```bash
qmk flash  -kb <tu_teclado> -km default
```
Así debería funcionar sin problema, sino llegase a funcionar 

```bash
cd ~/qmk_firmware/keyboards/Lily58/keymaps

```
Pegas directamente el directorio de druotoni, y ejecutas 

```bash
qmk flash  -kb Lily58 -km druotoni
```
