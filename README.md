# Atividade de Mineração de Texto em R - Motor de Busca

Este projeto implementa um pipeline simples de **mineração de texto** em R, utilizando textos da Wikipédia sobre três cidades do litoral paulista: **Santos**, **São Vicente (São Paulo)** e **Cubatão**.

## 📌 Objetivos
- Coletar textos automaticamente da Wikipédia via API.
- Tokenizar os textos (converter em palavras individuais).
- Construir um vocabulário único.
- Calcular frequências de termos.
- Gerar uma **Matriz Termo-Documento (TDM)**.
- Implementar busca booleana simples.
- Calcular **TF-IDF** para identificar termos mais relevantes.

## 🛠️ Pacotes utilizados
- [`httr2`](https://cran.r-project.org/web/packages/httr2/index.html): para acessar a API da Wikipédia.
- Funções base do R (`tolower`, `gsub`, `strsplit`, `table`, etc.).

## 📂 Estrutura do código
1. **Coleta de dados**  
   Função `baixar_wiki()` que consulta a API da Wikipédia e retorna o texto de cada cidade.

2. **Tokenização**  
   Função `tokenizar()` que:
   - Converte para minúsculas.
   - Remove pontuação e números.
   - Normaliza espaços.
   - Divide em tokens (palavras).

3. **Vocabulário e Frequência**  
   - Criação de um vocabulário único (`vocab`).
   - Cálculo da frequência total de cada termo no corpus.

4. **Matriz Termo-Documento (TDM)**  
   - Cada linha representa um termo.
   - Cada coluna representa um documento (cidade).
   - Os valores são as contagens de ocorrência.

5. **Busca Booleana**  
   Função `busca_booleana()` que retorna em quais documentos um termo aparece.

6. **TF-IDF**  
   Implementação manual do cálculo de TF-IDF para destacar termos mais relevantes.

## ▶️ Como executar
1. Instale o pacote `httr2`:
   ```r
   install.packages("httr2")
