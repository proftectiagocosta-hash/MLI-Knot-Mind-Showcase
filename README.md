# MLI-Knot-Mind-Showcase

> **Status:** vitrine pública sanitizada do `MLI-Knot-Mind`, alinhada ao estado operacional O0–O5 concluído.
> **Núcleo fonte:** privado/local; não incluído nesta superfície pública.
> **Função pública:** apresentar princípios, arquitetura sanitizada e capacidades verificadas sem expor código-fonte privado, prompts internos ou evidência operacional sensível.

![Status](https://img.shields.io/badge/status-public%20showcase-blue)
![Scope](https://img.shields.io/badge/scope-sanitized%20operational%20overview-darkgreen)
![Core](https://img.shields.io/badge/private%20core-not%20included-red)
![Language](https://img.shields.io/badge/language-PT--BR%20%7C%20EN-informational)
![Closed operational campaign](https://img.shields.io/badge/closed%20operational%20campaign-100%25-brightgreen)
![GitHub stars](https://img.shields.io/github/stars/proftectiagocosta-hash/MLI-Knot-Mind-Showcase?style=flat&label=stars)
![README views](https://hits.sh/github.com/proftectiagocosta-hash/MLI-Knot-Mind-Showcase.svg?label=README%20views)

[Português](#português) | [English](#english)

---

<div align="center">

<img src="assets/matrix-inspired-banner.gif" width="100%" alt="MLI-Knot Mind cyber governance banner" />

</div>

---

## Português

### O que é

O **MLI-Knot Mind** é um processador de governança para fluxos assistidos por IA. Ele organiza como contexto explícito, evidência, incerteza, invariantes e intenção são preparados antes da inferência e como um resultado candidato é validado estruturalmente antes de ser liberado.

O Mind **não é o modelo de IA**, não é memória persistente, não é banco de estados, não é cofre de histórico e não é executor automático. Modelo, host, exposição MCP e eventual executor são fronteiras separadas.

Esta vitrine apresenta somente uma projeção pública sanitizada. Código-fonte privado, prompts completos, checkpoints reais, caminhos operacionais, credenciais e mecanismos internos não são publicados aqui.

### Estado operacional público

A campanha operacional **O0–O5** do núcleo privado foi concluída. O que pode ser afirmado publicamente, sem expor material privado, é:

- **O0 — Modelo de execução:** fronteiras entre Mind, modelo, host, MCP e execução foram separadas; ambiente é contexto operacional, não identidade do Mind.
- **O1 — Core agnóstico de ambiente:** o core expõe `prepare_invocation`, `validate_result` e `capabilities`; é stateless e não cria memória implícita entre chamadas.
- **O2 — Exposição MCP opcional:** um adapter separado expõe duas tools e um resource de capacidades, com structured output e `stdio` como transporte inicial; o core não depende de MCP.
- **O3 — Host Integration:** a integração é provider-neutral e o host é restrito a inferência; observação, tool call, execução e memória persistente não são promovidas a funções do host.
- **O4 — Validação multiambiente:** regressões determinísticas cobriram `ENV-CASA`, `ENV-ALEAM`, um `ENV-OTHER` sintético e ausência de ambiente. O caso sintético testa portabilidade e **não prova um terceiro deployment real nem equivalência universal**.
- **O5 — Regressão e continuidade:** a regressão final consolidou **55/55** testes e a campanha O0–O5 foi encerrada por continuidade canônica.

Esses resultados descrevem o escopo validado. Eles não significam produto pronto para produção, deployment universal ou validação de todo provider possível.

### Progresso da campanha operacional documentada

A campanha operacional fechada é composta pelos seis marcos O0, O1, O2, O3, O4 e O5. Todos os seis estão documentados como concluídos no núcleo fonte e refletidos nesta vitrine pública sanitizada.

**Campanha operacional fechada: 6/6 = 100%.**

O denominador é exclusivamente a campanha operacional O0–O5 já encerrada. Este percentual **não** representa conclusão total do produto, conclusão de todas as evoluções públicas do roadmap, prontidão de produção, compatibilidade universal com providers ou encerramento futuro do ecossistema Mind.

### Fluxo público simplificado

```text
contexto explícito
        ↓
Mind core: prepare_invocation
        ↓
host/modelo: inferência somente
        ↓
resultado candidato
        ↓
Mind core: validate_result
        ↓
RELEASE / REVISE / HOLD
```

`validate_result` valida contrato e estrutura; não transforma automaticamente uma saída em verdade. Da mesma forma, `RELEASE` não equivale a autorização para executar uma ação externa.

A exposição MCP é opcional e fica ao redor do core. O **Context Agent** também permanece uma fonte externa opcional de evidência; ele não é componente obrigatório do Mind. Tunnel não é requisito do core.

### Princípios públicos

- honestidade intelectual;
- separação entre fato, hipótese, inferência, limitação e `UNKNOWN`;
- clareza de escopo;
- disciplina de contexto;
- rastreabilidade mínima;
- governança de prompts;
- redução de alucinação;
- distinção entre evidência, decisão de ferramenta, chamada de ferramenta e execução;
- resposta útil antes de resposta impressionante.

### O que esta vitrine contém

- visão pública do framework;
- arquitetura operacional sanitizada;
- estado público O0–O5;
- princípios conceituais;
- exemplos sanitizados;
- casos de uso;
- limites públicos;
- documentação bilíngue;
- templates públicos de apoio;
- vitrine HTML simples.

### O que esta vitrine não contém

- código-fonte privado do core;
- prompts privados completos;
- checkpoints reais;
- hashes e caminhos operacionais internos;
- histórico bruto;
- dados pessoais;
- credenciais ou provider keys;
- estados internos do ecossistema;
- regras privadas de ativação;
- mecanismos internos completos;
- material operacional sensível.

### Templates públicos de apoio

| Template | Uso |
|---|---|
| [Prompt Governance Checklist](https://gist.github.com/proftectiagocosta-hash/96e4de684b44b3ae115f4641803e7893) | Separar fatos, hipóteses, inferências, limitações, decisões e próximos passos. |
| [Project Resume Template](https://gist.github.com/proftectiagocosta-hash/007d4e9659b2f997452abf550002d829) | Retomar projetos sem perder o que já funciona e o que permanece pendente. |
| [README Project Status Template](https://gist.github.com/proftectiagocosta-hash/057195ac4a551383358fb871f8993219) | Tornar o estado de um repositório mais explícito e verificável. |

Veja também [`docs/public_templates.md`](docs/public_templates.md).

### Superfícies públicas relacionadas

| Superfície | Papel público |
|---|---|
| [`Tendoshk-Cerebro-Showcase`](https://github.com/proftectiagocosta-hash/Tendoshk-Cerebro-Showcase) | Continuidade, curadoria e arquitetura pública de memória. |
| [`MLI-Knot-Cursos-Showcase`](https://github.com/proftectiagocosta-hash/MLI-Knot-Cursos-Showcase) | Vitrine sanitizada do fluxo educacional. |
| [`MLI-Knot-ScriptPackage-Showcase`](https://github.com/proftectiagocosta-hash/MLI-Knot-ScriptPackage-Showcase) | Vitrine sanitizada do conceito ScriptPackage v0.1. |
| [`MLI-Knot-LAB-CLUSTER-PUBLIC`](https://github.com/proftectiagocosta-hash/MLI-Knot-LAB-CLUSTER-PUBLIC) | Vitrine técnica sanitizada com publicação auditada. |
| [`MLI-Knot-Keyboard`](https://github.com/proftectiagocosta-hash/MLI-Knot-Keyboard) | Ferramenta pública para digitação controlada no Windows. |

### Documentação principal

- [`MANIFESTO.md`](MANIFESTO.md)
- [`ROADMAP.md`](ROADMAP.md)
- [`SECURITY.md`](SECURITY.md)
- [`docs/STATUS_PUBLICO.md`](docs/STATUS_PUBLICO.md)
- [`docs/arquitetura_publica.md`](docs/arquitetura_publica.md)
- [`docs/principios_publicos.md`](docs/principios_publicos.md)
- [`docs/limites_publicos.md`](docs/limites_publicos.md)
- [`docs/exemplos_sanitizados.md`](docs/exemplos_sanitizados.md)
- [`docs/casos_de_uso.md`](docs/casos_de_uso.md)
- [`docs/faq.md`](docs/faq.md)
- [`docs/public_templates.md`](docs/public_templates.md)

### Limite público

O repositório público descreve contratos, princípios e resultados sanitizados. Ele não é espelho, backup nem distribuição do `MLI-Knot-Mind` privado.

---

## English

### What it is

**MLI-Knot Mind** is a governance processor for AI-assisted workflows. It structures how explicit context, evidence, uncertainty, invariants and intent are prepared before inference, and how a candidate result is structurally validated before release.

Mind **is not the AI model**, persistent memory, a state database, a raw-history vault or an automatic executor. Model, host, MCP exposure and any external executor remain separate boundaries.

This repository is only a sanitized public projection. Private source code, complete prompts, real checkpoints, operational paths, credentials and internal mechanisms are not published here.

### Public operational status

The private core's **O0–O5 operational campaign is complete**. The public-safe summary is:

- **O0 — Execution model:** Mind, model, host, MCP and execution boundaries are separated; environment is operational context, not Mind identity.
- **O1 — Environment-agnostic core:** the core exposes `prepare_invocation`, `validate_result` and `capabilities`; it is stateless and creates no implicit memory between calls.
- **O2 — Optional MCP exposure:** a separate adapter exposes two tools and one capabilities resource, with structured output and `stdio` as the initial transport; the core does not require MCP.
- **O3 — Host Integration:** integration is provider-neutral and the host is inference-only; observation, tool calls, execution and persistent memory are not promoted to host responsibilities.
- **O4 — Multi-environment validation:** deterministic regressions covered `ENV-CASA`, `ENV-ALEAM`, a synthetic `ENV-OTHER`, and no declared environment. The synthetic case tests portability and **does not prove a real third deployment or universal equivalence**.
- **O5 — Regression and continuity:** the final regression consolidated **55/55** tests and the O0–O5 campaign was closed through canonical continuity.

These results describe the validated scope. They do not imply production readiness, universal deployment or validation against every possible provider.

### Documented operational campaign progress

The closed operational campaign consists of six milestones: O0, O1, O2, O3, O4 and O5. All six are documented as complete in the private source core and reflected in this sanitized public showcase.

**Closed operational campaign: 6/6 = 100%.**

The denominator is limited strictly to the already-closed O0–O5 operational campaign. This percentage is **not** total product completion, completion of every public-roadmap evolution, production readiness, universal provider compatibility, or final completion of the future Mind ecosystem.

### Simplified public flow

```text
explicit context
      ↓
Mind core: prepare_invocation
      ↓
host/model: inference only
      ↓
candidate result
      ↓
Mind core: validate_result
      ↓
RELEASE / REVISE / HOLD
```

`validate_result` validates contract and structure; it does not automatically turn an output into truth. Likewise, `RELEASE` is not authorization to execute an external action.

MCP exposure is optional and sits around the core. The **Context Agent** remains an optional external evidence source rather than a required Mind component. A tunnel is not a core requirement.

### Public principles

- intellectual honesty;
- separation between fact, hypothesis, inference, limitation and `UNKNOWN`;
- scope clarity;
- context discipline;
- minimal traceability;
- prompt governance;
- reduced hallucination;
- separation between evidence, tool decision, tool call and execution;
- useful answers before impressive answers.

### What this showcase contains

- public framework overview;
- sanitized operational architecture;
- public O0–O5 status;
- conceptual principles;
- sanitized examples;
- use cases;
- public limits;
- bilingual documentation;
- public companion templates;
- simple HTML showcase.

### What it does not contain

- private core source code;
- full private prompts;
- real checkpoints;
- private operational hashes and paths;
- raw history;
- personal data;
- credentials or provider keys;
- internal ecosystem state;
- private activation rules;
- complete internal mechanisms;
- sensitive operational material.

### Public companion templates

| Template | Use |
|---|---|
| [Prompt Governance Checklist](https://gist.github.com/proftectiagocosta-hash/96e4de684b44b3ae115f4641803e7893) | Separate facts, hypotheses, inferences, limitations, decisions, and next steps. |
| [Project Resume Template](https://gist.github.com/proftectiagocosta-hash/007d4e9659b2f997452abf550002d829) | Resume project work without losing what already works or remains pending. |
| [README Project Status Template](https://gist.github.com/proftectiagocosta-hash/057195ac4a551383358fb871f8993219) | Make repository state explicit and easy to verify. |

### Related public surfaces

- [`Tendoshk-Cerebro-Showcase`](https://github.com/proftectiagocosta-hash/Tendoshk-Cerebro-Showcase)
- [`MLI-Knot-Cursos-Showcase`](https://github.com/proftectiagocosta-hash/MLI-Knot-Cursos-Showcase)
- [`MLI-Knot-ScriptPackage-Showcase`](https://github.com/proftectiagocosta-hash/MLI-Knot-ScriptPackage-Showcase)
- [`MLI-Knot-LAB-CLUSTER-PUBLIC`](https://github.com/proftectiagocosta-hash/MLI-Knot-LAB-CLUSTER-PUBLIC)
- [`MLI-Knot-Keyboard`](https://github.com/proftectiagocosta-hash/MLI-Knot-Keyboard)

---

## Public status

```text
Repository type: public sanitized showcase
Source core: private/local governance processor
Operational campaign: O0-O5 complete
Final deterministic regression: 55/55
Environment required by core: no
MCP required by core: no
Persistent session memory: no
Automatic execution: no
Private core included here: no
Sensitive material included here: no
```

## License

This public documentation is released under **CC BY-NC 4.0** unless otherwise stated. Commercial use requires prior authorization.
