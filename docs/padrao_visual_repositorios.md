# Padrão Visual de Repositórios — MLI-Knot / Tendoshk

Este documento registra o padrão visual recomendado para as superfícies públicas do ecossistema **MLI-Knot / Tendoshk**.

## Banner padrão

Cada repositório público deve manter sua própria cópia local do banner aprovado em:

```text
assets/matrix-inspired-banner.gif
```

No `README.md`, a referência recomendada é relativa ao próprio repositório:

```md
<div align="center">

<img src="assets/matrix-inspired-banner.gif" width="100%" alt="Cyber banner" />

</div>
```

Uma forma Markdown simples também pode ser usada:

```md
![Cyber banner](assets/matrix-inspired-banner.gif)
```

## Regra de autonomia

O banner não deve ser servido por hotlink a partir de outro repositório do ecossistema.

Cada superfície pública mantém uma cópia local byte-idêntica do asset aprovado. Nenhum showcase deve funcionar como CDN, origem binária ou autoridade de disponibilidade para os demais.

A identidade visual compartilhada depende da igualdade do asset aprovado, não de uma dependência entre repositórios.

## Escopo

Este padrão é visual e documental.

Ele não autoriza alteração de código, workflows, segredos, governanças privadas, checkpoints reais, conteúdo operacional interno ou material sensível.

## Objetivo

Criar unidade visual entre as superfícies públicas do ecossistema sem quebrar sua autonomia nem a separação entre camadas públicas, privadas, sensíveis, pausadas e experimentais.
