# Javascript - Tratamento de Erros

## ECMAScript Error

> - Erros que ocorrem em tempo de execução.
> - Composto por:
> 1. Mensagem
> 2. Nome
> 3. Linha
> 4. Call Stack

## DOMException

> - Erros relacionados ao Document Object Model (DOM).

## Tratamento de Erros

### Throw

#### :pencil2: Exemplo

    function verificaPalindromo(string) {
    	if(!string) return "String inválida";
    	return string === string.split('').reverse().join(''); 
    }    	
    
    verificaPalindromo('cat');

##### **👀 Neste exemplo, caso a String seja inválida, o sistema irá retornar uma string como erro. Por causa da função RETURN **

    function verificaPalindromo(string) {
    	if(!string) throw "String inválida";
    	return string === string.split('').reverse().join(''); 
    }
    	
    
    verificaPalindromo('cat');

##### **👀 Neste exemplo, caso a String seja inválida, o sistema irá retornar um erro  com todas as informações de um ECMAScript Error.  Por causa da função THROW**

### Try ... catch

#### :pencil2: Exemplo

    function verificaPalindromo(string) {
        	if(!string) throw "String inválida";
        	return string === string.split('').reverse().join('');
    }
    function tryCatchExemplo(string) {
    	try {
    		  verificaPalindromo(string);  	
    	}
    	catch(erro)
    	{
	    	console.log(erro);
        }
    }
    
    tryCatchExemplo('');
    
    
   ##### **👀 Neste exemplo, caso a String seja inválida, o sistema irá retornar um erro, que será capurado pela função CATCH.  Com o erro capturado, podemos tratá-lo da maneira que quisermos**

### Finally

#### :pencil2: Exemplo

    function verificaPalindromo(string) {
        	if(!string) throw "String inválida";
        	return string === string.split('').reverse().join('');
    }
    function tryCatchExemplo(string) {
    	try {
    		  verificaPalindromo(string);  	
    	}
    	catch(erro)
    	{
	    	throw erro;
        }
        finally
        {
	        console.log("A string enviada foi: " + string);
        }
    }
    
    tryCatchExemplo('');
    
    
   ##### **👀 O Finally é uma instrução que será executada havendo erro ou não. **

## O objeto Error

    new Error (message, fileName, lineNumber)
    // Todos os parâmetros são opcionais
    // Os parâmetros fileName e lineNumber podem não funcionar em todos browsers
    const MeuErro = new Error('Mensagem Inválida');
    
    throw MeuErro;

##### **👀 A Saída será:**

    Uncaught Error: Mensagem Inválida
    	at <anonymous>:1:17
    	...

##

    const MeuErro = new Error('Mensagem Inválida');
    MeuError.name = 'InvalidMessage';
    
    throw MeuErro;

##### **👀 A Saída será:**

    Uncaught InvalidMessage: Mensagem Inválida
    	at <anonymous>:1:17
    	...


