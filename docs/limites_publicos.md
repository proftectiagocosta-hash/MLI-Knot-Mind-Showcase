# Limites Públicos

Este repositório é uma vitrine pública sanitizada do `MLI-Knot-Mind`.

## Permitido

- explicar conceitos e princípios;
- publicar arquitetura sanitizada;
- citar as operações públicas `prepare_invocation`, `validate_result` e `capabilities`;
- explicar a separação entre Mind, modelo, host, MCP e execução;
- documentar a exposição MCP em nível de contrato público;
- registrar resultados agregados de validação, como `55/55`;
- explicar que a campanha O0–O5 foi concluída;
- explicar os limites do O4 e o caráter sintético de `ENV-OTHER`;
- mostrar exemplos fictícios e casos de uso;
- demonstrar diferença entre resposta genérica e resposta governada.

## Não permitido

- publicar código-fonte privado do core;
- publicar prompts privados completos ou dumps de governança;
- publicar checkpoints reais;
- publicar caminhos operacionais privados;
- publicar hashes Git privados como narrativa pública;
- publicar credenciais, tokens ou provider keys;
- publicar histórico bruto de conversas;
- expor rotinas internas sensíveis;
- importar automaticamente material do núcleo privado;
- publicar dados pessoais;
- publicar comandos privados de ativação;
- representar o Context Agent como componente obrigatório;
- representar tunnel como requisito do core;
- representar MCP como identidade do Mind;
- representar host ou provider como identidade ou autoridade do Mind;
- representar `ENV-OTHER` como deployment real;
- afirmar execução automática ou memória persistente;
- promover validação limitada a prova universal;
- afirmar produção pronta sem evidência específica;
- confundir vitrine pública com núcleo operacional.

## Regra de ouro

A superfície pública pode demonstrar **o que foi validado e quais fronteiras existem**, mas não deve publicar material suficiente para reconstruir o núcleo privado nem converter evidência limitada em afirmação universal.
