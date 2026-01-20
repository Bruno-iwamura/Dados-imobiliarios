🏠 Real Estate Data Pipeline & Analytics

Este projeto demonstra a construção de um pipeline de dados completo (End-to-End), desde a extração de dados brutos, passando por um processo de ETL robusto entre diferentes ecossistemas de bancos de dados (PostgreSQL e SQL Server), até a entrega de insights estratégicos via Power BI.

🎯 Objetivos
Processar e limpar uma base de dados imobiliária com mais de 10 mil registros.

Demonstrar a interoperabilidade entre diferentes bancos de dados relacionais.

Criar indicadores de performance (KPIs) para análise de mercado imobiliário brasileiro.

🛠️ Stack Tecnológica
Linguagem: Python 3.10

Bibliotecas: Pandas, SQLAlchemy, PyODBC, Psycopg2.

Bancos de Dados: PostgreSQL (Origem) e Microsoft SQL Server 2022 (Destino).

BI: Power BI (DAX e Modelagem).

⚙️ Arquitetura e Fluxo (ETL)
Ingestão: Extração de dados de arquivos CSV com tratamento de encoding (Latin-1).

Tratamento (Python): Limpeza de dados nulos, normalização de strings e correção de tipos de dados (Casting).

Migração Multi-DB: Script automatizado que extrai dados do PostgreSQL e injeta no SQL Server 2022, garantindo a integridade dos schemas.

🛡️ Desafios Técnicos & Soluções (Troubleshooting)
Como diferencial de engenharia, este projeto superou obstáculos reais de infraestrutura:

Conectividade: Configuração de protocolos TCP/IP e Named Pipes no SQL Server Configuration Manager para permitir conexões externas via Python.

Segurança e Drivers: Implementação do driver ODBC 17 e gerenciamento de permissões de acesso ao banco.

Qualidade do Dado: Tratamento de inconsistências estruturais e remoção de registros nulos que impactariam o cálculo do Ticket Médio.

📊 Insights do Dashboard
O relatório final foca em métricas de decisão:

Ticket Médio por Estado: Identificação de regiões com maior valorização.

Média de Preço por m²: KPI fundamental para comparação de custo-benefício.

Distribuição por Categoria: Segmentação entre imóveis de padrão Econômico, Médio e Luxo.

🚀 Como Executar este Projeto
Clone o repositório.

Certifique-se de ter o PostgreSQL e o SQL Server 2022 instalados.

Instale as dependências:

Bash

pip install pandas sqlalchemy pyodbc psycopg2

Configure suas credenciais no script de migração (utilize variáveis de ambiente por segurança).

Abra o arquivo .pbix na pasta /dashboard para explorar os dados.