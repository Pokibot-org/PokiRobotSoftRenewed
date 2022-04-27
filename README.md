# PokiRobotSoftRenewed

Using the zephyr west tool instead of platformio.

ZEPHYR VERSION: 2.7

## SOURCEZ !!!!!!!!

Avant toute chose: 

 - pip install west
 - clonez zephyr os 
 - checkout sur le tag Version 2.7.
 - sourcez zephyr/zephyr-env.sh

## BUILD
```bash
west build -bnucleo_f446re_pokibot --build-dir build-nucleo-poki
```

Pour un build clean, rajoutez: --pristine

## UNIT TEST

```
twister -T tests
ou bien 
twister -T tests/<TEST SUITE QUE VOUS VOULEZ>
```

