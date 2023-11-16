# Jmeter
Meu Script de Performance com JMeter
Este é o meu repositório contendo um script de teste de desempenho criado com o Apache JMeter. O objetivo é simular e avaliar a compra de passagem aérea no site www.blazedemo.com.

Passo 1: Configuração do Teste
Adicionei um Plano de Teste:
Abri o JMeter e criei um novo Plano de Teste.

Adicionei um Grupo de Threads (Thread Group):
Cliquei com o botão direito no Plano de Teste -> Adicionar -> Threads (Usuários) -> Grupo de Threads (Thread Group).

Configurei o número de usuários simultâneos, a duração do teste e o loop count conforme necessário.

Passo 2: Configuração da Requisição HTTP
Adicionei um Sampler HTTP Request:
Dentro do Grupo de Threads, cliquei com o botão direito -> Adicionar -> Sampler -> Requisição HTTP.

Configurei o nome do servidor (www.blazedemo.com) e o caminho para a compra de passagem aérea.

Passo 3: Adição de Elementos de Medição
Adicionei um Controlador de Grupos de Transações:
Cliquei com o botão direito no Sampler HTTP Request -> Adicionar -> Controladores -> Grupos de Transações.

Isso ajudará a medir o tempo de resposta do cenário como um todo.

Adicionei um Contador de Respostas Bem-Sucedidas:
Cliquei com o botão direito no Grupo de Transações -> Adicionar -> Elementos de Medição -> Contador de Respostas Bem-Sucedidas.

Isso ajudará a rastrear o número de transações bem-sucedidas.

Passo 4: Configuração de Relatórios e Tempo de Espera
Adicionei um Listener de Relatório Resumo:
Cliquei com o botão direito no Plano de Teste -> Adicionar -> Elementos de Resultado -> Relatório Resumo.

Isso fornecerá estatísticas úteis após a execução.

Adicionei um Temporizador Constant Throughput:
Cliquei com o botão direito no Grupo de Threads -> Adicionar -> Temporizadores -> Temporizador Constante (Constant Throughput Timer).

Configurei o valor para alcançar a taxa desejada de 250 requisições por segundo.

Passo 5: Configuração de Assertions (Opcional)
Adicionei Assertions (se necessário):
Para verificar se a compra foi bem-sucedida, adicionei um Assertion Response para validar o conteúdo da resposta.

Passo 6: Execução e Análise
Executei o Teste:
Salvei o Plano de Teste e o executei.

Analisei os Resultados:
Após a execução, analisei os resultados nos listeners, especialmente o Relatório Resumo e o Gráfico de Transações.

Passo 7: Ajustes
Ajustei para Atender ao Critério de Aceitação:
Ajustei o número de usuários, o tempo de espera e outros parâmetros para atender ao critério de aceitação.
