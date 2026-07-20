---
icon: lucide/rocket
---

# Início

Você saberia informar qual é o nome de seu computador, notebook ou máquina virtual?


## Escolha de hostname

Ao escolher o nome de uma máquina, prefira utilizar o nome de um **lugar geográfico**, como uma cidade, um bairro ou outro espaço geográfico bem definido. O nome deve seguir o padrão de *slug* de URL, como `sao-paulo` para representar o nome "São Paulo"[^1].

Evite utilizar seu próprio nome como *hostname*, pois isso pode gerar ambiguidades.

Imagine que seu nome seja Fulano e que você tenha acabado de adquirir uma máquina para configurá-la como servidor de um domínio. Se você utilizar o domínio `fulano.lab`, configurar a máquina com o nome `fulano` e criar um usuário chamado `fulano`, teremos a seguinte situação:

> O usuário `fulano` autenticou-se na máquina `fulano`, que pertence ao domínio `fulano.lab`.

Essa forma de identificação torna a comunicação entre administradores e usuários menos clara.

### Um bom exemplo de hostname

Agora imagine que Jurandy, natural de Teresina, no estado do Piauí, deseje configurar um servidor chamado `teresina`, pertencente ao domínio `pi.lab`, e criar um usuário para si nesse domínio. Nesse caso, a comunicação fica muito mais clara:

> O usuário `jurandy` autenticou-se na máquina `teresina`, que pertence ao domínio `pi.lab`.

Observe que:

* `jurandy` é o *slug* de um nome próprio;
* `teresina` é o *slug* do nome da capital do estado do Piauí (PI);
* `pi.lab` é um domínio que utiliza a sigla da unidade federativa onde se localiza a cidade de Teresina.

Cada identificador representa um conceito distinto: usuário, máquina e domínio.

### Um mau exemplo de hostname

Suponha que Fulano tenha atribuído à máquina o nome `fulano`, criado um usuário `beltrano` para um colega e configurado um servidor SSH para permitir acesso remoto. Se Beltrano desejar conectar-se ao servidor `fulano`, devidamente registrado no DNS, executará o seguinte comando:

```text
ssh beltrano@fulano
```

Esse comando pode ser descrito em português de duas formas:

1. O usuário `beltrano` iniciou uma sessão SSH na máquina `fulano`.
2. `beltrano` entrou em `fulano`.

A primeira forma é precisa, mas menos comum na linguagem cotidiana. A segunda é mais natural, porém pode causar interpretações ambíguas devido ao seu duplo sentido.

Por esse motivo, recomenda-se evitar utilizar nomes de pessoas como *hostnames*. Escolher nomes de lugares, fenômenos naturais, constelações, rios ou outros conjuntos de nomes coerentes costuma produzir uma nomenclatura mais clara, escalável e fácil de administrar.

Uma sugestão de conteúdo é acrescentar um critério técnico para a escolha de *hostnames*. Além de evitar nomes de pessoas, é recomendável que o nome:

* seja curto e fácil de pronunciar;
* contenha apenas letras minúsculas, números e hífens;
* não comece nem termine com hífen;
* evite acentos, espaços e caracteres especiais;
* seja único dentro do domínio;
* faça parte de uma convenção de nomenclatura (por exemplo, cidades, rios, montanhas, planetas ou constelações).

Essas recomendações aproximam o texto das boas práticas adotadas em administração de sistemas e redes.

[^1]: O nome "São Paulo" não é uma boa escolha para um *hostname*, pois pode se referir tanto ao estado quanto à cidade. Em situações como essa, prefira nomes que identifiquem um único lugar ou utilize convenções adicionais para eliminar ambiguidades.