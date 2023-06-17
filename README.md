# digitalsys
Desafio técnico para concorrer a uma vaga na empresa DigitalSys Tecnologia

Descrição do desafio: https://github.com/DigitalsysTecnologia/challenge-dev-django

## Sistema de Gestão de Propostas de Empréstimo Pessoal

Este é um desafio técnico para criar um sistema de gestão de propostas de empréstimo pessoal utilizando a seguinte stack:

    Django
    Django Rest Framework
    Django Celery
    RabbitMQ
    Docker compose

### Objetivo do Desafio

O objetivo deste desafio é criar um sistema onde os usuários possam cadastrar propostas de empréstimo pessoal e realizar sua avaliação através de uma fila RabbitMQ utilizando o Django Celery.
Estrutura da Proposta


### Casos de uso (stories)

[1] Como administrador do sistema, desejo cadastrar os campos que devem constar na proposta através do django-admin.

[2] Como cliente, quero acessar a página de preenchimento da proposta, para que possa solicitar um empréstimo.
(Após o preenchimento da proposta, a API deve registrar as informações no banco de dados e enviar a proposta para uma fila RabbitMQ. O Django Celery será responsável por avaliar a proposta, atribuindo um status de "Negada" ou "Aprovada". Para fins de teste, desenvolva um algoritmo onde metade das propostas serão negadas e metade serão aprovadas. Após a avaliação, o Django Celery deverá atualizar o status da proposta no banco de dados.)

[3] Como administrador do sistema, desejo visualizar no django admin as propostas cadastradas e seus status de aprovação (Aprovada ou Negada).


Requisitos da Entrega do Projeto

Para a entrega do projeto, certifique-se que tudo esteja em ambiente docker, preferencialmente, crie um docker-compose.yaml para que o projeto seja executado do modo mais simples possível, não se esqueça também dos seguintes detalhes

    [] Crie um README com as orientações para executar seu projeto
    [] Crie um usuário / senha padrão para o admin do sistema
    [] Caso algo em seu código não esteja inteligível, por favor, comente o trecho, imagine que outras pessoas darão manutenção no sistema

O que será avaliado no seu código

    Organização do código
    Separação de responsabilidades e manutenabilidade do sistema
    Bom funcionamento e performance

O que NÃO será avaliado no seu código

    Layout do front-end
    CSS
    Habilidade com Javascript (conseguindo realizar as chamadas à API estará 'good enough')

