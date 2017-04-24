# Continuous delivery (Entrega contínua)
Com o processo de desenvolvimento mais ágil, é possível entregar melhorias ao usuário final, e responder a demandas de mercado muito mais rápido.

O cenário ideal seria apertar um botão e entregar seu código onde quiser (Ambiente de homologação, teste ou produção).

A entrega contínua deve começar pela implantação (deploy) do software em um ambiente de teste que espelhe a produção.

O desenvolvedor após desenvolver uma nova funcionalidade ou produto deverá subir esse novo código para o ambiente de testes. Deverá então ser executados os testes de aceitação automatizados ou testes de regressão para garantir que nenhuma nova mudança de código quebrou as funcionalidades existentes. Casos os estes teste falhem o processo deve parar. O desenvolvedor deve ser notificado automaticamente. Caso os testes de aceitação passem, todos os testes não-funcionais automatizados devem ser executados.

Testes de Carga e de segurança pode sem executados nessa etapa também.

Caso a bateria de testes não detecte nenhum problema, o novo código estará pronto para ser incoporado ao ambiente de produção.


## Métodos de implantação (deploy)

### Entrega azul / verde
As cores Azul e Verde são apenas marcadores de posição para representar um grupo de servidores. A estratégia azul/verde ajuda a subir uma nova atualização, minimizando o tempo de inatividade. Você tem dois ambientes, chamados verde e azul. E você tem um roteador para escolher qual está online.


### Servidor Canário

Um Servidor Canário funciona como um canário das minas de Carvão, é um servidor onde colocamos uma certa porcentagem do trafego apenas para verificar seu comportamento e verificar se o novo release sobrevive.

Ferramentas para ajudar neste processo:
- [Ansible](https://www.ansible.com/)
- [Chef](https://www.chef.io/)
- [Puppet](https://puppet.com/)
