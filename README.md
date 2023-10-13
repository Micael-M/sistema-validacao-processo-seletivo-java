<h1 align="center">🤳💻 Boas vindas ao projeto Pequeno Sistema para Validação de Processo Seletivo 💻🤳</h1>

## 💻 Proposta do desafio - Controle de fluxo

Vamos exercitar todo o conteúdo apresentado no módulo de Controle de Fluxo codificando o seguinte cenário.

O sistema deverá receber dois parâmetros via terminal que representarão dois números inteiros, com estes dois números você deverá obter a quantidade de interações (for) e realizar a impressão no console (System.out.print) dos números incrementados, exemplo:

* Se você passar os números 12 e 30, logo teremos uma interação (for) com 18 ocorrências para imprimir os números, exemplo: `"Imprimindo o número 1"`, `"Imprimindo o número 2"` e assim por diante.
* Se o primeiro parâmetro for MAIOR que o segundo parâmetro, você deverá lançar a exceção customizada chamada de `ParametrosInvalidosException` com a segunda mensagem: "O segundo parâmetro deve ser maior que o primeiro"   


1. Crie o projeto `DesafioControleFluxo`
2. Dentro do projeto, crie a classe `Contador.java` para realizar toda a codificação do nosso programa.
3. Dentro do projeto, crie a classe `ParametrosInvalidosException` que representará a exceção de negócio no sistema. 

Abaixo temos um trecho de código no qual você poderá seguir alterando as partes que contenham `??`

```java
public class Contador {
	public static void main(String[] args) {
		Scanner terminal = new Scanner(System.in);
		System.out.println("Digite o primeiro parâmetro");
		int parametroUm = terminal.??;
		System.out.println("Digite o segundo parâmetro");
		int parametroDois = terminal.??;
		
		try {
			//chamando o método contendo a lógica de contagem
			contar(parametroUm, parametroDois);
		
		}catch (? exception) {
			//imprimir a mensagem: O segundo parâmetro deve ser maior que o primeiro
		}
		
	}
	static void contar(int parametroUm, int parametroDois ) throws ParametrosInvalidosException {
		//validar se parametroUm é MAIOR que parametroDois e lançar a exceção
		
		int contagem = parametroDois - parametroUm;
		//realizar o for para imprimir os números com base na variável contagem
	}
}
```


## 💻 Minha implementação

```java
package candidatura;
import java.util.Scanner;

public class Contador {
	public static void main(String[] args) {
		Scanner terminal = new Scanner(System.in);
		System.out.println("Digite o primeiro parâmetro");
		int parametroUm = terminal.nextInt();
		System.out.println("Digite o segundo parâmetro");
		int parametroDois = terminal.nextInt();
		
		try {
			//chamando o método contendo a lógica de contagem
			contar(parametroUm, parametroDois);
		
		}catch (ParametrosInvalidosException exception) {
			//imprimir a mensagem: O segundo parâmetro deve ser maior que o primeiro
			System.out.println(exception.getMessage());
		}
		
	}
	static void contar(int parametroUm, int parametroDois ) throws ParametrosInvalidosException {
		//validar se parametroUm é MAIOR que parametroDois e lançar a exceção
		if(parametroUm >= parametroDois) {
      throw new ParametrosInvalidosException("O segundo parâmetro deve ser maior que o primeiro");
    }
		int contagem = parametroDois - parametroUm;
		//realizar o for para imprimir os números com base na variável contagem
		for(int i = 1; i <= contagem; i++) {
      System.out.println("Imprimindo o número " + (parametroUm + i));
    }
	}
}

class ParametrosInvalidosException extends Exception {
    public ParametrosInvalidosException(String errorMessage) {
        super(errorMessage);
    }
}
```

<section class="social_networks">
  <p align="center">Para entrar em contato é só clicar no link abaixo!<br></p>
  <div align="center" class="contacts" >
    <a href="https://www.linkedin.com/in/micael-maicon/" target="_blank" alt="Linkedin do autor" rel="nofollow">
    <img src="https://camo.githubusercontent.com/fcc551d4cff1847eb5a8ee518859132d52149a6db9f37833fdbea96451684bb6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d4c696e6b6564696e2d3143314331433f7374796c653d666f722d7468652d6261646765266c6f676f3d4c696e6b6564696e266c6f676f436f6c6f723d303046464646266c696e6b3d68747470733a2f2f7777772e6c696e6b6564696e2e636f6d2f696e2f69757269636f6465" style="max-width: 100%;">
  </a>
  <a href="https://discord.gg/QXGn6nt2" target="_blank" alt="Discord do autor" rel="nofollow">
    <img src="https://camo.githubusercontent.com/964caa47c23f903c00d8966c08f42ee934635bae58d018b5e69b9d08f5e41d42/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d446973636f72642d3143314331433f7374796c653d666f722d7468652d6261646765266c6f676f3d446973636f7264266c6f676f436f6c6f723d303046464646266c696e6b3d68747470733a2f2f646973636f72642e67672f516576444a71437a6159" style="max-width: 100%;">
  </a>
  </div>  
<section>
