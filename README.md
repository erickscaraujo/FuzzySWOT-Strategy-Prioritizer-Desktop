# FuzzySWOT Strategy Prioritizer - Desktop

Aplicação desktop para priorização estratégica com lógica fuzzy e matriz TOWS, desenvolvida em Rust com Tauri.

## Autores

- **David de Oliveira Costa** - Autor Original
  - Doutorando em Engenharia de Computação, 2026
  - Desenvolvedor da metodologia FuzzySWOT e aplicação original em Python/Streamlit

- **Erick de S.C. Araújo** - Transcrição para Rust
  - Conversão e implementação desktop com Tauri
  - Responsável pela transcrição da aplicação para Rust/Tauri e desenvolvimento do ícone

## Versão

0.1.0

## Metodologia

Baseado na modelagem matemática apresentada no XLVI Encontro Nacional de Engenharia de Produção (ENEGEP 2026).

### Modelagem Matemática

1. **Construção da matriz TOWS fuzzy**
   - Fatores internos (Forças/Fraquezas) × Fatores externos (Oportunidades/Ameaças)

2. **Consolidação dos julgamentos**
   - Média ponderada dos pesos dos avaliadores para cada relação fuzzy

3. **Priorização dos fatores**
   - Cálculo da prioridade fuzzy de cada fator interno

4. **Geração das estratégias TOWS**
   - SO (Ofensiva), ST (Defensiva), WO (Melhoria), WT (Sobrevivência)

5. **Perfil estratégico por quadrante**
   - Intensidade total e participação percentual de cada quadrante

6. **Consenso entre avaliadores**
   - Convergência por média, desvio padrão e amplitude

## Tecnologias

- 🦀 **Rust** - Linguagem de programação
- 📦 **Tauri 1.x** - Framework para aplicações desktop
- 🧮 **Lógica Fuzzy** - Sistema de priorização
- 📊 **Matriz TOWS** - Análise estratégica

## Funcionalidades

### Análise SWOT Fuzzy

- Cadastro de projetos com dados organizacionais
- Definição de fatores SWOT (Forças, Fraquezas, Oportunidades, Ameaças)
- Cadastro de avaliadores com pesos hierárquicos automáticos
- Preenchimento de matrizes de julgamento fuzzy (escala 0-1)
- Consolidação dos julgamentos com média ponderada
- Cálculo de consenso entre avaliadores

### Estratégias TOWS

- Geração automática de estratégias por quadrante:
  - **SO**: Ofensiva (Forças × Oportunidades)
  - **ST**: Defensiva (Forças × Ameaças)
  - **WO**: Melhoria (Fraquezas × Oportunidades)
  - **WT**: Sobrevivência (Fraquezas × Ameaças)
- Perfil estratégico com participação percentual
- Radar estratégico visual

### Exportação

- Geração de relatório consultivo
- Dados do projeto e resultados consolidados

## Escala Fuzzy

| Valor | Label |
|-------|-------|
| 0.0 | Falso / nenhuma relação |
| 0.1 | Quase falso |
| 0.2 | Bastante falso |
| 0.3 | Algo falso |
| 0.4 | Mais falso que verdadeiro |
| 0.5 | Tão falso quanto verdadeiro |
| 0.6 | Mais verdadeiro que falso |
| 0.7 | Algo verdadeiro |
| 0.8 | Bastante verdadeiro |
| 0.9 | Quase verdadeiro |
| 1.0 | Verdadeiro / relação máxima |

## Pesos Hierárquicos

| Função | Peso |
|--------|------|
| Presidente do Conselho | 1.00 |
| CEO / Presidente Executivo | 0.90 |
| Diretor | 0.80 |
| Gerente | 0.70 |
| Coordenador / Supervisor | 0.60 |
| Especialista / Analista | 0.50 |
| Consultor externo | 0.50 |
| Outros | 0.40 |

## Licença

MIT License

## Agradecimentos

- David de Oliveira Costa pela autorização da transcrição e pela metodologia original.
[Perfil academico](https://orcid.org/0000-0002-6138-7451)
[Perfil profissional](https://www.linkedin.com/in/daviddeoliveiracosta)
