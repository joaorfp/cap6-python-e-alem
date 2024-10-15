# Sistema de Monitoramento de Estoque e Previsão de Demanda para Insumos Agrícolas

## Visão Geral

O sistema desenvolvido visa facilitar a gestão de insumos agrícolas para empresas do agronegócio. Ele é projetado para monitorar o estoque de sementes, fertilizantes, defensivos e outros insumos, ao mesmo tempo que prevê a demanda futura com base em dados históricos. Essa solução permite que as empresas otimizem sua logística, evitem o desperdício e a falta de insumos, e melhorem a eficiência das operações.

## Problema a Ser Resolvido

Empresas do agronegócio enfrentam desafios relacionados ao controle de estoque de insumos essenciais, como sementes e fertilizantes, o que pode resultar em excesso ou escassez de materiais. A má gestão desses recursos pode levar a perdas financeiras e operacionais, como desperdício de insumos e atrasos na produção.

O objetivo deste sistema é oferecer uma solução que automatize o controle de entradas e saídas no estoque e faça previsões sobre as necessidades futuras de insumos com base em padrões de uso anteriores.

## Funcionalidades do Sistema

- **Registro de Entradas e Saídas**: O sistema permite registrar todas as movimentações de estoque de insumos, garantindo um controle eficiente e atualizado dos materiais disponíveis.
  
- **Previsão de Consumo**: Através da análise de dados históricos, o sistema gera previsões de demanda futura para os insumos, facilitando o planejamento de compras e evitando problemas de falta ou excesso de materiais.

- **Armazenamento de Dados**: O sistema utiliza estruturas de dados eficientes, como listas, tuplas e dicionários, para manipulação e organização das informações sobre os insumos.

- **Exportação e Importação de Dados**: Os dados podem ser exportados e importados em formatos como JSON ou arquivos de texto, permitindo fácil integração com outros sistemas e manipulação dos dados.

- **Conexão com Banco de Dados Oracle**: Para garantir a persistência dos dados e facilitar a escalabilidade do sistema, as informações de estoque e as previsões de demanda são armazenadas em um banco de dados Oracle. Isso permite que o sistema opere de forma confiável e acessível.

## Estrutura do Código

O código está dividido nas seguintes partes principais:

1. **Conexão com o Banco de Dados**: 
   Utilizamos a biblioteca `cx_Oracle` para se conectar a um banco de dados Oracle, onde todas as operações de entrada e saída de insumos, bem como as previsões de demanda, são persistidas.

2. **Criação de Tabelas**: 
   Um script SQL cria as tabelas necessárias no banco de dados para armazenar as informações sobre as operações de colheita e movimentação de insumos.

3. **Registro de Operações**: 
   O sistema permite registrar manualmente a entrada e saída de insumos no estoque, com validações para garantir a entrada correta dos dados.

4. **Previsão de Demanda**: 
   A partir de dados históricos, o sistema calcula a previsão de demanda futura para diferentes insumos, facilitando o planejamento logístico e financeiro.

5. **Manipulação de Arquivos JSON**: 
   Implementamos funções para exportar os dados do banco de dados para arquivos JSON e, caso necessário, carregar dados de arquivos JSON para o banco de dados, garantindo flexibilidade na gestão dos dados.

## Instalação e Execução

Para rodar o sistema, siga os passos abaixo:

1. **Crie um ambiente virtual**:
```bash
python -m venv env && source ./env/bin/activate
```

2. **Instale as dependências**:
   - Python 3.x
   - cx_Oracle (`pip install cx_Oracle`)
   - As bibliotecas `datetime` e `json` são nativas do Python.

3. **Configuração do Banco de Dados Oracle**:
   Certifique-se de ter uma instância do Oracle configurada corretamente em sua máquina ou na nuvem. Utilize as credenciais adequadas para conectar-se ao banco de dados.

4. **Execução**:
   Execute o arquivo principal (`menu.py`) para iniciar o sistema e interagir com o menu de opções para registrar operações, analisar perdas, gerar recomendações, exportar ou importar dados, e criar as tabelas necessárias.

```bash
python main.py
```
