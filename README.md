# DOCUMENTO DE EXEMPLO




# Estratégia de Testes

+ Objetivo
   Esse documento visa descrever o processo de Qualidade adotado pelo Time #### para o Projeto #####

# Tipos de Teste

   Os testes automatizados estão distribuídos em camadas a partir de cada tipo de teste. 

+ **Testes Unitários**

   + **Back-end** Junit V4/V5, Mockito. 
   + **Mobile-Android** Junit V4
   + **Mobile-IOS** Quick + Nimble 
   
   + **Relatório de cobertura**
       
       + **Android e Back-end** Jacoco
       + **iOS** Slather
  
     **POR QUE:** Validar as partes unitárias do código e garantir que cada pedaço funciona 
     separadamente 

     **QUEM:**  Desenvolvedores de cada frente específica mais par com QA 

     **ONDE:** Local Dev + CI (parte do merge)

+ **Testes de Serviço**
  + **Contrato** Joi e JoiAssert
  + **API**  Mocha com Chai e supertest

     **POR QUE:** Para validar que a comunicação entre os componentes e serviços está 
     funcionando

     **QUEM:**  QAs

     **ONDE:** Local Dev (mas também será adicionado no CI)

+ **Testes instrumentados**
 
   + **Mobile-Android** Espresso com kotlin
   + **Mobile-IOS** kif 

+ **Testes de Interface**
   + **Mobile Android e iOS** 
     Cucumber com Appium em Linguagem Ruby.

     **POR QUE:** Para validar os fluxos conforme o comportamento dos usuários

     **QUEM:**  
     + Cenários -> QA, PO e Designer 
     + Testes Automatizados -> QA   
     + Testes Manuais -> PO e QA
     + ONDE: Local (mas também será adicionado no CI)

# Ambientes: 

+ **SandBox** (Ambiente para Desenvolvimento e Testes)
+ **Homologação** ( Ambiente para Testes, espelho de produção)
+ **WireMock**  ( Ambiente para Testes específicos “Massas que expiram e são difíceis de criar”)
 
# Tagueamento dos cenários

+ **@android e @ios**   Para geração de métricas no Weaver-Report
+ **@erro_conexao**  Identificar cenários que vão desabilitar a internet durante os testes
+ **@mock**   Identificar cenários que vão rodar no WireMock
+ **@instrumentados**  Identificar cenários que vão ser cobertos pelos desenvolvedores
+ **@api**  Identificar cenários que vão ser cobertos na camada de serviço




# Funcionalidades Testadas e Cenários Executados

   Ainda vamos definir os testes que serão executados no @smoke_test





+ **Execução dos Testes**

    No final da execução serão disponibilizadas o relatório de execução do cucumber com a 
    quantidade de testes que passaram e que falharam.
    Precisamos implementar a categorização dos cenários que falharem, a principio são essas:

    + **Impeditiva** – Ocorrência que impede o uso do sistema. Não existe forma de contorná-la.

    + **Funcional** – Ocorrência não impeditiva, ou seja, pode ser contornada pelo usuário e é relativa ao funcionamento do sistema. É o não cumprimento de algum requisito.
    
    + **Texto** – Qualquer ocorrência relacionada a mensagens da aplicação.











# Métricas

+ Cobertura de Testes Unitários

+ Quantidade de Cenários escritos X Cenários Automatizados 

+ Quantidade de Cenários Automatizados por Plataforma

+ [Weaver-Report](https://github.com/nathsilv/weaver)






# Melhorias


```Revisar estrutura atual do projeto```





# DOCUMENTO DE EXEMPLO


