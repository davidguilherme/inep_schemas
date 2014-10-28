INEP Schemas
============

Esse repositório contém schemas para converter os micro dados do inep que estão no formato de largura fixa para o formato CSV.

Pré-requisitos
--------------
- Python - Linguagem de programação, já vem instalado em todas as distribuições linux populares;
- Pip - Biblioteca python para gerenciamente de pacotes python;
- CSVKit - Biblioteca python para manipulação de arquivos em csv.

Instalando
----------

Instale o pip:
```
$ sudo apt-get install python-pip
```

Instale o csvkit:
```
$ sudo pip install csvkit
```

Pronto!

Convertendo
------------
Utilize o utilitário `in2csv`, da lib csvkit, que converte entradas de vários formatos para o formato csv. Como alguns dados do INEP se encontram no formato de largura fixa é necessário um arquivo de schema no formato .csv.

```
$ in2csv -e [encoding] -f [format] -s [schema-file] [FILE] > [CSV File]
```

Exemplo de formato do schema file:
```
column,start,length
name,0,30
birthday,30,10
age,40,3
```

Contribuindo
------------
Os dados SAS dos microdados do inep seguem o seguinte formato:
```
@[start] [COLUMN] [length].
```

Lembrando que a primeira posição no SAS é o número 1, e no schema file é o 0, ou seja, é necessário a subtração do do campo start na hora de criar o schema file.

Para contribuir:
- Fork o repositório;
- Crie uma branch com o nome da alteração;
- Commit as alterações;
- Solicite um Pull Request.





 
