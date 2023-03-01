# hse_hw2_chip
## Автор: Белова Наталья
[Ссылка на Google-Colab](https://colab.research.google.com/drive/1Ax1gdUdrt4AkWXrsGA5_9oggoQPMK1hF?usp=sharing)

Клеточная линия: PC-3

Гистоновая метка: H2AFZ

Реплики: ENCFF598PWF, ENCFF700QWJ

Контроль: ENCFF829PCB

### FastQC анализ исходных файлов (до подрезания)
**Первая реплика**
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/first_before1.png)
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/first_before2.png)
**Вторая реплика**
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/second_before1.png)
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/second_before2.png)
**Контроль**
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/third_before1.png)
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/third_before2.png)

По графикам per tile sequence quality первой реплики и контроля видно, что в некоторых позициях в ридах нарушено качество. Поэтому проведем подрезание чтений.
### FastQC Анализ после подрезания чтений:
**Первая реплика**
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/first_after1.png)
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/first_after2.png)

**Контроль**
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/third_after1.png)
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/third_after2.png)
### Таблица со статистикой по выравниванию

index | Общее число ридов | Выровнившиеся уникально | Выровнившиеся неуникально | Не выровнившиеся 
--- | --- | --- | --- | --- | 
ENCFF829PCB | 42549155 | 2020174 (4.75%) | 5200776 (12.22%)| 35328205 (83.03%)
ENCFF598PWF | 38836404 | 1792482 (4.62%) | 4311831 (11.10%) | 32732091 (84.28%)
ENCFF700QWJ | 73984712 | 3599228 (4.86%) | 8727635 (11.80%) | 61657849 (83.34%)

Большой процент не выровнявшихся ридов связан с тем, что выравнивание происходила по одной хромомсоме, а всего их у человека 23 пары. 

### Диаграммы Эйлера-Венна
![image](https://github.com/alkmnd/hse_hw2_chip/raw/main/images/Снимок_экрана_2023-03-01_в_23.03.36.png)
### Бонусная часть 
