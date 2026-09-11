# Roadmap Público — MLI-Knot Mind

## Estado atual

- [x] Criar vitrine pública sanitizada.
- [x] Definir fronteira entre núcleo privado e documentação pública.
- [x] Documentar princípios públicos.
- [x] Criar exemplos sanitizados.
- [x] Criar vitrine HTML simples.
- [x] Publicar repositório público.
- [x] Registrar publicamente, de forma sanitizada, a campanha operacional O0–O5 concluída.
- [x] Documentar a separação entre Mind, modelo, host, MCP e execução.
- [x] Documentar o core agnóstico de ambiente e sem memória implícita.
- [x] Documentar a exposição MCP opcional.
- [x] Documentar a integração provider-neutral com host de inferência.
- [x] Documentar os limites da validação multiambiente.
- [x] Registrar a regressão final O5 em `55/55`.
- [ ] Publicar GitHub Pages, se fizer sentido.
- [ ] Adicionar screenshots ou diagramas visuais revisados.

## Próximas evoluções públicas possíveis

- [ ] Criar um diagrama visual sanitizado do fluxo `contexto -> core -> host/modelo -> validação`.
- [ ] Criar matriz pública de avaliação de qualidade.
- [ ] Criar checklist público para uso de IA em projetos longos.
- [ ] Criar exemplos públicos minimalistas para `prepare_invocation` e `validate_result` sem reproduzir o núcleo privado.
- [ ] Executar e documentar, se útil, compatibilidade opcional com um provider real sem promover provider a autoridade.
- [ ] Criar release pública da documentação quando a superfície estiver estável.

## O que não é requisito de fechamento

O fechamento O0–O5 não depende de:

- provider específico;
- Context Agent obrigatório;
- tunnel obrigatório;
- memória persistente;
- execução automática de ferramentas;
- deployment real em `ENV-OTHER`.

Um E2E direto com provider real permanece uma validação opcional de compatibilidade, não uma condição retroativa para o fechamento já concluído.

## Regra de segurança

Nenhuma evolução pública deve importar automaticamente:

- código-fonte privado;
- prompts privados completos;
- estados reais;
- checkpoints reais;
- caminhos ou hashes operacionais internos;
- histórico bruto;
- material sensível;
- comandos privados de governança;
- credenciais ou provider keys;
- dados pessoais.

A vitrine não deve afirmar produção, deployment universal ou equivalência entre ambientes além do que foi efetivamente validado.
