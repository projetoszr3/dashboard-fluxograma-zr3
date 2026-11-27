# Dashboard – fluxo de execução de obra (ZR3)

Protótipo navegável do sistema de checklists com o fluxo de execução de obra e o dashboard **Execução da obra** (P11 - Residencial Artus). É um arquivo único, `index.html`, que funciona no computador e no celular, sem instalar nada e sem internet: a biblioteca 3D, a geração de PDF e a fonte já estão dentro do arquivo.

## Como abrir

- **Computador:** baixe o `index.html` e abra no navegador (Chrome ou Edge).
- **Celular:** abra o `index.html` no navegador. No Chrome (Android) ou no Safari (iPhone), *Adicionar à tela inicial* cria um atalho que abre em tela cheia.
- **GitHub Pages:** em *Settings → Pages*, escolha *Deploy from a branch*, branch `main`, pasta `/ (root)`. Em repositório privado, o Pages exige plano pago do GitHub; o link gerado fica acessível a quem o tiver, salvo se a organização restringir o acesso.

## O que tem

- **Dashboards → Execução da obra**, com seletor de obra, controle de data (−7 d, +7 d, Reproduzir; velocidades 1x a 16x na segunda linha) e quatro abas:
  - **Por apartamento:** matriz estágio × apartamento, resumo por pavimento e destaque de fora de sequência e NC.
  - **Fluxograma:** linha de balanço num quadro ao lado do título e dos indicadores (abaixo deles em telas estreitas) (clicar numa linha, no cabeçalho de um estágio ou na barra de pendentes destaca o estágio nos dois; *Ver completa* abre a aba Avanço e previsão), três modos (Frente, Último concluído e Em andamento) e “Planejado até”.
  - **Avanço e previsão:** curva de avanço, ritmo por fornecedor, linha de balanço e previsão por pavimento.
  - **Modelo 3D:** onze análises, entre elas *Número do estágio* (cada apartamento na cor do estágio da sua frente, uma cor para cada um dos 28 estágios, em escala do vermelho ao violeta; clicar num número da legenda mostra a empreiteira e os apartamentos por pavimento daquele estágio, com opção de isolar esses pavimentos), NC pendente em escala de vermelho pela idade da NC mais antiga e % concluído em escala de verde.
- **Configurações:** fornecedores com cor, estágios do grupo OBRAS, fluxo e planejamento por obra, e cadastro de plantas para o 3D.
- **Sobre:** as regras de cálculo e, em *Ver JSON*, a estrutura de dados sugerida.

## Celular

- O menu lateral vira uma gaveta, aberta pelo botão no canto superior esquerdo.
- As tabelas rolam na horizontal.
- O fluxograma fica em duas colunas.
- No 3D, as opções ficam num painel recolhível (*Opções*). Um dedo gira o modelo, a pinça dá zoom e dois dedos movem. "Isolar pavimentos" aceita vários pavimentos de uma vez.
- O desenho das plantas (Empreendimentos → Plantas) foi pensado para computador, com mouse.

## Dados

- Status dos checklists lido dos painéis BRUTO e ACABAMENTOS - OBRAS - ARTUS em 27/11/2026 às 15:15 (conferido com a API: nenhuma divergência).
- São 59 checklists de apartamento (A-01 a A-59), com a impermeabilização separada em parede (A-27) e piso (A-38).
- Plantas do 3D importadas do Revit (ambientes_export.json). A casca do Revit (fachada e esquadrias) não vai neste repositório público; ela está só na versão interna do protótipo.
- O arquivo traz dados reais da obra (códigos das unidades, datas e NCs), sem nomes de proprietários. Este repositório é público.

## Atualizar

O `index.html` é gerado pelo script de montagem do protótipo. Para atualizar, substitua o arquivo e faça o commit.
