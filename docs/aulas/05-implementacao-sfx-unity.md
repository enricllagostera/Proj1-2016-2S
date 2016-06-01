# Implementação de SFX na Unity

Agora temos um conjunto de arquivos de som, criados expressamente para o uso em nosso jogo. Como fazemos para que esses efeitos estejam integraddos corretamente com os eventos do meu jogo? Essa etapa é a **implementação dos sons** no jogo.

### Atividade: *Grotto*

Vamos implementar sons num jogo 2D simples na Unity. Etapas da atividade:

1. Listar sons (e arquivos) necessários
2. Definir entradas e saídas dos sons
3. Definir canais utilizados
4. Disparar gatilhos adequados para cada som

### O básico na Unity

A partir da versão 5.0 da Unity, o sistema de som da ferramenta mudou consideravelmente, facilitando bastante o tratamento e customização do som. 

O básico continua bastante semelhante: um objeto (normalmente a câmera principal) tem um componente `AudioListener`, que serve como referência para onde estariam os *ouvidos* do jogador dentro da cena. Toda fonte sonora é um objeto com um componente `AudioSource` que toca o som em uma determinada posição do espaço.

### O momento certo

Uma questão importante quando se está implementando sons é garantir que o som toca quando o evento certo acontece. Os motivos para prestar bastante atenção nessa questão são:

1. **Sincronização com eventos ou ações do jogador**: se o som tem a função de dar feedback sobre uma ação do jogador ou mudança de estado do jogo (som interativo ou adaptativo), ele tem de tocar em conjunto com esse evento.
2. **Controle de transições**: a maneira que um som começa ou termina é determinante para seu significado. É importante evitar entradas e saídas bruscas ou suaves demais que não sejam condizentes com o tipo de som em questão. 

### O `AudioMixer`

![](https://unity3d.com/sites/default/files/styles/original/public/audio-1.jpg)

No novo sistema de áudio na Unity 5, ficou mais fácil configurar efeitos e controlá-los para um conjunto de sons. Anteriormente, seria necessário ir em cada fonte sonora e aplicar o efeito desejado. Agora, é possível enviar o som de cada fonte para um mesmo canal de áudio e aplicar os efeitos e equalização de forma centralizada. Também é possível parametrizar esses efeitos de acordo com diferentes momentos do jogo (por exemplo, criando um efeito de *embaixo d'água*).

Vamos estudar o mixer em mais detalhes mais adiante, nas aulas sobre *mixagem*.

## Referências

- COLLINS, K. **Game sound: an introduction to the history, theory, and practice of video game music and sound design.** 1. ed. [s.l.] The MIT Press, 2008. 
- GIBSON, J. **Introduction to Game Design, Prototyping, and Development: From Concept to Playable Game with Unity and C#.** 1 edition ed. Upper Saddle River, NJ: Addison-Wesley Professional, 2014. 