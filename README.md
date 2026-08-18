# DevEx Marketplace

Afya DevEx Marketplace — uma coleção de skills, plugins, workflows e ferramentas de produtividade para desenvolvedores de software que utilizam Claude Code, Cursor e GitHub Copilot.

Desenvolvido pelo time de Developer Experience (DevEx) da Afya.

## Instalação

### Claude Code

Adicione este marketplace ao Claude Code:

```bash
/plugin marketplace add iclinic/devex-marketplace
```

### Cursor

1. Acesse o [Painel de Plugins do Cursor](https://cursor.com/dashboard/plugins)
2. Importe `iclinic/devex-marketplace` como um marketplace de equipe

Para instalar um plugin, clique nele no painel e depois clique em **Add to Cursor** para instalá-lo diretamente pela IDE desktop do Cursor.

### GitHub Copilot

Adicione este marketplace ao GitHub Copilot:

```bash
copilot plugin marketplace add iclinic/devex-marketplace
```

## Plugins Disponíveis

### Afyapowers (Core)

Um plugin de workflow de desenvolvimento determinístico e com fases controladas, derivado do superpowers. Impõe desenvolvimento estruturado de funcionalidades com estado persistente, continuidade de sessão e rastreabilidade completa.

**Repositório:** https://github.com/iclinic/afyapowers

**O que você obtém:**
- Workflow de desenvolvimento estruturado e com fases controladas
- Estado persistente e continuidade de sessão
- Rastreabilidade completa para desenvolvimento de funcionalidades

---

## Canais de Release

O afyapowers é publicado em dois canais, como entradas de plugin separadas no mesmo
marketplace, apontando para refs diferentes do repositório do plugin.

| Canal | Plugin | Ref do source | Plataformas | Para quem |
| :---- | :----- | :------------ | :---------- | :-------- |
| Stable | `afyapowers` | tag `v1.7.1` (fixa) | Claude Code, Cursor, GitHub Copilot | Uso geral. Só muda quando uma nova tag é publicada aqui. |
| Latest | `afyapowers-latest` | branch `master` | **Apenas Claude Code** | Early access. Acompanha o desenvolvimento contínuo. |

O canal Latest é exclusivo do Claude Code — ele existe apenas em
`.claude-plugin/marketplace.json`. Cursor e GitHub Copilot recebem somente o canal
Stable.

### Instalando o canal Latest (Claude Code)

```bash
/plugin marketplace add iclinic/devex-marketplace
/plugin install afyapowers-latest@devex-marketplace
```

> **Instale apenas um dos dois.** Os dois canais entregam as mesmas skills, então
> ter `afyapowers` e `afyapowers-latest` habilitados ao mesmo tempo duplica
> comandos e agentes. Para trocar de canal, desinstale o outro primeiro.

### Publicando no canal Latest

O canal Latest só entrega atualização quando a **versão resolvida muda**. O
afyapowers declara `version` no seu próprio `plugin.json`, e esse valor tem
precedência sobre o marketplace — por isso a entrada `afyapowers-latest` aqui
**não** define `version`.

Consequência prática: novos commits em `master` com o mesmo `version` no
`plugin.json` **não** chegam aos usuários. Cada release do canal Latest precisa
bumpar o `version` do `plugin.json` no repositório do afyapowers (por exemplo
`1.6.0-rc.1`, `1.6.0-rc.2`).

### Promovendo Latest para Stable

1. Publique uma tag no repositório do afyapowers (ex.: `v1.6.0`).
2. Atualize `ref` e `version` da entrada `afyapowers` nos três arquivos de marketplace.

---

## Estrutura do Projeto

```
devex-marketplace/
├── .claude-plugin/
│   └── marketplace.json       # Catálogo de plugins do Claude Code
├── .cursor-plugin/
│   └── marketplace.json       # Catálogo de plugins do Cursor
├── .github/
│   └── plugin/
│       └── marketplace.json   # Catálogo de plugins do GitHub Copilot
└── README.md
```

## Contribuindo

Para adicionar um novo plugin ao marketplace, adicione a definição do plugin nos três arquivos de marketplace:

- `.claude-plugin/marketplace.json`
- `.cursor-plugin/marketplace.json`
- `.github/plugin/marketplace.json`

Cada plataforma possui um formato de source ligeiramente diferente. Consulte as entradas existentes como referência.

Plugins específicos de uma plataforma vão apenas no arquivo correspondente — é o caso
do canal Latest (`afyapowers-latest`), que existe só em `.claude-plugin/marketplace.json`.
Veja [Canais de Release](#canais-de-release).

## Licença

Uso interno — Afya.
