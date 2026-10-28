# Infográfico cartográfico interativo — Saudades (SC)

Protótipo para o infográfico cartográfico do TCC. Inclui mapa 3D com marcador da CEI Pró-Infância Aquarela e uma janela interativa para consultar a planta geral da página 59 do arquivo `PROJETO CEI AQUARELA 4.pdf`.

## Conteúdo

- `index.html`: mapa, marcador, pop-up, janela da planta e alternância entre a reconstrução editorial de 2021 e o projeto atual.
- `data/locais.geojson`: coordenada e conteúdo do marcador da creche.
- `assets/planta-pagina-59.png`: imagem da página 59 usada como planta-base.

## Como funciona a planta

Ao clicar no marcador da CEI Pró-Infância Aquarela, selecione **Explorar planta da creche**. Dentro da janela, alterne entre **Configuração de 2021** e **Projeto atual (página 59)**. Clique na imagem para ampliar/reduzir e use a rolagem para examinar detalhes.

A configuração de 2021 é uma reconstrução editorial baseada na informação fornecida para o infográfico: na área onde hoje está o parquinho, ficavam a Creche II e o Sanitário da Creche II, posteriormente demolidos para dar lugar ao parquinho. Os demais espaços seguem a planta da página 59. O protótipo não altera graficamente os traços da planta original para redesenhar esses ambientes; a diferença está descrita no painel de contexto. Não apresentar a reconstrução como uma planta original de 2021.

## Como testar localmente

Na pasta do projeto, execute:

```bash
python -m http.server 8000
```

Abra `http://localhost:8000`. Abrir o HTML diretamente por `file://` pode impedir o carregamento do GeoJSON.

## Publicar no GitHub Pages

1. Faça backup do repositório atual.
2. Copie `index.html`, `data/` e `assets/` para a pasta publicada, mantendo essa estrutura.
3. Faça commit e push e aguarde a publicação.
4. Teste o mapa e a janela da planta em desktop e celular.

O mapa depende de serviços externos (MapLibre GL JS e OpenFreeMap) e de conexão à internet. Os edifícios 3D dependem dos dados disponíveis no mapa-base e não devem ser tratados como um modelo arquitetônico preciso da creche.
