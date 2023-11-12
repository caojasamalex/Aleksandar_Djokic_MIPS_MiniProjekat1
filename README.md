# Mini Projekat - Prvi domaći zadatak iz MIPS-a

## Autor

- [@Aleksandar Đokić 605-2021](https://www.github.com/caojasamalex)

## Postavka projekta

Potrebno je realizovati mikrokontrolersko kolo koje će vršiti kontolu paljenja/gašenja led diode.

Odabir Port-a vrši se na sledeći način:\
**1. Ukoliko ima više samoglasnika u imenu i prezimenu, koristićemo Port A mikrokontrolera**\
**2. Ukoliko ima više suglasnika u imenu i prezimenu, koristićemo Port B mikrokontrolera**

U mom slučaju (Aleksandar Đokić) koristićemo Port B s obzirom da u mom imenu i prezimenu ima više suglasnika nego samoglasnika.

Nakon što smo uspesno odredili koji Port treba koristiti, određujemo Pin koji će se koristiti.

Odabir Pin-a vrši se na sledeći način:\
**Broj slova u imenu i prezimenu po modulu 6 --> (10 + 5) % 6 = 3**

Na osnovu postavke, u mom slučaju, koristimo **Port B** i njegov **Pin 3.**

Način rada diode određen je tako da simulira PWM (Pulse Width Modulation)

![PWM Signal](https://wiki.analog.com/_media/university/courses/electronics/pwm-signal.png?w=500&tok=0492e2)

**Broj ponavljanja prvog takta jednak je broju slova u imenu - **U mom slučaju 10****
#### **Prvi takt**

Širina impulsa u prvom taktu - **Broj slova u imenu u milisekundama** - 10 ms\
Širina pauze u prvom taktu - **Broj slova u prezimenu u milisekundama** - 5 ms

**Broj ponavljanja drugog takta jednak je broju slova u prezimenu - **U mom slučaju 5****
#### **Prvi takt**
U ovom taktu se rotiraju širine impulsa i pauze prethodnog takta

Širina impulsa u prvom taktu - **Broj slova u prezimenu u milisekundama** - 5 ms\
Širina pauze u prvom taktu - **Broj slova u imenu u milisekundama** - 10ms
