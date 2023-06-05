# hse23_project

### 1. Описание белка

MINA контролирует пролиферацию и онкогенез глиобластомы, аденокарциномы и других типов рака через деметилирование H3K9 и контроль клеточного цикла путём активации экспрессии циклинов и циклин-зависмых киназ. Исследования показывают, что сокращение экспрессии MINA способствует замедлению развития глиобластомы, что может найти применение в таргетной терапии.

MINA экспрессируется во многих типах тканей. Наивысший уровень экспрессии наблюдается в щитовидной железе, скелетной мышечной ткани, фибробластах и т.д. В своей структуре содержит консервативный домен JmjC, принадлежит к семейству белков ROX. 

**Ссылки на статьи**:

"Structurally, MINA protein contains a conserved jumonji C (JmjC) domain that belongs to the histone demethylases family. It has been reported that MINA is involved in reducing the trimethylation of histone H3K9 (H3K9me3)." (https://pubmed.ncbi.nlm.nih.gov/27292258/)

"We have reported the histone demethylase activity of mdig/MINA. Our biochemical assays shows that immunoprecipitated mdig/MINA from the cells can demethylate H3K9me3 on histone H3 peptide." (https://pubmed.ncbi.nlm.nih.gov/26413213/)

"In this study, we established the functional relevance between MINA53 and DNA replication. We found that knockdown of MINA53 resulted in a decrease of CMG genes expression as well as an upregulation of H3K9me3 at CMG genes promoters." (https://pubmed.ncbi.nlm.nih.gov/30333481/)

<img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/MINA_domains.png" width="700" height="350"> <img src="https://github.com/KirillMatirko/hse23_project/blob/main/pics/MINA_expression.png" width="700" height="350">

### 3. Таблицы e-value

Ниже приведена таблица с наименьшим e-value для каждой пары протеом-гистон/белок, а также эта же таблица, но с -log_10 (e-value).

|     | human	| mouse |	zebrafish	| c.elegans |	drosophila| ciliate	| yeast	| methanocaldococcus | thermococcus	| e.coli | tuberculosis |
|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|
| MINA | 1e-300 |	1e-300 |1e-300| 3.5e-51	| 9.05e-43 | 1.8 | 1.0 | 0.6 | 1.2 | 0.002 | 2.6|
| H2A | 1.63e-89 | 5e-89 | 3.45e-82 | 1.34e-65 | 5.17e-68	| 6.05e-57 | 3.96e-63 |	0.000462 | 0.003 | 1.7 | 0.43 |
| H2B | 2.52e-88 | 1.76e-88 |9.04e-83 | 6.53e-66 | 2.82e-60 | 4.57e-51 | 5.4e-60 | 1.8 | 1.2 | 1.6 | 2.2 |
| H3 | 2.19e-96 | 1.54e-96 | 1.77e-95 | 4.46e-94 | 9.39e-96 | 8.41e-86 | 3.31e-87 | 0.034 | 0.057 | 0.9 | 4.6 |
| H4 | 1.09e-67 | 7.6e-68 | 1.13e-68 | 6.15e-68 | 8.02e-68 | 1.96e-45 | 1.08e-52 | 8.22e-05 | 3.31e-05 | 1.3 |0.069 |
