# O que é React?

React é uma **biblioteca para construir interfaces de usuário**. Essa é a descrição que encontramos no site do Facebook, a empresa por trás dessa biblioteca. 
Sim, React é uma **biblioteca** e não um **framework**, como muitos acreditam antes de começar a estudar sobre. Para os que não sabem, uma **biblioteca** é um pedaço de código reutilizável
que geralmente foca em uma única funcionalidade, que pode ser acessada através de sua API. Já um **framework** é também um pedaço de código, que geralmente envolve um conjunto de bibliotecas ou funcionalidades, para conseguir 
realizar uma operação maior, como por exemplo criar uma *single page application*, o que é o caso do **Angular**.  

React é uma biblioteca popular e por uma boa razão, ela é extremamente útil. Mas quando alguns desenvolvedores consideram aprender React, eles frequentemente acabam enfrentando um problema: eles não têm muita certeza do que o React é ou quais são os problemas que ele resolve. Você provavelmente já leu várias descrições explicando o que é React, aproveito para listar aqui algumas que eu já encontrei ao longo do meu aprendizado:

React é...

1. Uma biblioteca de JavaScript para criar interfaces de usuário.

2. Uma abstração da *view* baseada em componentes.

3. Uma abstração do DOM usada para evitar lidar diretamente com elementos HTML.

4. O `V` do famoso MVC.

Tudo isso é verdade, mas eles também descrevem toneladas de outros frameworks JavaScript. Eu acredito que React é melhor descrito pelo problema que resolve. E é isso que vamos focar nessa seção, no problema que o React resolve e como ele faz isso de maneira tal que o fez se tornar uma das bibliotecas Javascript mais conhecidas e usadas da atualidade. 

## Características

### Declarativo
Um estilo declarativo, como o que React, permite que você controle o fluxo e o estado em sua aplicação, dizendo: "Deve ser parecido com isso". Um estilo imperativo é diferente e permite que você controle sua aplicação dizendo "isto é o que você deve fazer".

Vamos ver um exemplo prático disso. Imagine um componente de uma interface do usuário simples, como um botão `curtir`. Quando você clica nele ele se torna azul se era cinza e se torna cinza se era azul. A maneira imperativa de fazer isso seria algo como:

```javascript
if(user.curtir()){
  if(!isAzul()) {
    removeCinza();
    addAzul();
  }
}else{
   if(isAzul()){
      removeAzul();
      addCinza();
   }
}
```

Então basicamente eu tenho que verificar o que está atualmente na tela e fazer chamadas para manipulá-lo. Você pode imaginar como complexo isso poderia ficar.

Isto é como você escreveria isso em React (abordagem declarativa):

```javascript
if(this.state.liked){
  return <LikeAzul />;
}else{
  return <LikeCinza />;
}
```

o foco aqui na interface é o estado. Você pode perceber quão mais simples o código é para entender. 

### Baseado em Componentes
Crie componentes encapsulados que gerenciam seu próprio estado e, em seguida, componha-os para criar UIs complexas.

### Aprenda uma vez, escreva em qualquer lugar
React também pode ser renderizado no servidor usando o Node e além disso é possível criar aplicativos móveis com recurso [React Native](https://facebook.github.io/react-native/)
