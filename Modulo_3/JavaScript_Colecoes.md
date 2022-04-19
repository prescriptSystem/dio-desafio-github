# Javascript - Coleções

## Map

### Estrututura

    const myMap = new Map()

#### Características:
> - Uma coleção de arrays no formato [chave, valor];
> - Pode ser iterado por um loop for...of

### Métodos
> Adicionar, ler e deletar

    const myMap = new Map();
    myMap.set('apple', 'fruit');
    // Map(1) {"apple" => "fruit"}
    myMap.get('apple');
    // "fruit"
    myMap.delete("apple");
    // true
    myMap.get("apple");
    // undefined

### Map vs Objeto

> - Maps podem ter chaves de qualquer tipo;
> - Maps possuem a propriedade lenght;
> - Maps são mais fáceis de iterar;
> - Utilizado quando o valor das chaves é desconhecido;
> - Os valores tem o mesmo tipo.

## Set

### Estrututura

    const myArray = [1, 1, 2, 2, 3, 4, 5, 6, 7, 8, 2, 1]
    const mySet = new Set(myArray);

#### Características:
> - Sets são estruturas que armazenam apenas **valores únicos**.

### Métodos
> Adicionar, consultar e deletar

    const mySet = new Set();
    mySet.add(1);
    mySet.add(5);
    
    myMap.has(1);
    //true
    
    myMap.has(3);
    // false
    
    myMap.dalete(5);
    
### Set vs Array

> - Possui valores únicos;
> - Em vez da propriedade lenght, consulta-se o número de registros pela propriedade size;
> - Não possui os métodos map, filter, reduce, etc;

