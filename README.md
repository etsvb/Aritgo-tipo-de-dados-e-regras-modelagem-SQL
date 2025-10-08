# Tipos de dados e regras na modelagem SQL

Introdução:
Os tipos de dados SQL são fundamentais para a definição e estruturação de informações dentro de um banco de dados relacional. Eles determinam o tipo de valor que uma coluna pode armazenar, garantindo a integridade e a consistência dos dados. Cada tipo de dado tem características próprias que influenciam a forma como os dados são armazenados e manipulados.

Os principais tipos de dados SQL incluem:

- Numéricos;

- Caractere e Cadeias de Texto;

- Data e Hora;

- Booleanos.

Além desses, existem outros tipos especializados, como os de dados geográficos (GEOMETRY), e os de identificadores únicos, como UUID. Compreender e escolher corretamente os tipos de dados é essencial para o bom desempenho e para a integridade do banco de dados. Vamos comentar dos quatros principais.

---

# Dados númericos

As colunas numéricas em SQL armazenam diferentes tipos de números e podem representar quatro escalas de medição:

`Nominal`: Números usados como rótulos, sem ordem ou valor numérico real (ex: número de telefone, ID de estudante).

`Ordinal`: Representam ordem ou classificação, mas sem diferença mensurável entre os valores (ex: escala de humor de 1 a 3).

`Intervalo`: Permitem medir diferenças exatas entre os valores, mas o zero não significa ausência (ex: temperatura em graus, datas).

`Razão`: Igual à escala de intervalo, mas com zero absoluto, que indica ausência total (ex: peso, duração, altura).

Diferente de outros tipos de dados, os numéricos podem representar todas essas escalas, o que os torna versáteis em diferentes contextos.

---

# String

É referente a um tipo de dado que armazena diferentes sequências de caracteres, como texto. Usadas para representar dados textuais, o SQL oferece vários tipos de dados (como `CHAR`, `VARCHAR` e `TEXT`) para essa finalidade. Além disso, o SQL possui diversas funções para manipular strings, como `CONCAT()` para unir strings, `LOWER()` e `UPPER()` para converter para maiúsculas/minúsculas, `SUBSTRING()` para extrair partes de uma string e `REPLACE()` para substituir caracteres.

Tipos de dados de string

- `CHAR`: Armazena strings de comprimento fixo, preenchendo com espaços se necessário. 

- `VARCHAR`: Armazena strings de comprimento variável, ocupando apenas o espaço necessário para os dados. 

- `TEXT`: Usado para armazenar textos mais longos, com um comprimento máximo maior que `VARCHAR`.

---

# Data e Hora

O tipo de dado de data e hora são usados para representar valores temporais, com eles podemos fazer cálculos e operações cronológicas. 
São eles os mais padrões: `DATE` / `TIME` / `TIMESTAMP` / `INTERVAL`.

`DATE`: É usado para armazenar datas sem a hora exata;

`TIME`: Nos permite armazenar tempo sem data;

`DATETIME`: Permite armazenar data e horas juntos;

`INTERVAL`: É usado para armazenar informações sobre intervalos de tempo.

 

# Booleanos

O tipo de dado booleano(BOOLEAN) serve para armazenar valores lógicos para representar verdadeiro`(TRUE)` ou `falso(FALSE)`.  Ele é ideal para situações que exigem uma resposta binária, como “sim ou não” e “ligado ou desligado”. 

No booleano se usa: `TRUE` // `FALSE` // `NULL`.

`TRUE`: Representa 1 ou Verdadeiro.

`FALSE`: Representa 0 ou Falso.

`NULL`: Representa “Desconhecido”.

