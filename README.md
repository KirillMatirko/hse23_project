# hse23_project

### 1. Описание белка

MINA контролирует пролиферацию и онкогенез глиобластомы, аденокарциномы и других типов рака через деметилирование H3K9 и контроль клеточного цикла путём активации экспрессии циклинов и циклин-зависмых киназ. Исследования показывают, что сокращение экспрессии MINA способствует замедлению развития глиобластомы, что может найти применение в таргетной терапии.

MINA экспрессируется во многих типах тканей. Наивысший уровень экспрессии наблюдается в щитовидной железе, скелетной мышечной ткани, фибробластах и т.д. В своей структуре содержит консервативный домен JmjC, принадлежит к семейству белков ROX. 

**Ссылки на статьи**:

"Structurally, MINA protein contains a conserved jumonji C (JmjC) domain that belongs to the histone demethylases family. It has been reported that MINA is involved in reducing the trimethylation of histone H3K9 (H3K9me3)." (https://pubmed.ncbi.nlm.nih.gov/27292258/)

"We have reported the histone demethylase activity of mdig/MINA. Our biochemical assays shows that immunoprecipitated mdig/MINA from the cells can demethylate H3K9me3 on histone H3 peptide." (https://pubmed.ncbi.nlm.nih.gov/26413213/)

"In this study, we established the functional relevance between MINA53 and DNA replication. We found that knockdown of MINA53 resulted in a decrease of CMG genes expression as well as an upregulation of H3K9me3 at CMG genes promoters." (https://pubmed.ncbi.nlm.nih.gov/30333481/)

<img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/MINA_domains.png" width="700" height="350"> <img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/MINA_expression.png" width="700" height="350">

### 2. Выравнивание гистонов

|Гистон|Выравнивание|<div style="width:100px">Комментарий</div>|
|:-------:|:----------------------:|:---------------:|
|H2A|<img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/H2A_alignment.png" width="1600" height="200">|По сравнению с другими гистонами,различий больше всего. Однако можно заметить, что они в основном заключаются в синонимичных заменах и полиморфизмах. Белки определённо выполняют схожие функции, но всё-таки не являются копиями друг друга. Возможно, различия являются следствием мутаций.|
|H2B|<img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/H2B_alignment.png" width="1600" height="200">|В отличие от H2A, у этого гистона заметно больше консервативных участков. Белки очень схожи, поэтому для дальнейшего анализа можно выбрать любой из них.|
|H3|<img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/H3_alignment.png" width="400" height="130">|Белки являются копиями друг друга. Присутствует всего несколько замен.|
|H4|<img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/H4_alignment.png" width="400" height="130">|Белки являются копиями друг друга. Присутствует всего несколько замен.|

### 3. Таблицы e-value

Запускаем следующую команду для каждой пары белок-протеом какого-то организма. В примере запуск для пары MINA-протеом человека

```bash
blastp -query MINA.fasta -db /mnt/storage/project_2023/proteomes/human.faa -out human.blast -outfmt 7
```

Ниже приведена таблица с наименьшим e-value для каждой пары протеом-гистон/белок, а также эта же таблица, но с -log_10 (e-value).

|     | human	| mouse |	zebrafish	| c.elegans |	drosophila| ciliate	| yeast	| methanocaldococcus | thermococcus	| e.coli | tuberculosis |
|:-------------------:|:---------------:|:----------------:|:---------------:|:----------------:|:----------------:|:---------------:|:--------------:|:---------------:|:----------------:|:-----------------:|:----------------:|
| MINA | 1e-300 |	1e-300 |1e-300| 3.5e-51	| 9.05e-43 | 1.8 | 1.0 | 0.6 | 1.2 | 0.002 | 2.6|
| H2A | 1.63e-89 | 5e-89 | 3.45e-82 | 1.34e-65 | 5.17e-68	| 6.05e-57 | 3.96e-63 |	0.000462 | 0.003 | 1.7 | 0.43 |
| H2B | 2.52e-88 | 1.76e-88 |9.04e-83 | 6.53e-66 | 2.82e-60 | 4.57e-51 | 5.4e-60 | 1.8 | 1.2 | 1.6 | 2.2 |
| H3 | 2.19e-96 | 1.54e-96 | 1.77e-95 | 4.46e-94 | 9.39e-96 | 8.41e-86 | 3.31e-87 | 0.034 | 0.057 | 0.9 | 4.6 |
| H4 | 1.09e-67 | 7.6e-68 | 1.13e-68 | 6.15e-68 | 8.02e-68 | 1.96e-45 | 1.08e-52 | 8.22e-05 | 3.31e-05 | 1.3 |0.069 |

|     | human	| mouse |	zebrafish	| c.elegans |	drosophila| ciliate	| yeast	| methanocaldococcus | thermococcus	| e.coli | tuberculosis |
|:-------------------:|:---------------:|:----------------:|:---------------:|:----------------:|:----------------:|:---------------:|:--------------:|:---------------:|:----------------:|:-----------------:|:----------------:|
| MINA | 300.0 | 300.0 | 300.0 | 50.455931955649724 | 42.0433514207948 | -0.25527250510330607 | -0.0 | 0.2218487496163564 | -0.07918124604762482 |	2.6989700043360187 | -0.414973347970818 |
| H2A | 88.78781239559605 | 88.30102999566398	| 81.46218090492673	| 64.87289520163519	| 67.28650945690606	| 56.21824462534753	| 62.40230481407449 |	3.3353580244438743 | 2.5228787452803374	| -0.2304489213782739	| 0.36653154442041347 |
| H2B | 87.59859945921846	| 87.75448733218585	| 82.04383156952464	| 65.18508681872493	| 59.54975089168064	| 50.34008379993015	| 59.26760624017703	| -0.25527250510330607 | -0.07918124604762482	| -0.2041199826559248	| -0.3424226808222063
| H3 | 95.65955588515988 | 95.81247927916354 | 94.75202673363819	| 93.35066514128786	| 95.02733440773389	| 85.07572071393813	| 86.48017200622428	| 1.4685210829577449 | 1.2441251443275085	| 0.045757490560675115	| -0.6627578316815741 |
| H4 | 66.96257350205937	| 67.11918640771921	| 67.94692155651659	| 67.21112488422459	| 67.09582563171584	| 44.69897000433602	| 51.96657624451305 |	4.0851281824599495	| 4.480172006224281	| -0.11394335230683679	| 1.1611509092627446 |

### 4. Тепловая карта

Используем следующий код для создания тепловой карты:

```python3
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("protenomes_logEval.csv",index_col=0)

f, ax = plt.subplots(figsize=(20,5))
ax = sns.heatmap(df)
ax.set_yticklabels(df.index.values)
plt.show()
````

Ниже приведена тепловая карта, полученная из таблицы с -log_10(e-value). Для большей наглядности структуры карты она продублирована для таблицы, в которой максимальное значение -log_10(e-value) не превосходит 150.

<img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/bioinf_project23_heatmap.png" width="700" height="350"> <img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/bioinf_project23_heatmap2.png" width="700" height="350">

### 5. Вывод

Из тепловой карты мы делаем вывод, что ген MINA, видимо, впервые появился у позвоночных. Однако его ортолог, ген NO66 (или RIOX2) стабильно присутствует и у беспозвоночных организмов (дрозофила фруктовая, сaenorhabditis elegans). Белки, кодируемые этими генами, имеют очень схожую доменную структуру и оба обладают эпигенетическими функциями. В доказательство последнего см. групповую часть проекта.
