# Criptografia_RSA
É um sistema simples de criptografia do Algoritmo RSA Desenvolvido para fins de aprendizado e compreensão do conceito do algoritmo.  O sistema gera números primos grandes, chaves públicas e privada, encripta e decripta com as chaves.

Sistema simples de criptografia do Algoritmo RSA
Desenvolvido para fins de aprendizado e compreensão do conceito do algoritmo.

O sistema gera números primos grandes, chaves públicas e privadas, encripta e decripta com as chaves.
Funcionamento
A RSA está fortemente ligada à Teoria dos Números, sendo baseado em pilares como as operações de resto e fatoração por números primos. O algoritmo pode ser resumido nos passos descritos abaixo:

Obter dois números primos p e q; (Utilizei o teste Miller-Rabin. É um teste probabilístico para saber se um número n é primo de forma eficiente).

Calcular n = p*q;

Calcul phi(n) = (p-1)(q-1); (Função totiente de Euler)

Escolher mdc(phi(n), E) == 1, ou seja, E e phi(n) são coprimos (primos relativos);

Calcul D sendo d*e = 1 mod(phi(n)), ou seja, d seja o inverso multiplicativo de E em (mod phi(n)); (Algoritmo de Euclides estendido)

Chave pública: (e, n); chave privada: (d, n);

Função para cifrar uma mensagem m: m^e = c mod(n);

Função para decifrar uma mensagem c: c^d = m mod(n);

O RSA se mantém devido à dificuldade em fatorar um grande número (n) em números primos (p e q). Se b é o número de bits de n, então existem v(2b-1) possibilidades a ser testadas em um eventual pior caso, o que resulta em complexidade de tempo. A título de curiosidade, considerando b = 2048, v(2b) resulta em um número um pouco maior que 1,79,10308. Considerando uma supermáquina que consegue processar 1 bilhão (109) de tentativas por segundo, foram necessários mais de 5,10291 anos.

Mais informações:
O Algoritmo de Criptografia RSA 1 de 2: Computando um exemplo

Criptografia RSA(canal Toda a Matemática)

RSA Criptografia Assimétrica e Assinatura Digital

https://medium.com/@prudywsh/how-to-generate-big-prime-numbers-miller-rabin-49e6e6af32fb

https://en.wikipedia.org/wiki/RSA_ (criptoistema)

https://seer.imed.edu.br/index.php/revistasi/article/view/1639/1296

https://www.lambda3.com.br/2012/12/entendendo-de-verdade-a-criptografia-rsa/
