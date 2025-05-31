# 42 Cursus - get_next_line

<img src="./assets/get_next_linem.png" alt="completion-with-bonus-badge" align="left">

A **get_next_line** é capaz de ler uma linha de um arquivo de texto, identificado por um `file descriptor`, a cada chamada da função, utilizando uma `variável estática` para continuar de onde parou sem perder dados. Ela precisa ser capaz de lidar com diferentes arquivos de entrada e ler cada linha de forma independente. Se chamado em um loop, retorna todo o conteúdo de um arquivo, linha por linha, até o final. E assim como a libft, a função get_next_line poderá ser útil em projetos futuros.

## Retornos <img src="https://img.shields.io/badge/GRADE-125%2F100-green" align="right">

- O valor `-1` será retornado se houver algum erro.
- O valor `1` será retornado se a linha for lida.
- O valor `0` será retornado quando o arquivo for totalmente lido.

## Bônus

O bônus permite a leitura de mais de um arquivo por vez sem que a informação seja perdida.

## Compilação e Execução

Um valor padrão para o **BUFFER_SIZE** (neste caso, quantidade de caracteres salvos na memória) pode ser definido em `get_next_line.h`, bastando que a compilação seja feita junto à main:

	cc -Werror -Wextra -Wall get_next_line.c get_next_line_utils.c main.c

Caso queira sobrescrever o tamanho do **BUFFER_SIZE**, deve-se passar o valor por parâmetro na compilação:

	cc -Werror -Wextra -Wall -D **BUFFER_SIZE**=3 get_next_line.c get_next_line_utils.c main.c

Para compilar o bônus, o procedimento é o mesmo, mas utilizando os arquivos bônus:

	cc -Werror -Wextra -Wall -D **BUFFER_SIZE**=3 get_next_line_bonus.c get_next_line_utils_bonus.c main.c

E para executar, temos algumas opções.

- Gera números aleatórios:

	```
	./a.out /dev/random
	```

- Standart input: Recebe uma entrada que nós digitamos e nossa GNL deve imprimir o mesmo texto (interrompa com ctrl+c):

	```
	./a.out /dev/tty
	```

- Lê um arquivo

	```
	./a.out file
	```

- \[**Bônus**] Lê vários arquivos

	```
	./a.out file0 file1 file2
	```

## Testers Utilizados

- [Tripoulli](https://github.com/Tripouille/gnlTester)
- [GNL Station Tester](https://github.com/kodpe/gnl-station-tester)
