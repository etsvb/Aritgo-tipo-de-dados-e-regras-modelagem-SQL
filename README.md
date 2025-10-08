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

---

# Constraints

No SQL, uma constraint é uma regra aplicada a uma ou mais colunas de uma tabela para impor restrições aos dados que podem ser inseridos ou modificados.


Existem vários tipos de constraints no SQL, incluindo:

- `Primary Key` (Chave Primária): Uma constraint que garante a unicidade e a não nulidade de uma coluna ou conjunto de colunas. É usada para identificar exclusivamente cada registro em uma tabela.


 - `Foreign Key` (Chave Estrangeira): Uma constraint que estabelece uma relação entre duas tabelas, garantindo que os valores em uma coluna correspondam aos valores em outra coluna de outra tabela.


- `Unique` (Único): Uma constraint que garante que os valores em uma coluna ou conjunto de colunas sejam únicos em uma tabela.


- `Not Null` (Não Nulo): Uma constraint que garante que uma coluna não possa conter valores nulos.

- `Check` (Verificação): Uma constraint que define uma condição que os valores de uma coluna devem atender.


A restrição default em SQL define um valor padrão para uma coluna em uma tabela, que será automaticamente inserido em um novo registro se nenhum valor for fornecido para essa coluna na operação de `INSERT`. Isso garante que a coluna sempre tenha um valor, seja ele um número, texto, data ou até mesmo o resultado de uma função de sistema, como `GETDATE()`. 


Essas constraints são usadas para impor integridade nos dados do banco de dados, garantindo que apenas valores válidos sejam armazenados nas tabelas e mantendo a consistência dos dados.
