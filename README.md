# Teste de Performance com JMeter
Este repositório contém um script de teste de performance utilizando o Apache JMeter para testar a compra 
de passagem aérea no site https://www.blazedemo.com.

## Pré condição
1. Certifique-se de ter o JMeter instalado em sua máquina. Você pode baixar o JMeter em https://jmeter.apache.org/download_jmeter.cgi.
2. Abra o JMeter e importe o arquivo "script_compra_passagem.jmx" localizado neste repositório.
3. Execute o teste de carga e de pico:
Selecione o plano de teste "Compra de Passagem - Teste de Carga".
Clique em "Play" ou "Start" para iniciar a execução do teste.
Monitore as métricas de desempenho no JMeter durante a execução.

## Relatório de execução dos testes

Ao analisar os resultados do teste de performance, foi verificado que o percentil de 90th (ou 90º percentil) do tempo de resposta das requisições não foi aderente ao critério de aceitação estabelecido,
que era de ter um tempo de resposta inferior a 2 segundos.
Isso significa que pelo menos 90% das requisições tiveram um tempo de resposta superior a 2 segundos. Essa situação indica que o sistema não conseguiu atender aos requisitos de desempenho estabelecidos.

Detalhes da execução nos relatório: "Aggregate Report.png" e "Sumary Report.png"

Existem algumas possíveis razões para esse resultado:
1. Sobrecarga do servidor: O servidor pode não ter sido capaz de lidar com a carga de requisições simultâneas, resultando em atrasos no processamento e aumento do tempo de resposta.
2. Recursos insuficientes: O ambiente de teste pode não ter recursos suficientes, como capacidade de processamento, memória ou largura de banda de rede, para suportar a carga de requisições e fornecer tempos de resposta adequados.
3. Problemas de escalabilidade: O sistema pode não ter uma arquitetura escalável que permita lidar com um número crescente de requisições sem degradar o desempenho.
4. Problemas de otimização: Pode haver áreas no código do aplicativo ou no design da aplicação que estão causando gargalos e afetando o tempo de resposta.

Para solucionar esse problema e melhorar o desempenho do sistema, recomenda-se realizar uma análise mais detalhada dos resultados e investigar as possíveis causas dos tempos de resposta mais longos.
Isso pode envolver ajustes na configuração do ambiente de teste, otimização do código, escalabilidade da infraestrutura ou aprimoramentos na arquitetura do sistema.

## Como realizar commit no projeto
1. Abra o terminal e selecione o comando `git status` para verificar os arquivos alterados.
2. Adicione os arquivos desejados com o comando `git add "nome do arquivo"`
3. Commit através do comando `git commit -m "Texto sobre o que está sendo incluido/alterado`
4. Suba o projeto para o repositório com o comando `git push origin main`