# 🧩 Quebra-Cabeça de Matemática: Funções e Encaixe Aritmético

![Disciplina](https://img.shields.io/badge/Disciplina-C%C3%A1lculo%20I-blue)
![Ferramenta](https://img.shields.io/badge/Ferramenta-GeoGebra-lightgrey)
![Instituição](https://img.shields.io/badge/PUC-Campinas-informational)
![Status](https://img.shields.io/badge/Status-Em%20desenvolvimento-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

---

<div align="center">
  <!-- Substitua pelo print do tabuleiro final no GeoGebra -->
  <img width="600" alt="Prévia do tabuleiro no GeoGebra" src="docs/tabuleiro.png" />
  <br>
  <em>Prévia do tabuleiro modelado no GeoGebra (substituir pela imagem final).</em>
</div>

---

## 📄 Visão Geral

Este repositório documenta o **Projeto de Cálculo I (Prática) do 2º semestre de 2026**, desenvolvido para os cursos de Engenharia da **PUC-Campinas** (Grupo 2).

A proposta une **rigor matemático e criatividade**: projetar no GeoGebra um **tabuleiro retangular de quebra-cabeça com 16 peças**, em que:

- as **bordas das peças** são traçados de **funções estudadas em Cálculo I**;
- o **encaixe** entre peças vizinhas depende da **equivalência entre resultados de operações aritméticas**.

Mais do que resolver exercícios, o projeto exige **projetar**: é preciso dominar domínio, curvatura e pontos notáveis de cada função para transformá-la em peça, e articular as operações para que os encaixes sejam matematicamente corretos, e não arbitrários.

> 💙 **Impacto social:** os melhores tabuleiros das turmas serão produzidos em MDF e doados pela PUC-Campinas a uma instituição de Barão Geraldo que oferece apoio escolar gratuito a crianças e jovens.

---

## 📐 1. Estrutura do Tabuleiro

| Elemento | Definição |
| :--- | :--- |
| **Centro** | P(0, 0) |
| **Formato** | Retangular |
| **Arestas internas da moldura** | A(−5, −4), B(5, −4), C(−5, 4), D(5, 4) |
| **Arestas externas da moldura** | A'(−6, −5), B'(6, −5), C'(−6, 5), D'(6, 5) |
| **Parte interna** | 16 peças delimitadas por funções |
| **Moldura** | Contém os números-alvo do encaixe aritmético |

---

## 📈 2. Funções Delimitadoras

As fronteiras entre as peças devem usar os tipos de função abaixo. Para a pontuação máxima, o projeto inclui **exatamente o mínimo** de cada tipo:

| Tipo de função | Quantidade |
| :--- | :---: |
| Lineares (máximo permitido) | **2** |
| Exponenciais | **2** |
| Trigonométricas | **2** |
| Logarítmicas | **2** |
| Racionais (quociente de funções) | **2** |
| Polinomiais | **4** |
| **Total** | **14** |

Todas as funções são desenhadas com **domínio restrito ao retângulo interno** do tabuleiro.

---

## 🔹 3. Funções dos Cantos (Corners)

Os cantos são definidos por funções fornecidas no enunciado:

| Canto | Definição |
| :---: | :--- |
| **A** | `h(x)`: polinomial por partes (8 trechos cúbicos) e `g(x)`: arco de circunferência |
| **B** | Reflexão de `h(x)` e `g(x)` em relação ao eixo vertical |
| **C** | `f(x)`: polinomial por partes (6 trechos cúbicos) |
| **D** | Reflexão de `f(x)` em relação ao eixo vertical |

### Pontos de inflexão P<sub>A</sub>, P<sub>B</sub>, P<sub>C</sub> e P<sub>D</sub>

Cada ponto é o **ponto de inflexão** da função do respectivo canto:

1. Calcular `f''(x)` em cada trecho e resolver `f''(x) = 0`, verificando **mudança de sinal** da concavidade.
2. Verificar também os **pontos de emenda** entre os trechos.
3. Se houver mais de um ponto de inflexão, escolher o de **coordenada x mais próxima do eixo y**.
4. Para os cantos **B** e **D**, aplicar a reflexão vertical: `(x, y) → (−x, y)`.

> 📝 Os cálculos passo a seguir (derivadas, critério do eixo y e reflexões) serão documentados em [`docs/pontos-de-inflexao.md`](docs/pontos-de-inflexao.md).

---

## 🎯 4. Pontos de Controle

As funções delimitadoras devem passar pelos pontos abaixo. Para cada ponto, basta que **uma** das funções passe por ele.

| Ponto | Coordenadas (x, y) |
| :---: | :---: |
| X1 | (−3,684; 0,947) |
| X2 | (2,417; −2,638) |
| X3 | (−1,362; 0,214) |
| X4 | (1,584; 2,663) |
| X5 | (−2,771; −1,542) |
| X6 | (2,836; 1,074) |
| X7 | (−2,116; 3,692) |
| X8 | (−0,238; −2,864) |

---

## 🔢 5. Encaixe Aritmético

Após a delimitação das peças, entra o desafio aritmético:

- Na **moldura**, são distribuídos números.
- As peças que tocam a moldura trazem, na face correspondente, uma **operação cujo resultado é o número da moldura**.
- Entre **peças vizinhas**, a face em comum deve conter operações **equivalentes** (mesmo resultado).

**Exemplo:** uma peça com `3 × 8` encaixa em uma vizinha com `4 × 6`, pois ambas resultam em **24**.

Todas as operações e valores devem estar **visíveis no GeoGebra**.

---

## 🗓️ 6. Cronograma e Avaliação (10 pontos)

| Marco | Período | Entregas | Pontos |
| :---: | :---: | :--- | :---: |
| **1** | Semana de 26/10 | Pontos de inflexão P<sub>A</sub> a P<sub>D</sub> (derivadas passo a passo, critério do eixo y, reflexões em B e D) | 1,5 |
| **1** | Semana de 26/10 | Funções que passam por pelo menos 3 dos pontos X, com equações e demonstração no GeoGebra | 1,5 |
| **2** | Semana de 09/11 | Modelagem completa das funções delimitadoras (quantidades e tipos corretos, passando pelos pontos) | 3,5 |
| **2** | Semana de 09/11 | Mapeamento das operações nas laterais das 16 peças, com equivalência entre vizinhas e moldura | 1,5 |
| **3** | Semana de 23/11 (prazo: **27/11, 23:59**) | Link final do GeoGebra no Canvas: 16 peças com domínios restritos e operações visíveis | 2,0 |

---

## 📁 7. Estrutura do Repositório

```text
.
├── README.md
├── docs/
│   ├── enunciado.pdf              # Diretrizes do projeto
│   ├── pontos-de-inflexao.md      # Marco 1: cálculos passo a passo
│   ├── funcoes-delimitadoras.md   # Marcos 1 e 2: equações e interpolações
│   └── mapeamento-operacoes.md    # Marco 2: esquema das 16 peças
├── geogebra/
│   └── tabuleiro.ggb              # Arquivo do GeoGebra
└── LICENSE
```

> Ajuste a estrutura conforme os arquivos que o grupo adicionar.

---

## 🔗 8. Produto Final

- **Link do GeoGebra:** _a ser adicionado após a conclusão (Marco 3)_

---

## 🗺️ Roadmap

- [ ] **Marco 1:** calcular P<sub>A</sub>, P<sub>B</sub>, P<sub>C</sub> e P<sub>D</sub>
- [ ] **Marco 1:** definir funções que passem por pelo menos 3 pontos X e validar no GeoGebra
- [ ] **Marco 2:** finalizar a interpolação de todos os pontos X1 a X8
- [ ] **Marco 2:** completar as 14 funções delimitadoras (2 lineares, 2 exponenciais, 2 trigonométricas, 2 logarítmicas, 2 racionais, 4 polinomiais)
- [ ] **Marco 2:** mapear as operações aritméticas das 16 peças e da moldura
- [ ] **Marco 3:** montar o tabuleiro final com domínios restritos e operações visíveis
- [ ] **Marco 3:** submeter o link do GeoGebra no Canvas

---

## 👥 Integrantes do Grupo 2

| Nome | RA | Contribuição |
| :--- | :---: | :--- |
| João Paulo Nunes Andrade | 25002703 |
| João Vitor Mariotto Cerqueira Leite  | 26006781 |
| Gustavo Antoniazzi Gouvea Santos | 25007671 |
| Giovana Dutra | 26021758 |



---

## 📚 Referências

1. **Enunciado:** Projeto Quebra-Cabeça de Matemática, Cálculo I Prática, PUC-Campinas (2026). Prof. Alexandre Monteiro.
2. **GeoGebra:** [geogebra.org](https://www.geogebra.org/)
3. **Stewart, J.** *Cálculo.* Cengage Learning. (Referência sugerida para derivadas, concavidade e pontos de inflexão.)

---

## 📜 Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 📬 Contato

<div align="center">
  <!-- Adicione os links do grupo -->
  <a href="mailto:email@exemplo.com"><img src="https://img.shields.io/badge/-Email-%23333?style=for-the-badge&logo=gmail&logoColor=white"></a>
  <a href="https://www.linkedin.com/in/seu-perfil" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a>
</div>
