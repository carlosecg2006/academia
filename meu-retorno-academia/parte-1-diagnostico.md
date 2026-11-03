# Parte 1 — Diagnóstico dos arquivos

## 1.1 O que foi encontrado

**O repositório `academia` estava vazio** (nenhum arquivo e nenhum commit). Todo o material de treino chegou como **anexo da conversa**: 7 arquivos de texto e 3 imagens. Guardei cópias idênticas em [`material-original/`](material-original/) e conferi cada uma com *checksum* MD5, uma "impressão digital" do arquivo que prova que a cópia é idêntica byte a byte.

| # | Arquivo (em `material-original/`) | Tipo | O que contém |
|---|---|---|---|
| 1 | `academia.txt` | Texto | O **plano de readaptação de 8 semanas** (tabela de volume), o **ciclo** das semanas 9 em diante e os **suplementos** que seu amigo usa |
| 2 | `tutorial_peito.txt` | Texto | Dicas de execução de 6 exercícios de peito |
| 3 | `tutorial_costas.txt` | Texto | Dicas de execução de 6 exercícios de costas |
| 4 | `tutorial_quadriceps__panturilha.txt` | Texto | Dicas de execução de 6 exercícios de pernas (frente da coxa) e panturrilha |
| 5 | `tutorial_ombro__trapezio.txt` | Texto | Dicas de execução de 5 exercícios de ombro e trapézio |
| 6 | `tutorial_braco__antebraco.txt` | Texto | Dicas de execução de 8 exercícios de braço e antebraço, mais **1 bloco sem título** (ver 1.6) |
| 7 | `tutorial_gluteo__posterior__abdomen.txt` | Texto | Dicas de execução de 6 exercícios de glúteo, parte de trás da coxa e abdômen |
| 8 | `hevy_rotina_deload.jpg` | Imagem (print do app Hevy) | Pasta **"Deload"**: 6 treinos com exercícios e nº de séries |
| 9 | `hevy_rotina_treino_de_forca.jpg` | Imagem (print do app Hevy) | Pasta **"Treino de força"**: **idêntica ao Deload** (ver 1.6) |
| 10 | `hevy_rotina_treino_de_hipertrofia.jpg` | Imagem (print do app Hevy) | Pasta **"Treino de hipertrofia"**: 6 treinos com séries e, em alguns exercícios, repetições |

> **Hevy** é um aplicativo de celular para registrar treinos. As imagens são o "cartão de compartilhamento" das rotinas do seu amigo (usuário `juan_growth`).
> Os exercícios que aparecem no Hevy com **um círculo escuro e duas letras** (CP, RU, TF, TC, CI, RI, FD) são **exercícios personalizados** que seu amigo criou no app. Por isso eles **não têm desenho nem animação de demonstração** no Hevy.

## 1.2 A divisão dos treinos (ORIGINAL)

O treino é dividido em **6 sessões**, cada uma focada em uma região do corpo. As 3 imagens usam **a mesma divisão e os mesmos exercícios, na mesma ordem**:

| Sessão | Nome no Hevy | Nº de exercícios (sem contar o Spinning) |
|---|---|---|
| A | Peitoral | 6 |
| B | Costas | 6 |
| C | Quadriceps + panturilha | 6 |
| D | Ombros + trapezio | 5 |
| E | Braço + antebraço | 9 |
| F | Gluteo + posterior + abdominal | 6 |

Todas as sessões terminam com **Spinning (1 série)**, a bicicleta ergométrica de academia.

**Os arquivos não dizem em que dia da semana cada sessão acontece.** A imagem mostra as sessões em uma grade de 3 colunas. Lida linha por linha (como um texto), a ordem é A-B-C-D-E-F, que é a ordem usada aqui. Para recuperação muscular, essa ordem também é melhor que a leitura por colunas, que juntaria Quadríceps e Glúteo em dias seguidos. **Confirme com seu amigo** (Parte 9).

## 1.3 Tabela completa de exercícios, séries e repetições (ORIGINAL)

Legenda: **Deload** = imagem "Deload" (igual à "Treino de força"). **Hipertrofia** = imagem "Treino de hipertrofia". "—" = o arquivo não informa.
**Carga, descanso e repetições do Deload/Força não aparecem em nenhum arquivo.**

### Sessão A — Peitoral
| Ordem | Exercício (nome exato no Hevy) | Deload | Hipertrofia (séries · reps) |
|---|---|---|---|
| 1 | Incline Chest Press (Machine) | 2 | 4 · — |
| 2 | Low Cable Fly Crossovers | 2 | 4 · — |
| 3 | Chest Press (Machine) | 2 | 4 · — |
| 4 | Crucifixo Polia Média (Maquina) *(personalizado: CP)* | 2 | 4 · 8 |
| 5 | Decline Bench Press (Machine) | 2 | 4 · — |
| 6 | Cable Fly Crossovers | 2 | 4 · 5–12 |
| 7 | Spinning | 1 | 1 |

### Sessão B — Costas
| Ordem | Exercício | Deload | Hipertrofia |
|---|---|---|---|
| 1 | Lat Pulldown (Cable) | 2 | 4 · 10–12 |
| 2 | Iso-Lateral High Row (Machine) | 2 | 4 · — |
| 3 | Remada Unilateral Na Polia *(personalizado: RU)* | 2 | 4 · 12 |
| 4 | Deadlift (Barbell) | 2 | 4 · 6 |
| 5 | Bent Over Row (Barbell) | 2 | 4 · 10 |
| 6 | Iso-Lateral Row (Machine) | 2 | 4 · 10 |
| 7 | Spinning | 1 | 1 |

### Sessão C — Quadríceps + panturrilha
| Ordem | Exercício | Deload | Hipertrofia |
|---|---|---|---|
| 1 | Hack Squat (Machine) | 4 | 8 · 6 |
| 2 | Leg Press (Machine) | 4 | 8 · 6–12 |
| 3 | Leg Extension (Machine) | 4 | 8 · 10–12 |
| 4 | Hip Adduction (Machine) | 3 | 6 · 6 |
| 5 | **Single Leg** Standing Calf Raise (Machine) no Deload / Standing Calf Raise (Machine) na Hipertrofia | 3 | 6 · 8–12 |
| 6 | Seated Calf Raise | 3 | 6 · 7 |
| 7 | Spinning | 1 | 1 |

### Sessão D — Ombros + trapézio
| Ordem | Exercício | Deload | Hipertrofia |
|---|---|---|---|
| 1 | Lateral Raise (Dumbbell) | 6 | 12 · 8 |
| 2 | Overhead Press (Dumbbell) | 3 | 6 · 6 |
| 3 | Crucifixo Inverso no Fly *(personalizado: CI)* | 3 | 6 · — |
| 4 | Upright Row (Cable) | 3 | 6 · — |
| 5 | Shrug (Cable) | 3 | 6 · — |
| 6 | Spinning | 1 | 1 |

### Sessão E — Braço + antebraço
| Ordem | Exercício | Deload | Hipertrofia |
|---|---|---|---|
| 1 | Triceps Rope Pushdown | 2 | 4 · — |
| 2 | triceps frances corda *(personalizado: TF)* | 2 | 4 · — |
| 3 | triceps coice com corda *(personalizado: TC)* | 2 | 4 · — |
| 4 | Bicep Curl (Dumbbell) | 2 | 4 · — |
| 5 | Single Arm Curl (Cable) | 2 | 4 · — |
| 6 | Preacher Curl (Machine) | 2 | 4 · — |
| 7 | rosca invertida polia *(personalizado: RI)* | 2 | 4 · — |
| 8 | Flexão De Punho Na Polia *(personalizado: FD)* | 2 | 4 · — |
| 9 | Wrist Roller | 2 | 4 · — |
| 10 | Spinning | 1 | 1 |

### Sessão F — Glúteo + posterior + abdominal
| Ordem | Exercício | Deload | Hipertrofia |
|---|---|---|---|
| 1 | Hip Thrust | 3 | 6 · — |
| 2 | Rear Kick (Machine) | 3 | 6 · — |
| 3 | Hip Abduction (Machine) | 3 | 6 · — |
| 4 | Seated Leg Curl (Machine) | 3 | 6 · — |
| 5 | Lying Leg Curl (Machine) | 3 | 6 · — |
| 6 | Crunch (Machine) | 3 | 3 · — |
| 7 | Spinning | 1 | 1 |

**Total de exercícios diferentes: 38 de musculação + Spinning = 39.** Todos têm guia na [Parte 4](parte-4-exercicios/README.md).

## 1.4 O plano de 8 semanas e o ciclo (ORIGINAL, de `academia.txt`)

Texto original (resumido apenas na formatação):

> **Fase de Readaptação — 8 Semanas.** Regra geral: cada bloco de 2 semanas repete o mesmo alvo de carga/volume. Só avance pro próximo bloco se os sinais de prontidão da semana estiverem OK. Se ainda estiver doendo muito ou sentindo desconforto articular, repita o bloco inteiro antes de avançar.

| Semana | % do volume | Base 24 → | Base 12 → | Base 6 → | Base 3 → |
|---|---|---|---|---|---|
| 1 | ~50% | 12 | 6 | 3 | 3 |
| 2 | ~60% | 14 | 7 | 4 | 3 |
| 3 | ~65% | 16 | 8 | 4 | 3 |
| 4 | ~75% | 18 | 9 | 4 | 3 |
| 5 | ~85% | 20 | 10 | 5 | 3 |
| 6 | ~90% | 22 | 11 | 5 | 3 |
| 7–8 | 100% | 24 | 12 | 6 | 3 |

> Na semana 8: Ciclo de transição (3) — Deload na semana 8.
> Na semana 9 em diante: Ciclo normal (1-2-1-2-3): (1) Hipertrofia, (2) Força, (3) Deload.

### O que isso significa, em linguagem simples
- "**Volume**" aqui é **a quantidade de séries**. A "ficha completa" (100%) corresponde ao **Treino de hipertrofia**.
- Os números 24/12/6/3 são os "tamanhos" das fichas completas. Conferindo com a imagem de Hipertrofia:
  - **Base 24** = total do **grupo inteiro** em Peitoral (6 exercícios × 4), Costas (6 × 4) e nos 3 primeiros de Quadríceps (Hack, Leg Press e Extensora: 3 × 8).
  - **Base 12** = Elevação lateral (12 séries sozinha) e, **por interpretação minha**, cada trio de braço (tríceps: 3 × 4; bíceps: 3 × 4; antebraço: 3 × 4).
  - **Base 6** = cada exercício com 6 séries (adutora, panturrilhas, ombros, glúteo, flexoras).
  - **Base 3** = Abdominal na máquina.
- **A semana 1 (~50%) bate exatamente com a imagem "Deload".** Conferi grupo por grupo: peito 12 séries (6 × 2), costas 12, quadríceps 12 (3 × 4), lateral 6, cada base 6 → 3, braços 2 por exercício, abdominal 3. **Então, na semana 1, você usa exatamente a rotina "Deload" do Hevy.**
- "**Deload**" (do inglês, "descarregar") é uma semana mais leve, planejada para o corpo se recuperar.
- "**Ciclo 1-2-1-2-3**" = depois da readaptação, as semanas se alternam assim: Hipertrofia → Força → Hipertrofia → Força → Deload, e o ciclo recomeça.

## 1.5 Informações que **não existem** nos arquivos

Não inventei nenhuma destas. Onde precisei de um ponto de partida, fiz uma **sugestão complementar separada e marcada**.

| Informação | Situação |
|---|---|
| Cargas (peso) | **Nenhuma carga em nenhum arquivo.** Não há "cargas antigas" a reaproveitar. Você vai descobrir as suas (método na [Parte 2](parte-2-planejamento-semanal.md#25-como-escolher-a-carga-sem-tabela-do-amigo-complementar)). |
| Descanso entre séries | **Não informado.** Sugestão complementar na Parte 2. |
| Repetições do Deload/Força | **Não informadas.** Repetições só aparecem em 15 exercícios da Hipertrofia. |
| Dias da semana de cada sessão | **Não informados.** Ordem A–F por leitura da imagem (ver 1.2). |
| Duração ou intensidade do Spinning | **Não informadas** ("1 série"). |
| "Sinais de prontidão" da semana | **Citados, mas não definidos.** |
| Como distribuir as séries das semanas 2 a 7 entre os exercícios | **Não informado** (ex.: como dividir 14 séries entre 6 exercícios de peito). |
| Técnicas especiais (drop-set, bi-set etc.) | **Nenhuma.** Há apenas detalhes de execução (torção do tronco nas remadas, queixo no peito no encolhimento, 3 ângulos no abdominal, alternância no rolo de punho). |

## 1.6 Contradições e problemas encontrados

Lista resumida (a explicação completa está na [Parte 9](parte-9-duvidas-e-atencao.md)):

1. **"Treino de força" = "Deload"**: imagens idênticas pixel a pixel, exceto o título.
2. **Semana 8**: a tabela diz "Semanas 7–8 = 100%", mas logo abaixo diz "Deload na semana 8".
3. **Panturrilha em pé**: "**Single Leg** Standing Calf Raise" (uma perna) no Deload/Força, "Standing Calf Raise" (duas pernas) na Hipertrofia. O tutorial descreve a versão com as duas pernas.
4. **Hip Thrust**: o tutorial diz "(Machine)"; o Hevy diz só "Hip Thrust", e o desenho sugere a versão com barra e banco.
5. **Crucifixo Polia Média**: o nome diz "(Máquina/Machine)", mas o texto descreve **polias/roldanas** (cabo).
6. **Rosca invertida polia**: **não tem tutorial**. No lugar dele há um **bloco sem título** que repete quase todo o texto da Rosca Scott (Preacher Curl).
7. **Flexão de punho na polia**: o tutorial descreve **6 séries** (2 + 2 + 2); o Hevy diz **4** (Hipertrofia) e **2** (Deload). A polia da terceira variação não é informada.
8. **Wrist Roller**: o tutorial descreve **6 séries** (3 + 3); o Hevy diz **4** e **2**. A palavra "Execução:" também aparece duplicada (erro de digitação).
9. **Hipertrofia não cabe em 1 hora**: Braço = 36 séries + Spinning; Ombros = 36 + Spinning. Ver Parte 2.
10. **Suplementos** (creatina e multivitamínico): são do **seu amigo**, não são prescrição para você. Ver Parte 6.
11. Pequenas diferenças de grafia: "Maquina"/"Machine", "panturilha" (o certo é "panturrilha"), "usa mão" (provavelmente "sua mão").

## 1.7 O que é ORIGINAL e o que é COMPLEMENTAR neste material

| Tipo | Onde aparece | Pode mudar? |
|---|---|---|
| **ORIGINAL** | Exercícios, ordem, séries, repetições, divisão, plano de 8 semanas, ciclo e textos dos tutoriais | **Não.** Só seu amigo (ou um profissional que assuma seu treino) deveria mudar |
| **COMPLEMENTAR** | Passo a passo detalhado, sensações, erros comuns, respiração, horários, descanso sugerido, método de carga, alimentação, sistema de pendências | É orientação de apoio, que pode ser ajustada à sua realidade |
| **RECOMENDAÇÃO DE SEGURANÇA** | Sempre em destaque, separada | É sugestão justificada; a decisão final é sua, de preferência com um profissional |
