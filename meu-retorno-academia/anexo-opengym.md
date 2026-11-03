# Anexo — openGym: o que é e como pode ajudar

Repositório analisado: <https://github.com/DuarteSantos8/openGym> (README, CLAUDE.md, `docs/DATA_IMPORTS.md` e a lista de idiomas e o catálogo de exercícios).
**Nada foi instalado nem executado, e nenhum arquivo do seu projeto foi alterado por causa dele.** Só li a documentação e consultei o catálogo de exercícios.

## 1. A natureza real do openGym

| Pergunta | Resposta |
|---|---|
| É uma "skill" de personal trainer para o Claude? | **Não.** É um **aplicativo** de registro de treinos (celular, relógio e web). |
| O que é o `CLAUDE.md` dele? | São **instruções para programadores** que usam o Claude Code para **desenvolver o próprio aplicativo** (estrutura do código, testes, regras de contribuição). **Não é prescrição de treino** e não ensina exercícios. |
| Ele traz um treino pronto? | Tem **modelos genéricos** (Push/Pull/Legs, Upper/Lower, Full Body, 5×5). **Nenhum deles é o treino do seu amigo.** Não use esses modelos no lugar do seu. |
| É pago? | **Gratuito e de código aberto** (licença AGPL-3.0), sem anúncios, sem assinatura. |
| Em português? | **Sim.** O app tem tradução para **português do Brasil** (conferi os arquivos `frontend/src/locales/pt-BR.js` e `catalogue/i18n/pt-BR.json` no repositório). |
| Onde conseguir? | **iPhone/iPad (App Store)**, com app de **Apple Watch**; **Android**: arquivo **APK** baixado do GitHub ou do site opengym.ch (~315 MB na versão padrão; a Google Play ainda está "em breve"). Também pode ser **instalado num servidor próprio** com Docker, mas **para você isso não é necessário**: o app do celular funciona **sozinho, sem servidor e sem conta**. |

## 2. Funcionalidades que ajudam na sua situação

| Sua necessidade | O que o openGym oferece | Ajuda? |
|---|---|---|
| **Organizar os exercícios** | Criar os seus próprios planos com os exercícios e a ordem que você quiser | ✅ Monte as 6 sessões A–F exatamente como na ficha do seu amigo |
| **Ver demonstrações** | Catálogo com **mais de 5.600 exercícios com animação**, busca por nome e por **mapa do corpo** | ✅ Indiquei o nome do catálogo em cada guia (seção H) |
| **Exercícios personalizados** (CP, RU, TF, TC, CI, RI, FD) | Criar exercício próprio com **foto, GIF ou vídeo curto** | ✅ Você pode **filmar o professor** demonstrando e guardar ali (com a autorização dele) |
| **Registrar séries, repetições e carga** | Registro por série; o treino guiado **preenche a carga da última vez** | ✅ |
| **Descanso** | **Cronômetro de descanso** por exercício (até 15 min), com alerta | ✅ Configure ~2 min nos exercícios grandes e ~1–1,5 min nos pequenos |
| **Spinning** | Exercícios **por tempo** e **cardio** (tempo e velocidade) | ✅ |
| **Histórico** | Editar treinos passados, registrar treinos de papel | ✅ |
| **Evolução** | Gráficos de **1RM estimado** (estimativa da carga máxima), **recordes pessoais**, **mapa de músculos** treinados/não treinados | ✅ Útil a partir de algumas semanas |
| **Rotina semanal** | Plano **por dia da semana** **ou por "rotação" (A, B, C…)**, em que **a próxima sessão é a próxima não feita** | ✅✅ A **rotação** é exatamente o **sistema de fila** da Parte 2 |
| **Mover sessões** | Mover uma sessão para outro dia sem mudar o plano | ✅ |
| **Regras de progressão** | Linear, dupla, tripla… (o app sugere quando aumentar) | ⚠️ **Use com cuidado.** Não deixe o app mudar a prescrição do seu amigo. Use, no máximo, como lembrete |
| **"AI coach"** (treinador por IA) | Opcional, **desligado por padrão**; sugere rotinas e mudanças (com sua aprovação) | ⛔ **Não recomendo para você agora.** Ele propõe mudanças de treino, e a regra do projeto é preservar a ficha original |
| **Importar do Hevy** | **Histórico** por arquivo CSV exportado do Hevy; **rotinas** só pela **chave de API do Hevy**, que exige **Hevy Pro** (pago) | ⚠️ Ver a seção 3 |
| **Exportar** | JSON e CSV | ✅ Útil para guardar cópias dos seus registros |

**O que ele NÃO faz:** não ensina **como regular os aparelhos da sua academia**, não confere sua postura e não sabe do seu horário nem do remédio da sua cachorra. As animações **mostram o desenho do movimento**; **os guias da Parte 4 continuam sendo a sua explicação principal**.

## 3. Como o openGym poderia ser usado neste projeto (sem instalar nada agora)

### Opção 1: só o app no celular (RECOMENDADA, se quiser usar)
1. Instale o app (App Store ou APK do Android) **quando você decidir**.
2. Escolha **português do Brasil**.
3. Crie **6 planos** (A a F) **à mão**, copiando a [tabela da Parte 1](parte-1-diagnostico.md#13-tabela-completa-de-exercícios-séries-e-repetições-original), com as séries da **semana do plano** em que você está (Parte 2, seção 2.3).
4. Use o modo **rotação**, não o modo "dia fixo", para combinar com o sistema de fila.
5. Configure o **descanso** de cada exercício.
6. Para os 7 exercícios personalizados, crie exercícios próprios com os mesmos nomes da ficha.
7. **Desligado:** AI coach e regras automáticas de progressão.

### Opção 2: usar o Hevy (o mesmo app do seu amigo)
Como seu amigo já tem as rotinas no **Hevy**, pode ser **mais simples** pedir que ele **compartilhe as rotinas** com você e salvá-las no seu Hevy. Assim você fica com o **mesmo nome e a mesma ordem** dos exercícios, sem digitar nada. ⚠️ Não verifiquei nesta sessão os detalhes atuais de compartilhamento do Hevy; confira no app. Se depois quiser migrar para o openGym, o histórico pode ser importado por CSV.

### Opção 3: integrar com este repositório (apresentada separadamente; não executada)
É possível **sem mexer em código nenhum**:
- de tempos em tempos, **exportar seus treinos do app em CSV** e salvar numa pasta nova, por exemplo `meu-retorno-academia/registros/`;
- eu (Claude) posso então **ler esse CSV** para atualizar pendências, conferir sua progressão e responder dúvidas com base no que você realmente fez.

Isso **não instala nada**, **não executa scripts** e **não altera** os arquivos originais. **Só faço isso se você pedir.**

**O que eu NÃO recomendo:** clonar o openGym dentro deste repositório ou instalar o servidor com Docker. É um projeto grande, voltado para quem quer hospedar o próprio servidor, e **não traz benefício** para o seu objetivo.

## 4. Cuidados

- **APK no Android:** instalar um APK fora da loja exige permitir "fontes desconhecidas". Baixe **somente** do GitHub oficial do projeto ou do site do projeto, e confira o arquivo `.sha256` (uma "impressão digital" do arquivo) se souber como. Se não se sentir seguro, prefira o Hevy (Opção 2), que está nas lojas oficiais.
- **Imagens dos exercícios:** as animações têm **licença própria** (Gym visual) e só podem ser usadas **dentro do app**. Não copiei nenhuma para este material.
- **Backup:** se usar só o celular, **exporte** seus dados de vez em quando.
