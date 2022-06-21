## Introdução  

**Arquitetura** é um conhecimento compartilhado por desenvolvedores experientes sobre como organizar um sistema de software.  
  
Existem padrões de arquitetura específicos para problemas específicos, mas, uma coisa que podemos ver quase sempre, independente da arquitetura utilizada, é a divisão de responsabilidades por camadas.  

**Regras de negócio**  
  
Regras de negócio definem ou restringem algum aspecto de um negócio. São elas que definem como o negócio deve se comportar, quando uma ação deve ser tomada e etc. As regras de negócio devem ser muito bem definidas e documentadas, pois guiam as tomadas de decisões e moldam processos. A princípio, as regras de negócio podem ser executadas manualmente, mas tem se tornado cada vez mais comum automatizá-las com a ajuda de sistemas de software.  
  
Naturalmente, em sistemas de software, as regras de negócio se traduzem em códigos que controlam o comportamento dessas aplicações.

**Arquitetura MSC**  
  
Podemos definir as três camadas das seguintes formas:  
**Camada de Modelo (M)**: Arquivos onde iremos executar as operações do banco de dados, como criar conexões e executar queries.  
  
**Camada de Serviço (S)**: Arquivos onde iremos estruturar nossas regras de negócio, geralmente é quem chama os métodos definidos na camada de modelo.  
  
**Camada de Controladores (C)**: Interface mais próxima da pessoa usuária ou de uma requisição, irá processar e chamar as devidas funções da camada de serviço.
A imagem abaixo ilustra essa arquitetura.  
  
*_Obs.: Algumas vezes a camada de Controladores pode se comunicar direto com a camada de Modelo, dispensando o uso da camada de Serviço, principalmente em situações em que não temos uma regra de negócio tão complexa._*