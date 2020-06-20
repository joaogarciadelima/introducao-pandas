# Instalação Python



[Vá até a página de downloads do site oficial](https://www.python.org/downloads/ "Python´s downloads page") e baixe a última versão estável.

![alt](img/donwload_python.png)


## Ambientes Virtuais

É altamente recomendável que você isole o seu ambiente de desenvolvimento para que seja reproduzível e fique organizado.

Você pode usar o pip que já vem por padrão ou usar algum outro gerenciador de dependências como o poetry, pyenv ou pipenv.

Para criar um ambiente virtual usando o pip abra o prompt de comando dentro da pasta do seu projeto e digite:

No windows:

```
python -m venv .venv

```
Esse comando irá criar o ambiente virtual dentro do seu projeto.

Após isso é só você ativar o ambiente virtual digitando

```
 .venv\Scripts\activate

```

Você confere se o ambiente virtual foi ativado observando se o nome do seu projeto aparece na sua linha de comando como abaixo:

```
(introducao-pandas) C:\python_projects\introducao-pandas>

```

Com o ambiente virtual ativado você já pode fazer as instalações das bibliotecas necessárias ao seu projeto usando o pip, como abaixo para instalar o pandas:

```
(introducao-pandas) C:\python_projects\introducao-pandas>pip install pandas

```

O pip é muito usado e você o encontrará na maioria dos projetos python. Mas o gerenciamento das versões pode ser um processo um pouco trabalhoso que por padrão é feito em um arquivo txt chamado requirements.txt. Você pode criar esse arquivo com o comando abaixo:

```
(introducao-pandas) C:\python_projects\introducao-pandas>pip freeze > requirements.txt

```

Note que é um processo manual. Por esse motivo existem outras opções como o pipenv, que é o que tenho usado, onde ele já faz a gestão das dependências de forma mais automática.

Para instalar o pipenv fora do seu ambiente virtual digite o comando:

```
C:\python_projects\introducao-pandas>pip install pipenv

```

Depois disso é importante que você saia do prompt e entre novamente para conferir se foi reconhecido:

```
C:\python_projects\introducao-pandas>pipenv

```

Outra opção interessante e que eu uso para melhor organização é setar para que todos os ambientes virtuais sejam criados dentro do projeto. Para isso é necessário que você adicione uma variável de ambiente às suas variáveis de ambiente no windows:

```
PIPENV_VENV_IN_PROJECT com o valor de 1

```

Assim ao instalar qualquer lib no seu projeto se não houver ainda um ambiente virtual criado ele criará na raiz do seu projeto.
