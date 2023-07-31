# Recomendador de fretes complemento

Realizamos um estudo de viabilidade das funcionalidades de um recomendador de fretes complemento para caminhoneiros. Há 2 pontos chaves na solução que queríamos avliar a viabilidade:

1. É comum que especificações de tamanho, volume e peso da carga venham especificadas em um campo de observação de texto aberto quando um frete é postado. Para solucionar esse problema, utilizamos a API da Open AI para extrair essas informações relevantes quando elas vêm no meio dos textos de observações do frete.
2. Para facilitar o caminhoneiro, ele pode entrar com as especificações de tamanho e/ou peso disponíveis no caminhão dele através de uma interface de chat utilizando mensagens. Dessa forma, é fácil para ele procurar um frete complemento que se encaixe nas suas necessidades. Para isso ser posível, utilizamos novamente a API da Open AI para extrair essas informações dos requisitos da carga descritos pelo caminhoneiro.

## Como rodar

Basta criar um arquivo na raiz do repositório com um arquivo nomeado 'openai_token.env' e nesse arquivo deve conter uma única linha com o seguinte conteúdo

```
OPENAI_KEY=000000000000000000000000000000000000000000000000000
```
Não esqueça de substituir os '0' no arquivo por uma chave válida de acesso a API da openai.

No repositório, também há um arquivo de requirements com as bibliotecas necessárias para rodar o notebook com o comando:
```
pip insall -r requirements.txt
```

Por fim, basta abrir o arquivo no jupyter lab ou jupyter notebook e executar.

