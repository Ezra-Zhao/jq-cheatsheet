# Cola de referência do jq · jq Cheatsheet

> 🌍 [中文](README.md) · [Español](README.es.md)

Uma **cola de uma página só** para jq: 30 filtros verificados um por um com dados reais (testados no jq 1.7). Cada entrada responde a apenas três perguntas — **o que faz, um comando pronto para copiar e colar, e etiquetas de uso**. Sem funções inventadas nem sintaxe improvisada.

## Para quem é

Para desenvolvedores backend, engenheiros SRE/DevOps e qualquer pessoa que lide com JSON todo dia. Se toda vez que você analisa a resposta de uma API precisa pesquisar a sintaxe do jq, esta cola ajuda a memorizar os filtros mais usados de uma vez.

## Como usar

1. Vá direto ao **[CHEATSHEET.md](CHEATSHEET.md)** — o corpo da referência; os filtros em inglês qualquer desenvolvedor entende.
2. Instale o jq primeiro: `brew install jq` no macOS, `sudo apt install jq` no Debian/Ubuntu.
3. Salve o `config.json` de exemplo no final da página e rode cada filtro na mão: em uma hora você domina.

## O que está incluído

| Categoria | Conteúdo |
|---|---|
| 📥 Básico | Formatação legível, extrair campos, saída crua com `-r`, saída compacta com `-c` (4) |
| 🧭 Aninhados e arrays | Caminhos profundos, índices, expansão com `.[]`, contagem com `length` (4) |
| 🔎 Filtragem | `select` por número, por texto e com condições combinadas (3) |
| 🔄 Transformação | `map` para extrair campos, remodelar objetos e adicionar campos calculados (3) |
| 🔗 Pipes e construção | Encadear com `|`, sintaxe curta `{a, b}`, montar objetos de resumo (3) |
| 🔤 Strings e números | `tostring`/`tonumber`, `split`/`join`, regex com `test()` (3) |
| 📊 Agregação | Ordenar, deduplicar, agrupar e contar, somar, máximo/mínimo (5) |
| 🗝️ Chaves | `keys`/`has`/`del` (1) |
| 🛠️ Casos reais | `curl \| jq`, estatísticas de logs, `--arg` para variáveis do shell, `--slurp` (4) |

Cada filtro foi executado com jq 1.7 sobre dados reais; os exemplos de entrada e saída estão nos comentários.

## Por que estes 30

- **Frequência primeiro**: cada categoria cobre comandos que realmente se digitam no dia a dia; nada de funções exóticas que ninguém usa.
- **Fechamento prático**: os últimos 4 são cenários reais de produção (consumir APIs, ler logs, passar variáveis), prontos para usar.

## Contribuições são bem-vindas

Achou um filtro errado, um caso de uso faltando ou uma tradução a melhorar? *Pull requests* são bem-vindos. Mantenha o formato de cada entrada (o que faz / comando / etiquetas) e **rode cada filtro com jq de verdade antes de enviar**.

## Licença

MIT © 2026 Guangyi Zhao. Veja [LICENSE](LICENSE).
