# FAQ — MLI-Knot Mind

## MLI-Knot Mind é uma IA?

Não. O Mind é uma camada de governança e processamento. Um modelo de IA pode realizar inferência por meio de um host, mas modelo e provider não são a identidade nem a autoridade do Mind.

## Ele guarda memória?

Não como memória persistente de sessão. O core é stateless entre chamadas.

Contexto anterior pode ser fornecido explicitamente como entrada, mas isso não vira memória implícita apenas por ter sido usado antes.

## Quais operações públicas do core podem ser descritas?

A superfície sanitizada pode citar `prepare_invocation`, `validate_result` e `capabilities`.

`validate_result` valida contrato e estrutura; não certifica automaticamente verdade factual ou correção do conteúdo.

## MCP é obrigatório?

Não.

A exposição MCP é um adapter opcional e separado. A superfície validada possui duas tools — `mind_prepare_invocation` e `mind_validate_result` — e o resource `mind://core/capabilities`.

O core não depende de MCP e MCP não é o Mind.

## O host executa ferramentas?

Não no contrato público validado. O host tem papel de inferência (`INFERENCE_ONLY`).

Observação autônoma, tool call, execução, memória persistente e inferência de ambiente não são promovidas a responsabilidades do host.

## O Mind executa ações automaticamente?

Não.

O desenho separa necessidade de evidência, decisão de ferramenta, chamada de ferramenta, autorização e execução. Uma saída `RELEASE` não é autorização automática para agir externamente.

## O Context Agent é obrigatório?

Não. Ele pode ser uma fonte externa opcional de evidência, mas não é dependência obrigatória do core.

## Um tunnel é obrigatório?

Não. Tunnel é infraestrutura opcional e não faz parte da identidade do Mind.

## O Mind exige ENV-CASA ou ENV-ALEAM?

Não. O core foi desenhado para aceitar ambiente explícito quando relevante ou operar sem ambiente declarado.

## O que foi validado no O4?

Uma matriz determinística cobriu `ENV-CASA`, `ENV-ALEAM`, um `ENV-OTHER` sintético e ausência da chave de ambiente.

O `ENV-OTHER` é um caso sintético de portabilidade. Ele não prova que houve deployment real em um terceiro ambiente nem prova equivalência universal.

## Qual foi o resultado final da campanha O0–O5?

A regressão final O5 consolidou `55/55`, e a campanha O0–O5 foi fechada por continuidade canônica no núcleo privado.

A vitrine publica apenas o resultado sanitizado, não os checkpoints, hashes, caminhos ou artefatos privados que sustentam o fechamento.

## Ele substitui o usuário?

Não. Governança, evidência e validação melhoram o processamento, mas autoridade e autorização continuam explicitamente separadas.

## Esta vitrine contém os prompts privados?

Não. Este repositório é público e sanitizado.

## Posso usar os princípios em meus próprios fluxos?

Sim, para uso não comercial conforme a licença pública. Uso comercial exige autorização.
