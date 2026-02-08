# ⚕️Abstergo Industries

> Abstergo industries é uma organização com foco na distribuição de rémedios e produtos farmacêuticos em geral. 
> Ela atende a diversos clientes localizados nos estados brasileiros.  
> Por meio de suas operações B2B eficientes, a Abstergo industries busca cumprir a missão de garantir que seus clientes
> cumpram seus objetivos principais, promovendo  
> uma cadeia de valores compartilhado e o bem-estar de todas partes envolvidas. 
---

## 🌐RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS ☁

    Data: 01/03/2026  
    Empresa: Abstergo Industries  
    Responsável: Thiago Basilio

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por **Thiago Basilio**.  
O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos.  
Após um estudo levantado pela equipe de DevOps juntamente com a Governança de TI, e empresa optou como meta de curto  
e medio prazo, a migração de seus serviços para o ambiente cloud, na expectativa de flexibilizar e economizar com 
recursos computacionais   
garantindo também o foco no desenvolvimento de seus negócios com o intuito de entregar maior valor aos seus clientes.    

---
## Descrição do Projeto

Para o inicio da migração, aplicaremos a estratégia de **Rehost**(Lift-and-Shift) no ambiente de Desenvolvimento/Testes    
nos serviços web de alto impacto no négocio que serão descritos a seguir nas etapas do projeto.  
**Observação:** escolhemos os serviços de alto impacto devido a urgência e escolha do ambiente(Desenvolvimento/Testes) 

Com foco na apresentação á Diretoria da empresa, a implementação das ferramentas foi dividido em 3 etapas, evitando  
a exposição de detalhes muito técnicos e focando nos aspectos estratégicos, cada uma com seus objetivos especificos:

✅ **Etapa 1:** Implantação do serviço de armazenamento 
-  **Amazon RDS com PostgreSQL** 
- Banco de dados relacional fácil de gerenciar e otimizado para o custo total de propriedade
- Esse serviço será responsável por amazenar os dados que representam as nossas entidades, tais como: 
  - **Clientes**, **Laboratorios**, **Produtos**, **Estoques** e **Pedidos**. 
  
Para mais informações, acesse: [Amazon RDS](https://aws.amazon.com/pt/rds/postgresql)

✅ **Etapa 2:** Implatação do serviço de contêineres servless
- **AWS Fargate + ECS**,
- Computação sem servidor para contêineres auto gerenciáveis
- Esse serviço será reponsável por executar nossas cargas de trabalho com capacidade de auto _autoscaling_  
  nas imagens registradas no ECS, 
  nosso foco é no desenvolvimento da aplicação sem se preocupar muito com cofigurações de implantação.

Para mais informações, acesse: [AWS Fargate](https://aws.amazon.com/pt/fargate)

✅ **Etapa 3:** Implantação do serviço de mensagerias
- **Amazon SQS**
- Filas de mensagens gerenciadas para microsserviços, sistemas distribuídos e aplicações sem servidor
- Esse serviço será responsável por prover a comunicação assíncriona entre nossos microserviços, tais como:
  - **customer-manager**, **lab-manager**, **stock-manager**, **orders-manager**.  

Para mais informações, acesse: [Amazon SQS](https://aws.amazon.com/pt/sqs)

---

## Conclusão
A implementação de ferramentas na empresa **Abstergo Industries** tem como esperado 
- *Direcionar os esforços no desensenvolvimento das soluções do negócio*
- *Flexibilizar o potencial das operações com agilidade conforme as demandas*
- *Baixar o custo financeiro com recursos computacionais de forma geral*

Com essa implatação, a expectativa de uma forma geral é garantir o aumento da eficiência e produtividade da empresa.   
Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam 
melhorar ainda mais os processos da empresa.

---

## Anexos

### Diagrama AWS da solução:
![service-archtecture.drawio.svg](service-archtecture.drawio.svg)

### Estimativa de Custo:
A estimativa do custo total no ambiente de Desenvolvimento/Testes será de aproximadamente R\$ 42.785,00 anuais

| Periodo | Custo em dolares | Custo em reais |
|:--------|:----------------:|:---------------|
| Mensal  |     $ 667,56     | R$ 3.498,00    |
| Anual   |    $ 8.010,72    | R$ 42.785,00   |

Para mais informações acesso o documento: [Custo Estimado](estimated-cost.pdf), ou acesse o link 
[Calculo estimado AWS](https://calculator.aws/#/estimate?id=f70a9a9433c4533e9b15dbb8fd07e08e407df639) 

Assinatura do Responsável pelo Projeto:

Thiago Basilio