### Inserção e balanceamento da árvore AVL

Os valores foram inseridos na seguinte ordem:
55, 26, 29, 13, 12, 11, 16, 1, 5, 29, -15, 4, 16, 8, 4, 5, 3, 1312, 100, 88.

Para realizar as inserções, foi seguida a regra da Árvore Binária de Busca, em que os valores menores ficam à esquerda e os valores maiores ficam à direita.    

Para verificar se a árvore estava balanceada, foi considerada a altura das subárvores. A altura corresponde à quantidade de arestas entre um nó e a folha mais distante abaixo dele.

Foi utilizado o cálculo:

FB = altura da esquerda − altura da direita

Quando o resultado fica entre -1 e +1, o nó está balanceado. Quando chega a +2 ou -2, é necessário realizar o balanceamento.
Inserção do valor 29

Primeiro foi inserido o valor 55, que se tornou a raiz. Depois foi inserido o 26, ficando à esquerda do 55.
Ao inserir o 29, como 29 < 55, ele foi para a esquerda. Depois, como 29 > 26, ele ficou à direita do 26.

Nesse momento, o nó 55 ficou desbalanceado.
Cálculo:
Altura da esquerda = 1
Altura da direita = -1
FB(55) = 1 − (-1) = +2

Como o valor foi inserido na direita do filho esquerdo, foi necessário fazer um balanceamento do tipo Esquerda-Direita (LR).
Após o balanceamento, o valor 29 passou a ocupar a posição central entre 26 e 55.
Inserção do valor 12

Depois da inserção dos valores 13 e 12, o nó 26 ficou com a subárvore esquerda maior que a direita.

Cálculo:
Altura da esquerda = 1
Altura da direita = -1
FB(26) = 1 − (-1) = +2

Como os valores estavam concentrados no lado esquerdo, foi feito o balanceamento correspondente, fazendo com que o valor 13 passasse a ficar acima de 12 e 26.
Inserção do valor 11
Ao inserir o valor 11, o nó 29 ficou desbalanceado.

Cálculo:
Altura da esquerda = 2
Altura da direita = 0
FB(29) = 2 − 0 = +2

Foi necessário realizar novamente o balanceamento da árvore. Depois da correção, o valor 13 passou a ocupar uma posição superior nessa região.
Inserção do valor 1
O valor 1 foi inserido à esquerda do 11.
Com essa inserção, o nó 12 ficou desbalanceado.

Cálculo:
Altura da esquerda = 1
Altura da direita = -1
FB(12) = 1 − (-1) = +2

Após o balanceamento, o 11 passou a ficar entre o 1 e o 12.
Inserção do valor 4
Depois da inserção dos valores 5, 29, -15 e 4, ocorreu um novo desbalanceamento na região do nó 11.

Cálculo:
Altura da esquerda = 2
Altura da direita = 0
FB(11) = 2 − 0 = +2

Nesse caso, o crescimento ocorreu na direita da subárvore esquerda, sendo necessário realizar um balanceamento Esquerda-Direita.
Inserção da segunda ocorrência de 16
O valor 16 já aparecia na árvore, mas o visualizador utilizado permitiu inserir uma segunda ocorrência.
Depois dessa inserção, o nó 26 ficou desbalanceado.

Cálculo:
Altura da esquerda = 1
Altura da direita = -1
FB(26) = 1 − (-1) = +2

Foi realizado o balanceamento dessa região, mantendo os valores 16 e 26 corretamente organizados.
Inserção do valor 88
Após a inserção dos valores 1312, 100 e 88, ocorreu outro desbalanceamento.
O valor 88 ficou abaixo do 100, que estava abaixo do 1312.

No nó 1312:
Altura da esquerda = 1
Altura da direita = -1
FB(1312) = 1 − (-1) = +2

Foi realizado o balanceamento dessa parte da árvore. Depois disso, o valor 100 passou a ficar entre 88 e 1312.

### Resultado após as inserções

Depois de inserir todos os valores e realizar os balanceamentos necessários, a árvore ficou balanceada.

O próprio material diferencia uma Árvore Binária de Busca não balanceada de uma Árvore AVL balanceada e apresenta o visualizador AVL utilizado na atividade.  

### Remoções

Depois das inserções, foram removidos os valores:
4, 29, 100, 5, 15, 16 e 55.

Apresenta três situações de remoção: nó folha, nó com um filho e nó com dois filhos.  

Remoção do valor 4
O valor 4 encontrado possuía dois filhos. Para realizar a remoção, foi utilizado o valor imediatamente menor disponível nessa região da árvore.
O valor 3 foi utilizado na substituição.

Após a remoção, a árvore continuou balanceada e não foi necessária uma nova rotação.
Remoção do valor 29
O nó 29 também possuía dois filhos.

O valor imediatamente menor disponível na sua subárvore esquerda era o 26. Dessa forma, o valor 26 foi utilizado na substituição do 29.
Depois da remoção, a árvore permaneceu balanceada.

Remoção do valor 100
O nó 100 possuía dois filhos: 88 e 1312.
O valor imediatamente menor era o 88. Por isso, o 88 ocupou a posição anteriormente ocupada pelo 100.
A árvore continuou balanceada após essa operação.

O material explica que, para um nó com dois filhos, pode ser utilizado o valor imediatamente maior ou o imediatamente menor, dependendo da implementação.     

Remoção do valor 5
O primeiro valor 5 encontrado também possuía dois filhos.
Foi utilizado o valor 4 para substituir o 5. Por esse motivo, na árvore final, o lado esquerdo da raiz passa a ter o valor 4 nessa posição.

Remoção do valor 15
Ao buscar o valor 15, ele não foi encontrado na árvore.
Por isso, nenhuma alteração foi realizada.

Remoção do valor 16
Existiam duas ocorrências do valor 16.
Ao remover uma delas, a outra permaneceu na árvore. Depois dessa operação, ocorreu um desbalanceamento na região do nó 26.

O cálculo ficou:
Altura da esquerda = 0
Altura da direita = 2
FB(26) = 0 − 2 = -2

Como o valor ficou desbalanceado para o lado direito, foi necessário realizar o balanceamento dessa região.

Remoção do valor 55
O valor 55 possuía dois filhos.
Foi utilizado o maior valor existente na sua subárvore esquerda, que era o 29.
Assim, o 29 passou a ocupar a posição do 55 e a ocorrência utilizada na substituição foi removida.
Depois dessa operação, não foi necessária outra rotação.

### Árvore final
Depois de realizar todas as inserções, balanceamentos e remoções, foi obtida a árvore final.

Os valores 4, 29, 5 e 16 ainda aparecem porque existiam duas ocorrências de cada um deles na sequência de inserção e foi solicitada a remoção de apenas uma ocorrência.
O valor 15 não aparece porque ele não fazia parte da sequência de inserção.
Verificação do balanceamento final

Na raiz, que possui o valor 13:
Altura da subárvore esquerda = 3
Altura da subárvore direita = 2

Então:
FB(13) = 3 − 2 = +1
Como o resultado é +1, a raiz está balanceada.
Alguns outros cálculos da árvore final são:

Nó 4:
Altura esquerda = 1
Altura direita = 2
FB(4) = 1 − 2 = -1

Nó 11:
Altura esquerda = 1
Altura direita = 0
FB(11) = 1 − 0 = +1

Nó 29:
Altura esquerda = 1
Altura direita = 1
FB(29) = 1 − 1 = 0

Nó 26:
Altura esquerda = 0
Altura direita = -1
FB(26) = 0 − (-1) = +1

Nó 88:
Altura esquerda = -1
Altura direita = 0
FB(88) = -1 − 0 = -1

Como os fatores encontrados ficam entre -1 e +1, a árvore final permanece balanceada.

### Conclusão

Durante a inserção dos elementos, os valores foram posicionados seguindo as regras da Árvore Binária de Busca, em que os valores menores ficam na subárvore esquerda e os maiores na subárvore direita. Após as inserções, o balanceamento da árvore foi realizado considerando as alturas das subárvores, de modo a manter a estrutura como uma Árvore AVL balanceada.
Em seguida, foram realizadas as remoções dos valores 4, 29, 100, 5, 15, 16 e 55, considerando os diferentes casos de remoção de nós apresentados no conteúdo: nó folha, nó com um filho e nó com dois filhos. O valor 15 não estava presente na árvore e, por isso, sua tentativa de remoção não provocou alteração.
Ao final das operações, a árvore permaneceu balanceada e respeitando as propriedades de uma Árvore Binária de Busca.
