```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o salário e profissão}}
B --> C[\sal, prof\]
C --> D{prof == 'Tecnico'}
D --FALSE--> E{prof == 'Gerente'}
D --TRUE--> F[sal_reaj = 1.5 * sal]
E --FALSE--> H[sal_reaj = 1.1 * sal]
E --TRUE--> G[sal_reaj = 1.3 * sal]
G --> I([FIM])
F --> I
H --> J{{'Salário Reajustado = ', sal_reaj}}
J --> I
```

#### Pseudocódigo
```java
ALGORITMO calReajuste
DECLARE  sal, sal_reaj: real, prof: caractere

INICIO

    // Variaveis sal (Salário) e prof (Profissão) como entrada.
    LEIA sal, prof

    // Condições que decidirão para onde os dados de entrada serão enviados.
    ENVIE AS ENTRADAS PARA AS DETERMINADAS CONDIÇÕES

        // Caso a profissão seja técnico, o salário é multiplicado em 1.5 (+50%) 
        CASO prof == “Técnico”		
            sal_reaj ← 1.5 * sal

        // Caso a profissão seja gerente, o salário é multiplicado por 1.3 (+30%) 
        CASO prof = “Gerente”		
            sal_reaj ← 1.3 * sal

    // Caso a profissão não seja nenhuma das duas anteriores, o salário é multiplicado por 1.1 (+10%) 
    SENÃO
        sal_reaj ← 1.1 * sal

    FIM_CÓDIGO

    // Texto para informar o usuário de que a operação foi um sucesso.
    ESCREVA “Salário Reajustado = “, sal_reaj

FIM
```
