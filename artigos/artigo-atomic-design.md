#### Unoesc Chapecó
#### Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#### Disciplina: HTML5+CSS3
#### Professor: Jean Carlo Nascimento
#### Acadêmico(a): Álvaro Gianni Pagliari
### Artigo de revisão de Atomic Design


#####Resumo:
Atomic Design é uma metodologia desenvolvida por Brad Frost para melhorar o processo de design web. O autor utiliza uma analogia com os termos definidos pela ciência para separar as etapas do design e a granularidade de cada componente usado em um determindo design. Para isso o autor utiliza os termos *átomos*, *moléculas*, *organismos*, *modelos* (templates) e *páginas*. 

#####O que é?

Com o objetivo de otimizar o tempo de desenvolvimento e melhorar a comunicação entre designers, programadores e clientes, Brad Frost propôs o Atomic Design como uma metodologia de trabalho. O autor utiliza uma analogia com a biologia para definir o processo de design, ou seja, o universo é composto por **átomos** que são indivisíveis por definição mas que quando combinados viram **moléculas** que então se agrupam para formar **organismos**, e é aí que saímos do abstrato e da analogia com a biologia e passamos ao concreto. Vários organismos compõem **modelos** ou **templates** que serão utilizados para a criação de **páginas** (que são instâncias específicas dos templates).

A imagem abaixo ilustra essa sequência de crescimento do design.

![Alt Text](http://bradfrost.com/wp-content/uploads/2013/06/atomic-design.png)

####Como funciona?

Segundo o autor, devemos iniciar o design desenvolvendo os átomos - menores itens presentes em uma página web -  como labels, inputs, botões, entre outros. Em seguida, devemos agrupar os átomos e criar moléculas, que são pequenas funcionalidades da interface como um agrupamento de headers ou um label com um input e um botão que pode servir como um formulário de busca. Em seguida agrupamos as moléculas em organismos, por exemplo, o cabeçalho de um site pode ser composto pelas moléculas de logotipo, menu de navegação, formulário de busca, formulário de login, entre outros.   Na sequência reúnem-se vários organismos em um template, que é um modelo de baixa fidelidade do site sendo desenvolvido. O termo baixa fidelidade se dá ao fato de que um template, não necessariamente, possui a tipografia, cores e imagens do design, mas já especifica onde cada organismo deve estar, muito útil para a fase de desenvolvimento e prototipação. Com base nessas informações então é definida uma página, sendo esta uma instância do template porém em alta fidelidade.

A metodologia de Atomic Design tem a característica de ir do abstrato ao concreto, ou seja, partindo de pequenos átomos chegamos no design da página desejada. Ao invés de desconstruir uma página a partir da idéia inicial do design, vamos criando o design em outra direção. Essa inversão na maneira de pensar o design permite que programadores comecem a definir os átomos, moléculas e organismos que um design terá enquanto o designer ainda está pensando nos templates. Essa modularização permite a reutilização dos componentes em vários locais do design garantindo maior consistência e facilidade de uso.

#####Por que usar?

Segundo o blog nomadev, várias são as razões do porque utilizar o Atomic Design, como uma melhor organização do código (Regra da Modularidade), códigos mais limpo e fácil de ler (Regra da Clareza), maior facilidade de comunicação entre os componentes (Regra da Composição) e uma separação entre o comportamento do componente na interface em relação às sua interação com o backend (Regra da Separação). Também podemos ressaltar que muitos projetos utilizam frameworks prontos para a Web, com estilos, átomos, moléculas e organismos já pré-definidos. Isso faz com que vários sites tenham um design semelhante e até certo ponto "sem graça". O Atomic Design preza pela organização do design, mas te dá liberdade de criar sobre uma fundação sólida, ou seja, ele não te dá o peixe, mas te ensina a pescar.

#####Onde usar?

Por ser uma metodologia, o Atomic Design pode ser utilizado em qualquer desenvolvimento web. É indicado que o projeto já inicie utilizando as definições da metodologia pois assim é possível criar uma biblioteca de padrões utilizados e modificar o design com mais eficácia.

#####Exemplos

Abaixo seguem imagens com exemplos de cada uma das categorias definidas pelo Atomic Design.



#####Referências
[atomic_web_design_brad_frost](http://bradfrost.com/blog/post/atomic-web-design/)<br/>
[atomic_design_nomadev](http://nomadev.com.br/atomic-design-por-que-usar/)<br/>
[atomic_design_nomadev2](http://nomadev.com.br/atomic-design-nomeclatura-suissa/)<br/>
[atomic_design_tableless](http://tableless.com.br/o-que-e-design-atomic/)<br/>
