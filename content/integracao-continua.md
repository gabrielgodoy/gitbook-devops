# Continuous integration (Integração contínua)

A CI ajuda com os objetivos de eficiência em nosso desenvolvimento, implantação, pipeline operacional e o objetivo de um software de qualidade.

O CI é um processo onde os desenvolvedores confirmam seu código ao longo do dia para um repositório compartilhado e cada commit é automaticamente construído e testado, e os resultados são enviados aos desenvolvedores. Ao criar e testar automaticamente cada commit, você pode identificar erros imediatamente.

Segue algumas etapas de um bom CI

- Ambientes espelhados
- Versionamento
- Hooks/Linters
- Migrations
- Testes
- Build

## Ambientes espelhados
O objetivo é deixar o seu ambiente de desenvolvimento mais próximo do ambiente de produção, assim evitamos o velho problema “Mas na minha maquina esta funcionando”

[Docker](https://www.docker.com/) ou Virtualização são boas ferramentas para este fim


## Versionamento
Algumas dicas para um bom uso de versionamento

- commits de pequenas mudanças
- usar um plugin ou convenção para ajudar a organizar melhor o histórico do repositório, git flow é um bom exemplo disso
- Hooks de pre e pós commit rodando teste e requisitos necessários
- [Versionamento Semântico](http://semver.org/lang/pt-BR/#versionamento-semntico-200)

## Git Hooks
Hooks do Git são úteis para rodar scripts de `pre-commit` e `pre-push` a fim de verificar a qualidade do código escrito. 

## Linters de código
Linters como [eslint](http://eslint.org/) [stylelint](https://github.com/stylelint/stylelint) [pycodestyle](https://pypi.python.org/pypi/pycodestyle) definem padrões que todo desenvolvedor deve seguir ao escrever seu cógigo. Dessa forma é possíve lter um código uniforme entre todos os membros da equipe, facilitando a leitura do mesmo.

## Migrations
Temos de ter todo um cuidado especial aqui uma boa dica é ler toda a documentação [django migrations](https://docs.djangoproject.com/en/1.9/topics/migrations/)

## Testes

### Testes de unidade:
> Práticas como TDD e refatoração dão bastante ênfase nesse tipo de teste, que exercita unidades de código isoladamente sem a necessidade de subir e aplicação inteira. Esses testes geralmente rodam bem rápido – na ordem de milissegundos – podendo ser executados com bastante frequência e fornecendo o melhor tipo de feedback para os desenvolvedores.

### Testes de integração ou testes de componente:
> Exercitam uma parte da aplicação ou como ela se integra com suas dependências, por exemplo: um banco de dados, um serviço REST, uma fila de mensagens, ou até mesmo os frameworks e bibliotecas utilizados. Dependendo do componente que está sendo testado, a execução desses testes podem exigir que partes do sistema estejam rodando.

### Testes funcionais ou testes de aceitação:
> Exercitam as funcionalidades do sistema como um todo, do ponto de vista externo. Geralmente este tipo de teste exercita a interface gráfica ou simula a interação com o sistema do ponto de vista de um usuário. Esses testes geralmente são mais lentos pois exigem que a maior parte do sistema esteja rodando.

## Build

O processo de Build é prepara o código para ser entregue em qualquer ambiente seja ele Produção, Teste, homologação ou qualquer outro ambiente.

Este processo se beneficia muito da automação um dos fundamentos da cultura DevOps

Algumas ferramentas para automatizar este processos:

- [Jenkins](https://jenkins.io/)
- [Travis CI](https://travis-ci.org/)
- [TeamCity](https://www.jetbrains.com/teamcity/)




