# Stack de ferramentas e IA do projeto

Referência única do stack de ferramentas do projeto: harnesses de código, skills, fluxo no GitHub, artigo científico, documentação, design, frontend, backend, catálogos de modelos gratuitos, agregadores, gateways, provedores e modelos locais.

**Última verificação de links:** 24/10/2026.
**Escopo:** documentação. Este arquivo descreve ferramentas; não configura nenhuma delas.

## Sumário

1. [Visão geral](#1-visão-geral)
2. [Diretório oficial de links](#2-diretório-oficial-de-links)
3. [Harnesses e agentes de programação](#3-harnesses-e-agentes-de-programação)
4. [Contexto do agente](#4-contexto-do-agente)
5. [GitHub e fluxo de desenvolvimento](#5-github-e-fluxo-de-desenvolvimento)
6. [Artigo científico e pesquisa](#6-artigo-científico-e-pesquisa)
7. [Documentação](#7-documentação)
8. [Design e UX/UI](#8-design-e-uxui)
9. [Frontend](#9-frontend)
10. [Backend](#10-backend)
11. [Descoberta de APIs e modelos gratuitos](#11-descoberta-de-apis-e-modelos-gratuitos)
12. [Proxies e agregadores de free tiers](#12-proxies-e-agregadores-de-free-tiers)
13. [Gateways de LLM](#13-gateways-de-llm)
14. [Provedores de inferência](#14-provedores-de-inferência)
15. [Modelos locais](#15-modelos-locais)
16. [Estratégia de fallback](#16-estratégia-de-fallback)
17. [Recomendação por área](#17-recomendação-por-área)
18. [Instalar skills com `npx skills`](#18-instalar-skills-com-npx-skills)
19. [Stack mínima recomendada](#19-stack-mínima-recomendada)
20. [Ferramentas alternativas](#20-ferramentas-alternativas)
21. [Ferramentas não priorizadas](#21-ferramentas-não-priorizadas)
22. [Critérios para adicionar novas ferramentas](#22-critérios-para-adicionar-novas-ferramentas)
23. [Links rápidos](#23-links-rápidos)

## 1. Visão geral

As ferramentas do projeto se dividem em camadas com papéis diferentes. Confundir essas camadas é a origem mais comum de escolha errada:

| Camada | O que faz | Exemplos no projeto |
|---|---|---|
| Harness | conduz a conversa, edita arquivos, executa comandos e chama ferramentas | OMP, OpenCode, Freebuff, Kilo Code |
| Contexto do agente | dão regra, procedimento, ferramenta e índice ao agente | `.agents/skills/`, `AGENTS.md`, MCP, `docs/codebase/` |
| Fluxo de trabalho | organiza demanda, revisão e entrega | GitHub, Issues, Pull Requests, Projects |
| Produção de conteúdo | pesquisa, escrita, design | Elicit, Oleafly, Pen.dev, Figma |
| Catálogo | descobre o que existe e o que é gratuito | FreeTokens.fyi, FreeLLM.net |
| Agregador | reúne várias contas e chaves próprias em um ponto | FreeLLMAPI |
| Gateway | padroniza endpoint, roteia, aplica fallback e mede uso | LiteLLM, Portkey |
| Provedor | executa a inferência | Gemini, Groq, Z.ai, NVIDIA NIM, OpenRouter |
| Local | executa o modelo na própria máquina | Ollama |

Três regras valem para todo o documento:

- **Catálogo não é provedor.** Um site que lista modelos gratuitos não serve inferência.
- **Gateway não é fonte de modelos gratuitos.** Ele organiza o acesso aos provedores que já existem.
- **Coding agent não é API para aplicação.** Freebuff e Kilo Code entregam compute subsidiado para programar, não um endpoint de produção.

Limites, modelos gratuitos e promoções mudam sem aviso. Nenhum número deste documento deve ser tratado como garantia permanente; a verificação é feita nos catálogos da seção 11 antes de depender de uma oferta.

## 2. Diretório oficial de links

Esta é a fonte única dos links. As seções seguintes descrevem papel e classificação, sem repetir URLs. Quando não existe site, documentação ou repositório público oficial confirmado, o campo diz isso explicitamente.

### Harnesses e agentes de programação

| Ferramenta | Site | Documentação | Repositório oficial |
|---|---|---|---|
| OMP (Oh My Pi) | https://omp.sh/ | https://omp.sh/docs | https://github.com/can1357/oh-my-pi |
| OpenCode | https://opencode.ai/ | https://opencode.ai/docs/ | https://github.com/sst/opencode |
| Freebuff | https://freebuff.com/ | Documentação pública dedicada: não encontrada/confirmada (o repositório e o blog de lançamento descrevem o uso) | https://github.com/CodebuffAI/freebuff |
| Kilo Code | https://kilo.ai/ | https://kilo.ai/docs | https://github.com/Kilo-Org/kilocode |
| Codex | https://openai.com/codex/ | https://platform.openai.com/docs/codex | https://github.com/openai/codex |
| Claude Code | https://claude.com/product/claude-code | https://code.claude.com/docs/en/overview | https://github.com/anthropics/claude-code (issues e documentação; o código não é aberto) |

### Skills

| Ferramenta | Site | Documentação | Repositório oficial |
|---|---|---|---|
| `npx skills` (CLI) | https://skills.sh/ | https://github.com/vercel-labs/skills/tree/main/docs | https://github.com/vercel-labs/skills |

A especificação aberta seguida pelas skills, comum aos agentes, está em https://agentskills.io.

### Contexto do agente, MCP e disciplina de código

| Ferramenta | Site | Documentação | Repositório oficial |
|---|---|---|---|
| MCP (Model Context Protocol) | https://modelcontextprotocol.io/ | https://modelcontextprotocol.io/docs | https://github.com/modelcontextprotocol/modelcontextprotocol |
| graphify | Site dedicado: não encontrado/confirmado (o repositório é a referência publicada) | https://github.com/Graphify-Labs/graphify#readme | https://github.com/Graphify-Labs/graphify |
| Ponytail | https://ponytail.dev/ | https://github.com/DietrichGebert/ponytail/blob/main/INSTALL.md e o README do repositório | https://github.com/DietrichGebert/ponytail |

Configuração de MCP por harness: OMP em https://omp.sh/docs/mcp e OpenCode em https://opencode.ai/docs/mcp-servers/.

### Artigo científico

| Ferramenta | Site | Documentação | Repositório oficial |
|---|---|---|---|
| Elicit | https://elicit.com/ | https://docs.elicit.com/ (API) e https://support.elicit.com/ (central de ajuda) | Repositório público oficial: não encontrado/confirmado |
| Oleafly | https://oleafly.com/ | https://oleafly.com/docs | https://github.com/Oleafly/Oleafly |
| OpenPrism | Demonstração pública: https://openprism.vercel.app/ | Repositório (README e guia de instalação) | https://github.com/OpenDCAI/OpenPrism |

### Design

| Ferramenta | Site | Documentação | Repositório oficial |
|---|---|---|---|
| Pen.dev | https://pen.dev/ | https://docs.pen.dev/ | Repositório público oficial: não encontrado/confirmado |
| Figma | https://www.figma.com/ | https://help.figma.com/ | Repositório público oficial: não encontrado/confirmado |
| Starry | https://starry.design/ | https://app.starry.design/docs | Repositório público oficial: não encontrado/confirmado |
| Doop | https://doop.design/ | Repositório (README e guia de uso) | https://github.com/kgoedecke/doop |
| Paper | https://paper.design/ | https://paper.design/docs | Repositório público oficial: não encontrado/confirmado |
| OpenPencil | https://openpencil.dev/ | https://openpencil.dev/getting-started | https://github.com/open-pencil/open-pencil |
| Penpot | https://penpot.app/ | https://help.penpot.app/ | https://github.com/penpot/penpot |

### Catálogos e agregadores de free tiers

| Ferramenta | Site | Documentação | Repositório oficial |
|---|---|---|---|
| FreeTokens.fyi | https://freetokens.fyi/ | Documentação dedicada: não encontrada/confirmada (o próprio site lista os modelos e a validade) | Repositório público oficial: não encontrado/confirmado |
| FreeLLM.net | https://freellm.net/ | Gerador de configuração: https://freellm.net/config/ | Repositório relacionado: https://github.com/open-free-llm-api/awesome-freellm-apis |
| FreeInference.dev | https://freeinference.dev/ | Repositório (README) | https://github.com/surendranb/free-inference |
| Free LLM API Resources | Repositório | Repositório (README) | https://github.com/raullenchai/free-llm-api-resources |
| FreeLLMAPI | Repositório | Repositório (README) | https://github.com/OliverMoooi/freellmapi |

### Gateways

| Ferramenta | Site | Documentação | Repositório oficial |
|---|---|---|---|
| LiteLLM | https://www.litellm.ai/ | https://docs.litellm.ai/ | https://github.com/BerriAI/litellm |
| Portkey | https://portkey.ai/ | https://portkey.ai/docs | https://github.com/Portkey-AI/gateway |
| Vercel AI Gateway | https://vercel.com/ai-gateway | https://vercel.com/docs/ai-gateway | Repositório relacionado (AI SDK): https://github.com/vercel/ai |
| Cloudflare AI Gateway | https://developers.cloudflare.com/ai-gateway/ | https://developers.cloudflare.com/ai-gateway/ | Repositório público oficial: não encontrado/confirmado |

### Provedores de inferência e modelos locais

| Ferramenta | Site | Documentação | Repositório oficial |
|---|---|---|---|
| Gemini API | https://ai.google.dev/ | https://ai.google.dev/gemini-api/docs | Repositório público oficial do provedor: não encontrado/confirmado |
| Groq | https://console.groq.com/ | https://console.groq.com/docs | Repositório público oficial do provedor: não encontrado/confirmado |
| Z.ai (GLM) | https://z.ai/ | https://docs.z.ai/ | Repositório público oficial do provedor: não encontrado/confirmado |
| NVIDIA NIM | https://build.nvidia.com/ | https://docs.nvidia.com/nim/ | Repositório público oficial do provedor: não encontrado/confirmado |
| Cloudflare Workers AI | https://developers.cloudflare.com/workers-ai/ | https://developers.cloudflare.com/workers-ai/ | Repositório público oficial do provedor: não encontrado/confirmado |
| OpenRouter | https://openrouter.ai/ | https://openrouter.ai/docs | Repositório público oficial do provedor: não encontrado/confirmado |
| Ollama | https://ollama.com/ | https://docs.ollama.com/ | https://github.com/ollama/ollama |

## 3. Harnesses e agentes de programação

### OMP (Oh My Pi): harness principal

Harness principal do projeto para desenvolvimento diário. É um fork do Pi com foco em código, mantido em código aberto, e cobre:

- uso de skills e regras do repositório;
- MCPs e ferramentas externas;
- subagentes e sessões paralelas;
- frontend, backend e debugging;
- operações de GitHub;
- code review.

Toda decisão de fluxo do projeto pressupõe este harness. As skills da seção 4 foram escritas para ele.

### OpenCode: principal alternativa open source

Alternativa principal ao harness para quem não usa OMP, com o mesmo papel no fluxo. Recursos relevantes:

- BYOK, com a chave do próprio usuário;
- suporte a múltiplos provedores;
- modelos locais;
- catálogo próprio de modelos (OpenCode Zen);
- modelos gratuitos e promocionais;
- uso em terminal, desktop e web quando disponível.

### Freebuff: coding gratuito subsidiado

Classificação: **coding agent gratuito / fonte de compute subsidiado**. Não é API genérica para aplicações.

- franquia gratuita sustentada por anúncios;
- o conjunto de modelos disponíveis muda com o tempo;
- bom fallback para tarefas de código;
- não usar números fixos de horas ou créditos como garantia permanente.

### Kilo Code: coding alternativo com BYOK e Auto Free

Classificação: **coding agent alternativo com BYOK e Auto Free**.

- funciona em IDE, terminal e navegador;
- aceita chave própria de provedor;
- o modo Auto Free (`kilo-auto/free`) escolhe automaticamente entre os modelos gratuitos disponíveis no momento;
- a seleção automática depende do catálogo do dia, não de uma lista fixa.

### Codex e Claude Code

Ferramentas especializadas e complementares. Não são o harness principal do projeto e não substituem o fluxo descrito na seção 5.

- Codex: agente de código em terminal, com integração à conta OpenAI.
- Claude Code: agente de código em terminal, com integração à conta Anthropic.

## 4. Contexto do agente

O agente decide e escreve com o que estiver no contexto dele. Quatro camadas fornecem esse contexto, e cada uma tem um dono diferente:

| Camada | O que fornece | Onde vive |
|---|---|---|
| Regras do repositório | convenções, comandos, limites e proibições | `AGENTS.md` de cada repositório |
| Skills | procedimento reutilizável para um tipo de tarefa | `.agents/skills/` no projeto; `npx skills` para as externas |
| MCP | ferramentas e dados externos consultados sob demanda | configuração de MCP do harness, `.omp/mcp.json` no projeto |
| Índice e documentação do código | navegação, busca e arquitetura | `docs/codebase/`, `graphify-out/` |

Cada camada resolve um problema diferente. `AGENTS.md` diz o que vale em qualquer tarefa; skill diz como executar um tipo de tarefa; MCP entrega ferramenta ou dado que o agente não tem; índice encurta a busca no código. O mesmo conteúdo repetido em duas camadas gera conflito, porque a instrução mais próxima do turno vence.

### AGENTS.md e `/init`

`AGENTS.md`, na raiz do repositório, é a fonte única das regras daquele repositório: comandos que funcionam, convenções de código, o que nunca fazer e onde ficam as decisões. `CLAUDE.md` apenas importa ou aponta para ele, para não existirem duas cópias.

`/init` é o comando embutido do OMP e do OpenCode que cria ou melhora o `AGENTS.md` a partir do que o agente lê no repositório. A saída é rascunho: regra errada muda o comportamento em toda tarefa, então a revisão é humana e o arquivo entra em commit como qualquer outra mudança.

Regra prática: `AGENTS.md` curto e específico. O que muda a cada sprint fica na issue ou no documento de estado, não no arquivo de regras.

### Skills do projeto

Fonte canônica: `.agents/skills/`. Cada skill é um procedimento reutilizável, com regras que o agente deve seguir antes de agir. As skills abaixo são as que o projeto adota na data deste documento; a lista real é sempre a do diretório.

Há duas origens de skill, e elas não se misturam:

- **Skills do projeto:** escritas para este repositório, vivem em `.agents/skills/` e são versionadas. São as listadas nesta seção.
- **Skills externas:** vêm de repositórios de terceiros e são instaladas pelo CLI `npx skills`. O procedimento, os alvos e a coleção recomendada por área estão na seção 18.

#### Processo, board e priorização

| Skill | Quando usar |
|---|---|
| `gaps-agile-governance` | interpretar regra do curso GAPS e suas exceções |
| `gaps-dor-board-checklist` | validar uma issue, checar se está pronta ou cumpre o DoR |
| `gaps-issue-refinement` | criar, refinar ou dividir uma issue em GAPS |
| `issue-validation-stamp` | reutilizar, invalidar ou registrar uma validação anterior |
| `github-board-audit-cycle` | auditar o board inteiro |
| `github-projects-v2-ops` | aplicar escrita em Issues e no Project |
| `pm-ab-test-analysis` | analisar resultado de experimento |
| `pm-analyze-feature-requests` | triar e priorizar pedidos de funcionalidade |

#### GitHub, PR e entrega

| Skill | Quando usar |
|---|---|
| `coordenacao-commit-seguro` | preparar commit e PR sem incluir trabalho não autorizado |
| `code-review` | revisar mudança de código |
| `ci-watch-loop` | acompanhar e corrigir checks de CI até ficarem verdes |
| `mash-branch-protection-gh-cli` | conferir ou aplicar proteção de branch |
| `mash-conferir-entrega` | comparar o que um integrante entregou com a issue |

#### Backend, contrato e segurança

| Skill | Quando usar |
|---|---|
| `mash-contrato-api` | escrever ou revisar contrato de rota, status, corpo e nomenclatura |
| `mash-conferir-entrega` | validar entrega contra o contrato da issue |
| `code-review` | revisão de código com foco em regressão e segurança |

#### Documentação e texto

| Skill | Quando usar |
|---|---|
| `docs-state-canonical` | sincronizar documentação com a fonte canônica |
| `mash-texto-sem-slop` | remover marcas de texto gerado por IA em pt-BR |
| `mash-handoff-pessoa` | criar ou atualizar handoff de uma pessoa |

#### Artigo

| Skill | Quando usar |
|---|---|
| `article-academic-review` | revisar artigo do PI: citações, afirmações conflitantes, estrutura e metadados |

#### Exploração de código

| Skill | Quando usar |
|---|---|
| `graphify` | consultar o grafo de conhecimento gerado em `graphify-out/` |

O `graphify` está em validação: a CLI está instalada e o grafo existe, mas a adoção como índice oficial do projeto ainda não foi decidida. Enquanto a validação não termina, o caminho de leitura que não depende dele é o código e `docs/codebase/`. GitNexus e CodeGraph não fazem parte do stack e não têm seção neste documento.

### Disciplina de código: Ponytail

Ponytail não é skill de tarefa: é uma camada de disciplina que fica ativa durante a sessão e empurra o agente para a menor mudança que resolve o problema, com a menor quantidade de código novo.

| Nível | Comportamento |
|---|---|
| `lite` | constrói o que foi pedido e cita em uma linha a opção menor, deixando a escolha para quem pediu |
| `full` | padrão: menor mudança completa, sem abstração, dependência nova ou código para depois |
| `ultra` | questiona o pedido antes de construir e aponta a parte que a necessidade não justifica |
| `off` | desliga as regras |

- Ativa por sessão. Troca de nível com `/ponytail lite`, `/ponytail full`, `/ponytail ultra` ou `/ponytail off`; sem argumento, informa o nível atual.
- `/ponytail-review` revisa a mudança atual, `/ponytail-audit` revisa o repositório inteiro, `/ponytail-debt` recolhe os comentários `shortcut:` em uma lista, `/ponytail-gain` mostra o placar medido e `/ponytail-help` resume os comandos.
- A regra não corta validação em fronteira de confiança, tratamento de erro que evita perda de dado, segurança, acessibilidade nem o que foi pedido.
- Convivência com as skills do projeto: a skill diz como fazer a tarefa; Ponytail limita o tamanho da solução. Nenhuma das duas substitui a outra.

Instalação e comandos ficam na seção 18.

### MCP

MCP (Model Context Protocol) é o protocolo que expõe ferramentas e fontes de dado ao agente como servidores. O agente descobre o que cada servidor oferece e chama só o que a tarefa exige, em vez de carregar o conteúdo inteiro no prompt.

- O servidor é declarado na configuração do harness. No OMP o arquivo do projeto é `.omp/mcp.json`; no OpenCode é a chave `mcp` do `opencode.json`.
- `stdio` sobe um processo local e serve para índice de código na própria máquina. HTTP e SSE apontam para serviço remoto.
- Um servidor por fonte de contexto. Dois servidores que indexam o mesmo código competem entre si e confundem a escolha do agente.

Estado no projeto:

| Servidor | Situação | Como consultar |
|---|---|---|
| `graphify` | em validação | CLI `graphify query`, `graphify path` e `graphify explain` sobre `graphify-out/graph.json` |

A entrada MCP do graphify chama o binário `graphify-mcp`, que não está instalado. Enquanto ele não existir, o servidor não sobe e a consulta é feita pela CLI. O grafo só é atualizado por `graphify update .`; grafo velho responde com estrutura velha.

### Documentação de apoio

- `AGENTS.md`: regras do repositório para o agente, com fonte única por repositório.
- `docs/codebase/`: arquitetura, convenções, integrações, testes e riscos do repositório.
- `codemap.md`: mapa de navegação do código, quando existir.
- `graphify-out/`: grafo, relatório e wiki gerados pela CLI do graphify; o wiki só existe depois de gerado, e nada no fluxo depende dele.

Skill ensina procedimento. Estado atual, números de issue, SHAs, rotas e opções de campo ficam nas fontes canônicas: código, issue do roteiro e GitHub.

## 5. GitHub e fluxo de desenvolvimento

O GitHub é a fonte de verdade do projeto. Toda mudança nasce e termina nele.

| Elemento | Papel |
|---|---|
| Issues | requisito, critério de aceite e contrato da entrega |
| Branches | uma por mudança, com nome ligado ao tipo e à issue |
| Commits | mensagem convencional, em pt-BR, referenciando a issue |
| Pull Requests | revisão, discussão e fechamento da issue |
| Milestones | agrupamento por ciclo de entrega |
| Labels | tipo, escopo e prioridade |
| GitHub Projects | status, sprint, área e estimativa |
| Code review | revisão por par, obrigatória antes do merge |
| Critérios de aceite | condição objetiva para considerar a issue concluída |
| Dependências | vínculo entre issues que impede começar antes |
| Merge | integração na branch principal, com histórico preservado |
| GitHub CLI | operação de issues, PRs e Project por linha de comando |

Fluxo recomendado:

```
Issue -> Branch -> Implementação -> Testes -> Review -> PR -> Merge
```

Regras de convivência:

- a branch principal não recebe commit direto;
- o PR fecha a issue com `Closes #NN`;
- trabalho não autorizado do ambiente local não entra no commit;
- bot e análise estática podem comentar, mas não aprovam nem bloqueiam o merge por conta própria.

## 6. Artigo científico e pesquisa

Três ferramentas, três papéis distintos. Não são intercambiáveis:

| Ferramenta | Papel |
|---|---|
| Elicit | pesquisa científica e revisão de literatura |
| Oleafly | workspace principal para escrita acadêmica com BYOK |
| OpenPrism | alternativa self-hosted no estilo Prism |

**Elicit = pesquisa.** Busca e organiza literatura, apoia a revisão de trabalhos relacionados e a extração de dados de artigos. Não é onde o texto é escrito.

**Oleafly = escrita acadêmica.** Workspace local-first para LaTeX, Typst e Markdown, com bibliografia, compilação, histórico e IA opcional com chave própria. É a ferramenta principal de redação.

**OpenPrism = workspace self-hosted.** Implementação aberta inspirada no Prism, com edição LaTeX, pré-visualização de PDF e assistência de IA local. Serve quando o requisito é rodar a escrita em infraestrutura própria ou manter o conteúdo fora de serviço de terceiro.

Cuidados que valem para as três:

- referência acadêmica é validada na fonte original, nunca só na resposta do modelo;
- resultado experimental não é gerado por IA;
- trecho produzido com apoio de IA é revisado antes de entrar no documento.

## 7. Documentação

A documentação do projeto segue três regras:

1. **Fonte única por assunto.** Uma decisão mora em um lugar canônico; o resto é espelho com data e link.
2. **Estado atualizado na mesma tarefa.** Mudança verificada em código, contrato, board ou decisão atualiza o documento de estado no mesmo trabalho.
3. **Documento gerado não se edita à mão.** Índice, PDF e snapshot são regenerados pela ferramenta que os produz.

A skill `docs-state-canonical` define o procedimento e a lista de consumidores de uma decisão. Textos em pt-BR passam pela `mash-texto-sem-slop` antes de publicar.

## 8. Design e UX/UI

| Ferramenta | Classificação | Papel |
|---|---|---|
| Pen.dev | design agentic principal | exploração e produção de interface com agente |
| Figma | colaboração e handoff | apresentação, revisão com o time, Design System final |
| Starry | alternativa experimental | geração de UI a partir de descrição, com exportação de código |
| Doop | alternativa aberta/self-hosted | canvas multiplayer com agentes via MCP |
| Paper | alternativa para exploração rápida | ideação visual antes do refinamento |
| OpenPencil | não priorizado | editor aberto que abre `.fig` |
| Penpot | não priorizado | plataforma aberta de design e design system |

Regra de ouro: o design aprovado é a referência. O agente não redesenha tela, não troca componente e não cria token por conta própria.

## 9. Frontend

Fluxo:

```
Issue -> requisito -> design aprovado -> implementação -> testes -> browser QA -> review -> PR
```

Ferramentas principais:

- OMP;
- Pen.dev;
- Figma;
- skills de `.agents/skills/`;
- GitHub.

A IA deve respeitar, nesta ordem:

1. o Design System existente;
2. os componentes existentes;
3. os tokens existentes;
4. o layout aprovado.

Redesenhar tela sem necessidade é regressão, não melhoria. Quando a mudança exigir componente novo, a decisão é registrada na issue antes da implementação.

## 10. Backend

Ferramentas principais:

- OMP;
- GitHub;
- testes automatizados;
- documentação da API;
- skills de `.agents/skills/`.

O trabalho é contract-first: o contrato da rota é definido e revisado antes da implementação. O contrato cobre:

- schemas e nomes de campo;
- payloads de entrada e saída;
- formato de erro e mensagem;
- autenticação e autorização;
- status HTTP por caso;
- validação de entrada;
- segurança e exposição de dado;
- testes do caminho felizes e dos erros;
- code review antes do merge.

O padrão de contrato e nomenclatura fica na skill `mash-contrato-api` e na issue de cada rota. Este documento não copia o contrato.

## 11. Descoberta de APIs e modelos gratuitos

Estas ferramentas respondem "o que existe e o que está gratuito agora". Nenhuma delas executa inferência.

| Ferramenta | Classificação |
|---|---|
| FreeTokens.fyi | tracker de modelos/promos gratuitas |
| FreeLLM.net | catálogo de APIs e modelos gratuitos |
| FreeInference.dev | diretório de inferência gratuita utilizável por desenvolvedores |
| Free LLM API Resources | comparação de free tiers, créditos e requisitos |

- **FreeTokens.fyi:** acompanha ofertas gratuitas e a validade declarada. Serve para decidir se uma oferta ainda vale, não como provedor.
- **FreeLLM.net:** catálogo com gerador de configuração, útil para montar o bloco de um provedor sem erro de digitação.
- **FreeInference.dev:** diretório com foco em uso por desenvolvedor.
- **Free LLM API Resources:** compara limites, créditos e requisitos entre provedores.

## 12. Proxies e agregadores de free tiers

**FreeLLMAPI** é agregador e roteador de free tiers. Usa chaves próprias, tenta aproveitar vários free tiers ao mesmo tempo, pode expor endpoint compatível com OpenAI, pode fazer fallback e centraliza provedores em um ponto.

Relação entre as duas ferramentas de nome parecido:

```
FreeLLM.net = descobrir
FreeLLMAPI = agregar/rotear
```

FreeLLM.net lista o que existe. FreeLLMAPI opera o que foi escolhido.

## 13. Gateways de LLM

### LiteLLM: gateway principal

Gateway self-hosted principal do projeto. Entrega endpoint compatível com OpenAI e concentra:

- roteamento entre provedores;
- fallback e retries;
- limites de orçamento;
- chaves virtuais por projeto ou pessoa;
- observabilidade de uso.

### Portkey: gateway com observabilidade

Classificação: **gateway + observabilidade**. Não é provedor de modelos gratuitos. Quando o LiteLLM já resolve roteamento e fallback, o Portkey tende a ser redundante e só se justifica se a observabilidade for o requisito principal.

### Gateways gerenciados

| Ferramenta | Classificação |
|---|---|
| Vercel AI Gateway | gateway gerenciado |
| Cloudflare AI Gateway | gateway e proxy |

Cloudflare AI Gateway não é o mesmo produto que Cloudflare Workers AI: o primeiro é gateway, o segundo é provedor de inferência.

## 14. Provedores de inferência

Organização por função. Limites atuais não são promessa de disponibilidade futura.

### Fontes gratuitas principais

| Provedor | Papel |
|---|---|
| Gemini API | modelos Google, camada gratuita para desenvolvimento |
| Groq | inferência rápida com modelos abertos |
| Z.ai (GLM) | modelos GLM com camada gratuita |

### Alternativas

| Provedor | Papel |
|---|---|
| NVIDIA NIM | catálogo de modelos com créditos de avaliação |
| Cloudflare Workers AI | inferência integrada ao ecossistema Cloudflare |
| OpenRouter | acesso único a vários provedores e modelos |

Antes de depender de uma oferta gratuita, consulte FreeTokens.fyi e FreeLLM.net. Modelos gratuitos mudam, promoções expiram e limites são ajustados sem aviso.

## 15. Modelos locais

**Ollama** é a opção de inferência local: baixa, executa e serve modelos na própria máquina, com API compatível. Serve para:

- trabalho offline;
- dado que não pode sair da máquina;
- teste de prompt sem custo de API;
- fallback quando nenhum provedor externo está disponível.

Modelo local é fallback e laboratório, não substituto automático de provedor para tarefa pesada: qualidade e velocidade dependem do hardware.

## 16. Estratégia de fallback

A ordem abaixo evita depender de um único fornecedor e mantém o custo previsível:

1. **Harness:** OMP. Se indisponível, OpenCode.
2. **Coding gratuito:** Freebuff ou Kilo Code em Auto Free.
3. **Gateway:** LiteLLM como endpoint único, com fallback configurado entre provedores.
4. **Provedor:** Gemini, Groq e Z.ai como primeira camada; NVIDIA NIM, Cloudflare Workers AI e OpenRouter como segunda.
5. **Local:** Ollama quando não houver rede, chave ou cota.

Regras:

- a chave fica no gateway ou no harness, nunca no código da aplicação;
- fallback é testado, não presumido;
- erro de provedor é registrado com o provedor de origem;
- troca de modelo não muda o contrato consumido pela aplicação.

## 17. Recomendação por área

A stack da seção 19 é uma só. O que muda por área é a combinação de harness, skills e ferramentas, e o portão que a entrega precisa atravessar antes do merge ou da publicação.

Cada bloco abaixo tem a mesma estrutura: harness, skills do projeto (`.agents/skills/`), skills externas opcionais, ferramentas e portão de entrega. As skills externas só entram depois do procedimento da seção 18.

### Backend

| Item | Recomendação |
|---|---|
| Harness | OMP; OpenCode como alternativa |
| Skills do projeto | `mash-contrato-api` antes de escrever rota, `code-review` antes do merge, `mash-conferir-entrega`, `ci-watch-loop` |
| Skills externas | `nodejs-backend-patterns`, `api-and-interface-design`, `mysql`, `sequelize`, `security-review` |
| Disciplina de código | Ponytail em `full`; `/ponytail-review` antes do merge |
| Ferramentas | GitHub e GitHub CLI, a issue da rota como contrato, migrations do Sequelize (`npm run db:migrate`) |
| Portão de entrega | contrato aprovado na issue antes do código, testes do caminho felizes e dos erros, review antes do merge, nenhuma credencial no código |

### Frontend

| Item | Recomendação |
|---|---|
| Harness | OMP; OpenCode como alternativa |
| Skills do projeto | `code-review`, `mash-contrato-api` para o consumo da API, `ci-watch-loop` |
| Skills externas | `tailwind-4-docs`, `accessibility`, `web-design-guidelines`, `webapp-testing` |
| Disciplina de código | Ponytail em `full`; `/ponytail-review` antes do merge |
| Ferramentas | Pen.dev para exploração, Figma para o design aprovado, preview na porta 4000 contra a API na 8080 |
| Portão de entrega | aderência ao design aprovado e ao Design System, QA no navegador, nenhuma tela redesenhada sem issue |

### Design

| Item | Recomendação |
|---|---|
| Harness | OMP com MCP |
| Skills do projeto | nenhuma específica de design; a decisão vive na issue de design |
| Skills externas | `figma-use`, `figma-design-to-code`, `web-design-guidelines`, `web-quality-audit`, `accessibility` |
| Ferramentas | Pen.dev para design agentic, Figma para colaboração e handoff |
| Portão de entrega | design aprovado registrado na issue, handoff com componente, estado e token definidos |

### Artigo e pesquisa

| Item | Recomendação |
|---|---|
| Harness | OMP |
| Skills do projeto | `article-academic-review` |
| Skills externas | `latex-paper-en`, `pdf` |
| Ferramentas | Elicit para pesquisa, Oleafly para escrita com BYOK, OpenPrism para escrita self-hosted |
| Portão de entrega | referência validada na fonte original, resultado experimental não gerado por IA, IA não decide o resultado do classificador |

### Documentação

| Item | Recomendação |
|---|---|
| Harness | OMP |
| Skills do projeto | `docs-state-canonical`, `mash-texto-sem-slop`, `mash-handoff-pessoa` |
| Skills externas | `documentation-and-adrs`, `documentation`, `docx` quando o entregável for Word |
| Ferramentas | GitHub como fonte canônica, `docs/codebase/`, `handoff-deposito/` com PDF gerado por `tools/handoff-pdf.py` |
| Portão de entrega | uma fonte por assunto, estado atualizado na mesma tarefa, PDF nunca editado à mão |

Regra comum às cinco áreas: skill do projeto tem precedência sobre skill externa. As internas carregam decisão do projeto (contrato, board, estado, texto); as externas só acrescentam técnica de framework, banco, acessibilidade ou formato.

## 18. Instalar skills com `npx skills`

### O que é

CLI da Vercel Labs que instala skills no formato `SKILL.md` a partir de repositório Git, URL ou diretório local. Na verificação de 24/10/2026 estava na versão 1.7.4 e exige Node.js 22.20 ou superior. O catálogo público fica em https://skills.sh/ e a especificação comum aos agentes em https://agentskills.io.

O CLI instala skill de terceiro no diretório do agente. Ele não escreve o conteúdo da skill nem substitui as skills que já estão no repositório; `npx skills init` apenas cria um `SKILL.md` vazio para ser preenchido.

### Onde a skill é gravada

| Agente | `--agent` | Escopo de projeto | Escopo global (`-g`) |
|---|---|---|---|
| OMP | `pi` | `.agents/skills/` | `~/.agents/skills/` |
| OpenCode | `opencode` | `.agents/skills/` | `~/.config/opencode/skills/` |
| Claude Code | `claude-code` | `.claude/skills/` | `~/.claude/skills/` |
| Codex | `codex` | `.agents/skills/` | `~/.agents/skills/` |
| Kilo Code | `kilo` | `.agents/skills/` | `~/.kilo/skills/` |
| Cline | `cline` | `.agents/skills/` | `~/.agents/skills/` |
| Cursor | `cursor` | `.agents/skills/` | `~/.cursor/skills/` |

O OMP não tem alvo próprio no CLI. Ele varre `.agents/skills/` no projeto e `~/.agents/skills/`, `~/.claude/skills/`, `~/.codex/skills/` e `~/.config/opencode/skills/` no usuário, segundo a documentação de skills do próprio OMP. Por isso o alvo `pi` serve ao OMP: grava exatamente em `.agents/skills/` e `~/.agents/skills/`.

Os diretórios nativos do OMP (`.omp/skills/` e `~/.omp/agent/skills/`) não são usados pelo CLI. Skill copiada à mão para lá fica fora do controle de versão e do `npx skills list`.

### Escopo: projeto ou global

| Escopo | Efeito | Quando usar |
|---|---|---|
| Projeto (padrão) | grava em `.agents/skills/` ou `.claude/skills/`, dentro do repositório | a equipe adotou a skill e ela deve ser versionada |
| Global (`-g`) | grava no diretório do usuário, fora do repositório | teste e uso individual |

No repositório de coordenação do projeto, `.agents/skills/` é versionado e concentra as skills do projeto. Instalar em escopo de projeto mistura skill externa com skill interna no mesmo diretório, e o resultado vai para o commit. O caminho seguro é testar com `-g` e só promover para o projeto depois de ler o `SKILL.md` e revisar o diff.

### Comandos

| Objetivo | Comando |
|---|---|
| descobrir skill | `npx skills find` ou `npx skills find <termo>` |
| ver o que um repositório oferece | `npx skills add <owner/repo> --list` |
| instalar uma skill | `npx skills add <owner/repo> --skill <nome>` |
| escolher o agente | `-a <agente>`, repetível |
| instalar no escopo global | `-g` |
| copiar em vez de criar symlink | `--copy` |
| instalar sem confirmação | `-y` |
| listar instaladas | `npx skills list` |
| testar sem instalar | `npx skills use <owner/repo>@<skill>` |
| conferir atualização | `npx skills check` |
| atualizar | `npx skills update [skill]` |
| remover | `npx skills remove <skill>` |
| criar skill nova | `npx skills init <nome>` |

O padrão é symlink: uma cópia canônica e links por agente. `--copy` existe para agente que não aceita symlink e cria cópias independentes, que precisam ser atualizadas uma a uma.

### Fluxo em seis passos

1. **Descobrir:** `npx skills find <termo>` ou a busca em https://skills.sh/.
2. **Ler antes de instalar:** `npx skills add <owner/repo> --list` mostra os nomes; o `SKILL.md` mostra o que o agente passa a fazer.
3. **Testar global:** instalar com `-g`, no agente que será usado.
4. **Conferir:** `npx skills list` deve mostrar a skill no agente certo. Skill que não aparece está no escopo ou no agente errado.
5. **Adotar:** se a equipe decidir manter, instalar no escopo de projeto, revisar o diff e commitar como qualquer outra mudança.
6. **Manter:** `npx skills check` e `npx skills update` de tempos em tempos; atualização de skill externa muda comportamento do agente e entra em PR.

### Instalação por área

Os comandos abaixo usam o alvo `pi`, que grava onde o OMP lê, e o escopo global, para não alterar o repositório. Todos os nomes e repositórios foram conferidos no catálogo em 24/10/2026.

Backend:

```bash
npx skills add wshobson/agents --skill nodejs-backend-patterns -a pi -g -y
npx skills add addyosmani/agent-skills --skill api-and-interface-design -a pi -g -y
npx skills add planetscale/database-skills --skill mysql -a pi -g -y
npx skills add mindrally/skills --skill sequelize -a pi -g -y
npx skills add getsentry/skills --skill security-review -a pi -g -y
```

Frontend:

```bash
npx skills add lombiq/tailwind-agent-skills --skill tailwind-4-docs -a pi -g -y
npx skills add addyosmani/web-quality-skills --skill accessibility -a pi -g -y
npx skills add vercel-labs/agent-skills --skill web-design-guidelines -a pi -g -y
npx skills add anthropics/skills --skill webapp-testing -a pi -g -y
```

Design:

```bash
npx skills add figma/mcp-server-guide --skill figma-use -a pi -g -y
npx skills add figma/mcp-server-guide --skill figma-design-to-code -a pi -g -y
npx skills add addyosmani/web-quality-skills --skill web-quality-audit -a pi -g -y
```

Artigo e pesquisa:

```bash
npx skills add bahayonghang/academic-writing-skills --skill latex-paper-en -a pi -g -y
npx skills add anthropics/skills --skill pdf -a pi -g -y
```

Documentação:

```bash
npx skills add addyosmani/agent-skills --skill documentation-and-adrs -a pi -g -y
npx skills add anthropics/knowledge-work-plugins --skill documentation -a pi -g -y
npx skills add anthropics/skills --skill docx -a pi -g -y
```

Para adotar uma skill no projeto e deixá-la disponível para a equipe, o comando perde o `-g` e ganha os agentes usados no repositório:

```bash
npx skills add anthropics/skills --skill webapp-testing -a pi -a opencode -a claude-code -y
```

Nesse formato a skill entra em `.agents/skills/` e o Claude Code recebe um link em `.claude/skills/`. O commit precisa passar por review, porque `SKILL.md` é instrução executada pelo agente, com o mesmo risco de um script.

### Ponytail: skills pelo `npx skills`

Ponytail é plugin, não uma skill avulsa: o ruleset fica ativo a cada turno e os comandos `/ponytail-*` vêm do plugin. Baixar as seis skills pelo `npx skills` entrega o procedimento sem o ruleset sempre ativo, e é o caminho quando o harness não aceita plugin.

As seis skills, no alvo do OMP e em escopo global:

```bash
npx skills add DietrichGebert/ponytail --skill '*' -a pi -g -y
```

Uma por vez:

```bash
npx skills add DietrichGebert/ponytail --skill ponytail -a pi -g -y
npx skills add DietrichGebert/ponytail --skill ponytail-review -a pi -g -y
npx skills add DietrichGebert/ponytail --skill ponytail-audit -a pi -g -y
npx skills add DietrichGebert/ponytail --skill ponytail-debt -a pi -g -y
npx skills add DietrichGebert/ponytail --skill ponytail-gain -a pi -g -y
npx skills add DietrichGebert/ponytail --skill ponytail-help -a pi -g -y
```

Para deixar as skills versionadas no projeto, o comando perde o `-g` e ganha os agentes do repositório:

```bash
npx skills add DietrichGebert/ponytail --skill '*' -a pi -a opencode -a claude-code -y
```

Diferença entre as duas rotas:

| Rota | O que instala | Nível e comandos |
|---|---|---|
| `npx skills add DietrichGebert/ponytail --skill '*'` | as seis skills em `.agents/skills/` ou `~/.agents/skills/` | não; o comportamento vem do `SKILL.md` carregado |
| plugin | skills, hooks e ruleset ativo por turno | sim; `/ponytail` e `/ponytail-*` |

Instalação como plugin, por harness:

| Harness | Comando |
|---|---|
| Claude Code | `/plugin marketplace add DietrichGebert/ponytail` e depois `/plugin install ponytail@ponytail` |
| OMP | `omp plugin marketplace add DietrichGebert/ponytail` e `omp plugin install ponytail@ponytail` |
| OpenCode | `opencode plugin add @dietrichgebert/ponytail`, ou `"plugins": ["@dietrichgebert/ponytail"]` no `opencode.json` |
| Codex | `codex plugin marketplace add DietrichGebert/ponytail` e `codex plugin add ponytail@ponytail`; depois confiar nos dois hooks em `/hooks` |

Depois de instalar como plugin, abrir sessão nova e rodar `/ponytail full`. O plugin oficial vem de `DietrichGebert/ponytail` no GitHub ou `@dietrichgebert/ponytail` no npm; cópia de outro pacote com o mesmo nome não é o original.

### Regras de convivência

- skill externa não substitui skill do projeto: contrato, board, estado e texto continuam nas internas;
- skill que contradiga decisão registrada não entra, mesmo com muitas instalações no catálogo;
- `SKILL.md` é lido antes da adoção, incluindo scripts e arquivos que ele referencia;
- `skills-lock.json` registra a origem e não é editado à mão;
- instalação com `--skill '*'` só em repositório conhecido, e nunca no escopo de projeto sem revisão;
- skill externa que deixou de ser usada é removida com `npx skills remove`, para não inflar o contexto do agente.

### Problemas comuns

| Sintoma | Causa provável | Correção |
|---|---|---|
| erro de versão ao rodar `npx skills` | Node.js abaixo de 22.20 | atualizar o Node |
| skill instalada e não usada pelo agente | agente não instalado ou alvo errado | `npx skills list -a <agente>` e reinstalar com o alvo correto |
| comando travado pedindo confirmação | execução não interativa | `-y` |
| skill duplicada com versões diferentes | uma cópia no projeto e outra global | remover uma com `npx skills remove -g <skill>` |
| skill externa sobrescrevendo comportamento esperado | conflito com skill do projeto | remover a externa e registrar a decisão em issue |

## 19. Stack mínima recomendada

| Frente | Ferramenta |
|---|---|
| Desenvolvimento | OMP |
| Alternativa de desenvolvimento | OpenCode |
| Skills do projeto | `.agents/skills/` |
| Skills externas | `npx skills` |
| Disciplina de código | Ponytail |
| Contexto externo | MCP |
| Índice de código | graphify (em validação) |
| Coding gratuito | Freebuff ou Kilo Code |
| Artigo: pesquisa | Elicit |
| Artigo: escrita | Oleafly |
| Artigo: self-hosted | OpenPrism |
| Design agentic | Pen.dev |
| Colaboração e handoff | Figma |
| GitHub | GitHub e GitHub CLI |
| Descoberta de modelos gratuitos | FreeTokens.fyi e FreeLLM.net |
| Agregação de free tiers | FreeLLMAPI |
| Gateway | LiteLLM |
| Gateway alternativo | Portkey |
| APIs gratuitas principais | Gemini, Groq e Z.ai |
| APIs adicionais | NVIDIA NIM, Cloudflare Workers AI e OpenRouter |
| Local | Ollama |

Essa é a stack suficiente para o projeto. O resto é alternativa, experimento ou item não priorizado.

## 20. Ferramentas alternativas

| Ferramenta | Alternativa a | Quando faz sentido |
|---|---|---|
| OpenCode | OMP | preferência por harness open source com BYOK |
| Freebuff | harness pago | tarefa de código sem custo, com modelo do dia |
| Kilo Code | harness pago | IDE ou CLI com Auto Free e chave própria |
| Codex | OMP | tarefa pontual com a conta OpenAI |
| Claude Code | OMP | tarefa pontual com a conta Anthropic |
| Starry | Pen.dev | exploração de UI com exportação de código |
| Doop | Figma | canvas aberto com agente via MCP |
| Paper | Figma | ideação visual rápida |
| OpenPrism | Oleafly | escrita acadêmica em infraestrutura própria |
| Portkey | LiteLLM | observabilidade como requisito principal |
| Vercel AI Gateway | LiteLLM | operação gerenciada sem servidor próprio |
| Cloudflare AI Gateway | LiteLLM | projeto já hospedado na Cloudflare |
| NVIDIA NIM | Gemini | avaliação de modelo específico |
| Cloudflare Workers AI | Gemini | inferência próxima da aplicação na Cloudflare |
| OpenRouter | gateway próprio | acesso a vários modelos sem montar gateway |
| Ollama | provedor externo | offline, privacidade ou teste local |

## 21. Ferramentas não priorizadas

| Ferramenta | Motivo |
|---|---|
| OpenPencil | editor aberto promissor, mas sem vantagem concreta sobre o fluxo atual com Pen.dev e Figma |
| Penpot | plataforma aberta de design e design system, sem necessidade atual; reavaliar se houver requisito de self-hosted |

Reavaliação só com requisito concreto registrado em issue.

## 22. Critérios para adicionar novas ferramentas

Uma ferramenta entra neste documento quando:

1. resolve necessidade real e registrada do projeto;
2. tem site e documentação oficiais confirmados;
3. tem licença e modelo de custo explícitos;
4. deixa claro o que acontece com o dado enviado;
5. não duplica ferramenta já aprovada sem vantagem concreta;
6. tem manutenção ativa ou uso consolidado;
7. não exige compartilhar credencial entre pessoas;
8. pode ser removida sem quebrar o fluxo.

Ferramenta sem repositório público oficial confirmado entra com essa ressalva escrita. Nome parecido não é prova de origem: fork e repositório homônimo não contam como oficial.

## 23. Links rápidos

- Harness principal: https://omp.sh/docs
- Alternativa open source: https://opencode.ai/docs/
- Skills do projeto: `.agents/skills/`
- Skills externas: https://skills.sh/
- Disciplina de código: https://ponytail.dev/
- MCP: https://modelcontextprotocol.io/docs
- Índice de código: https://github.com/Graphify-Labs/graphify
- Fluxo do projeto: https://github.com/conloq
- Escrita acadêmica: https://oleafly.com/docs
- Design colaborativo: https://www.figma.com/
- Gateway: https://docs.litellm.ai/
- Modelos gratuitos: https://freetokens.fyi/ e https://freellm.net/
- Inferência local: https://docs.ollama.com/
