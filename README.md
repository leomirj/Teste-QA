# Testes de API e Desempenho do ViaCEP

Este repositório contém uma coleção do Postman e testes de desempenho configurados no JMeter para a API do ViaCEP. O objetivo é validar o comportamento e o desempenho do serviço de consulta de CEPs.

## Estrutura do Repositório

- **postman_collection.json**: Coleção do Postman com requisições para testar os diferentes endpoints da API ViaCEP.
- **jmeter_test_plan.jmx**: Plano de teste do JMeter para avaliar o desempenho da API sob diferentes cargas de usuários.

## Pré-requisitos

- **Postman**: Para importar e executar a coleção de testes.
- **Apache JMeter**: Para executar os testes de desempenho.

## Configuração

### Postman

1. **Importar a Coleção**:
   - Abra o Postman.
   - Clique em "Import" no canto superior esquerdo.
   - Selecione o arquivo `postman_collection.json` deste repositório e importe-o.

2. **Executar Testes**:
   - Navegue até a coleção importada no Postman.
   - Use o "Collection Runner" para executar os testes.

### JMeter

1. **Abrir o Plano de Teste**:
   - Inicie o JMeter.
   - Vá em "File" > "Open" e selecione o arquivo `jmeter_test_plan.jmx`.

2. **Executar Testes de Desempenho**:
   - Ajuste os parâmetros de carga conforme necessário (número de threads, ramp-up, etc.).
   - Clique no botão de start (verde) para iniciar o teste.
   - Revise os resultados usando os listeners configurados, como "View Results Tree" e "Summary Report".

## Testes Implementados

### Postman

- **Consulta CEP Valido**: Testa o endpoint `/ws/{cep}/json/` para confirmar o retorno correto de dados para um CEP válido.
- **CEP Inválido**: Valida a resposta da API para um CEP malformado ou inexistente.
- **Requisições Simultâneas**: Simula múltiplas requisições para garantir estabilidade sob carga leve (usando o Collection Runner).

### JMeter

- **Desempenho Sob Carga**: Avalia o tempo de resposta e a taxa de erros com diferentes volumes de usuários simultâneos.
- **Resiliência e Estabilidade**: Testa a capacidade da API de tratar grandes quantidades de requisições sem falhas.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests para melhorias ou correções.

## Licença

Este projeto está licenciado sob a MIT License - veja o arquivo [LICENSE](LICENSE) para mais detalhes.


