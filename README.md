# TradingView — faixa de cotações

Página estática que incorpora o widget **Ticker Tape** do TradingView. O conteúdo servido é um único [index.html](index.html), sem aplicação de servidor, banco de dados ou etapa de compilação.

**Página publicada:** [viczk.github.io/TradingView](https://viczk.github.io/TradingView/).

## Conteúdo

O HTML configura os seguintes símbolos no widget externo:

| Símbolo | Par exibido |
| --- | --- |
| `BINANCE:BTCBRL` | Bitcoin / real |
| `FX_IDC:USDBRL` | Dólar americano / real |
| `FX_IDC:EURBRL` | Euro / real |
| `FX_IDC:GBPBRL` | Libra esterlina / real |

A configuração atual usa tema claro, disposição adaptável, logotipos e idioma inglês. O JavaScript e os dados são fornecidos pelo TradingView; disponibilidade e atualização das cotações dependem desse serviço. Este repositório apenas incorpora a apresentação e não calcula preços nem executa operações financeiras.

## Executar e alterar

Abra `index.html` em um navegador com acesso à internet ou sirva a pasta com um servidor estático. Por exemplo, com Python instalado:

```bash
python -m http.server 8000
```

Depois, acesse `http://localhost:8000`. Os símbolos e opções ficam no bloco JSON dentro do elemento `script` em `index.html`. Preserve a sintaxe JSON e confirme a renderização após editar.

Não há dependências npm, build ou suíte de testes própria. Uma verificação útil inclui a resposta HTTP da página, integridade do HTML, carregamento do script externo, console do navegador e apresentação em telas estreitas e largas. A resposta HTTP por si só não comprova a disponibilidade das cotações.

## Publicação e organização

Em 06/11/2026, o GitHub Pages está configurado para publicar a raiz da branch `main`. Um push nessa branch pode iniciar uma nova publicação, inclusive quando altera somente documentação. Antes de mudar `index.html`, registre a revisão anterior para permitir reversão e confira o resultado na URL pública.

O nome [`VicZk/TradingView`](https://github.com/VicZk/TradingView) foi mantido para preservar o endereço do Pages e possíveis incorporações externas. No catálogo geral, este é um projeto web estático independente; não é parte do Telegram Stock Bot nem de outro sistema de investimentos. Esta inclusão do README mantém `index.html` intacto.
