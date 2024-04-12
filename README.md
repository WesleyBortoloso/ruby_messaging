# Relatório de uso do RabbitMQ como message broker 

### Linguagem utilizada: *Ruby*
Ruby foi escolhida como a linguagem utilizada para implementar o producer e o consumer por conta de ser a linguagem a qual tenho maior familiaridade. Além disso a implementação do producer e do consumer foi facilitada por conta de sua sintaxe agradável e enxuta.

### Código
O código em si é relativamente simples, utilizamos da gem Bunny para facilitar a comunicação com o RabbitMQ então a primeira coisa a se fazer em ambos os códigos é inicializar a comunicação e executar os processos para localização da fila.

#### Producer: 
O producer foi chamado de send para facilitar o entendimento, basicamente o producer é responsável por produzir e enviar as mensagens, no código ele está publicando uma mensagem na fila previamente imposta, após publicar a mensagem ele fecha a conexão.

#### Consumer:
O consumer que foi chamado de receive é onde as mensagens enviadas pelo producer devem chegar, para que isso aconteça, no código temos uma estrutura de rescue para garantir que se um erro ocorra no meio do caminho ele será minimamente tratado, no entanto, enquanto um erro não aconteça, o consumer vai "entrar" na fila previamente imposta e vai executar um bloco de código caso algo entre na fila, nesse caso vai apenas exibir a mensagem recebida.

### Conclusão:
O RabbitMQ possui uma excelente documentação para dar os primeiros passos utilizando o message broker, nenhuma dificuldade foi encontrada para executar esse exemplo de código, além das várias possibilidades que podem ser implementadas.
