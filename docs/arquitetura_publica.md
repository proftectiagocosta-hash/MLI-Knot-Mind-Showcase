# Arquitetura Pública — MLI-Knot Mind

## Visão geral

O MLI-Knot Mind é uma camada de governança e processamento separada do modelo de IA, do host, da exposição MCP e de qualquer executor externo.

A projeção pública do fluxo operacional é:

```text
Contexto explícito
      ↓
Mind core
prepare_invocation
      ↓
Host / modelo
INFERENCE_ONLY
      ↓
Resultado candidato
      ↓
Mind core
validate_result
      ↓
RELEASE / REVISE / HOLD
```

`validate_result` verifica contrato e estrutura. Ele não prova automaticamente verdade, correção factual ou suficiência do resultado.

`RELEASE` também não significa autorização para executar uma ação externa.

## Fronteiras arquiteturais

### Mind core

O core público pode ser descrito pelas operações:

- `prepare_invocation`;
- `validate_result`;
- `capabilities`.

Ele é agnóstico de ambiente, stateless entre chamadas e não cria memória implícita de sessão.

A ausência de ambiente declarado é um estado válido. O core não deve inferir `ENV-CASA`, `ENV-ALEAM` ou outro ambiente pela localização do runtime.

### Modelo e host

O modelo é o motor de inferência, não a autoridade do Mind.

A integração de host é provider-neutral e o papel público do host é `INFERENCE_ONLY`.

Não são responsabilidades promovidas ao host:

- observação autônoma;
- tool call;
- execução;
- memória persistente;
- inferência silenciosa de ambiente.

Provider não é autoridade e engine de IA não é identidade do Mind.

### Exposição MCP opcional

O adapter MCP é uma camada separada. A superfície validada expõe:

- tool `mind_prepare_invocation`;
- tool `mind_validate_result`;
- resource `mind://core/capabilities`.

As tools usam structured output. `stdio` é o transporte inicial documentado.

O core não depende de MCP para existir ou operar.

MCP não é o Mind.

### Context Agent e tunnel

O Context Agent pode fornecer evidência externa quando explicitamente disponível, mas não é componente obrigatório do Mind.

Tunnel é infraestrutura opcional de transporte entre fronteiras e também não é requisito do core.

### Execução externa

O Mind distingue necessidade de evidência, decisão de usar ferramenta, chamada de ferramenta e execução.

Uma recomendação ou uma disposição `RELEASE` não concede por si só autorização operacional.

## Campanha operacional O0–O5

A campanha privada concluída pode ser resumida publicamente assim:

- **O0:** separação do modelo de execução e das fronteiras.
- **O1:** core agnóstico de ambiente, stateless e sem memória implícita.
- **O2:** adapter MCP opcional, com duas tools e um resource.
- **O3:** integração provider-neutral com host de inferência.
- **O4:** validação determinística em `ENV-CASA`, `ENV-ALEAM`, `ENV-OTHER` sintético e ausência de ambiente.
- **O5:** regressão final `55/55` e fechamento por continuidade canônica.

O `ENV-OTHER` do O4 é um caso sintético de portabilidade. Ele não é evidência de um terceiro deployment real.

A validação O4 também não constitui prova universal de equivalência entre todos os ambientes, hosts, modelos ou providers.

## Separação epistêmica

O processamento preserva distinções como:

- fato confirmado;
- inferência;
- hipótese;
- `UNKNOWN`;
- limitação;
- necessidade de evidência;
- próximo passo possível.

## Limite público

Esta arquitetura é sanitizada. Ela descreve fronteiras, contratos públicos e resultados agregados sem expor código-fonte privado, prompts completos, checkpoints reais, caminhos operacionais, hashes internos, credenciais ou mecanismos sensíveis.
