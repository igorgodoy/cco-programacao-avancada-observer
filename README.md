# Programação Avançada

Atividade padrão de projeto - **Observer**.

## Conteúdos

1. [Classificação](https://github.com/igorgodoy/cco-programacao-avancada-observer#classifica%C3%A7%C3%A3o)
2. [Intenção](https://github.com/igorgodoy/cco-programacao-avancada-observer#inten%C3%A7%C3%A3o)
3. [Motivação](https://github.com/igorgodoy/cco-programacao-avancada-observer#motiva%C3%A7%C3%A3o)
4. [Aplicação](https://github.com/igorgodoy/cco-programacao-avancada-observer#aplica%C3%A7%C3%A3o)
5. [Estrutura](https://github.com/igorgodoy/cco-programacao-avancada-observer#estrutura)
6. [Participantes](https://github.com/igorgodoy/cco-programacao-avancada-observer#participantes)
7. [Implementação](https://github.com/igorgodoy/cco-programacao-avancada-observer#implementa%C3%A7%C3%A3o)

## Composite

### Classificação

- O padrão de projeto **Observer** pode ser classificado, de forma básica e literal, em multiplos objetos capazes de "monitorar" outro determinado objeto e serem notificados a cada mudança de estado deste objeto observado.

### Intenção

- Notificar objetos observadores sobre mudanças de estado em um outro objeto observado para que os "efeitos colaterais" desta mudança de estado ocorram.

### Motivação

- O padrão **Observer** nos poupa esforços ao trabalhar com multiplos objetos em colaboração entre si.

### Aplicação

- Este padrão é comumente utilizado em casos onde há validações de pagamento em aplicações, de modo que diversas entidades devem monitorar o status de uma transação de pagamento para que tomem diferentes estados. Por exemplo em uma situação de compra de curso, onde o aluno de uma instituição (usuário) realiza a compra de determinado curso, desta forma o curso deve observar as mudanças de status de pagamento para que passe de "bloqueado" para "liberado", dentre outros cenários possíveis.

### Estrutura

- Este [diagrama](http://www.linhadecodigo.com.br/artigos/img_artigos/DiogoSouza/ObserverJava/ObserverJava01.jpg) representa um componente desenhado utilizando este padrão de projeto.

### Participantes

- *Subject*: Objeto a se monitorar através do observer.
- *Observer*: Interface onde se define os métodos para notificações de interesse dos observadores.
- *ConcreteObserverA & ConcreteObserverB*: Objetos (multiplos) observadores, os quais serão notificados sobre mudanças de estado do objeto *Subject*.

### Implementação

- [Implementação](https://github.com/igorgodoy/cco-programacao-avancada-observer/tree/main/example) onde o padrão de projeto **Observer** foi utilizado para o implementar as relações entre os objetos de um editor de texto, onde a cada mudança no objeto Editor, os assinantes serão notificados e um *log* será escrito.