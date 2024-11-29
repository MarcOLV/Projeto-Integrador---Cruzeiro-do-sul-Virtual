#### projeto-integrador
Projeto Integrador Transdisciplinar em Ciência da Computação II



##### Tela de Login :


![Login](https://user-images.githubusercontent.com/43417699/204143586-77de8e1c-06e7-4df5-a37b-2f16379b29ff.png)

##### Home :

![bem vindo](https://user-images.githubusercontent.com/43417699/204143609-488c6031-491f-4ced-a2be-6538e331483b.png)

##### Cadastro de Usuário :

![image](https://user-images.githubusercontent.com/43417699/204143642-ac9e4f1b-188b-43e1-8e91-860917abadeb.png)

##### Cadastrar lançamentos :

![image](https://user-images.githubusercontent.com/43417699/204143665-3381b789-23e4-4bd0-bff7-df924aee102d.png)

##### Tela de Conculta de Lançamentos :

![image](https://user-images.githubusercontent.com/43417699/204143727-e0681590-3918-4c12-b717-2d0b427b6e48.png)



#### Como subir o projeto : 

1 - Abra a pasta backend no intellj e dê o start na aplicação spring boot

2 - Crie o seu banco e insira as tabelas : 

```
CREATE TABLE financas.usuario
(
	id bigserial NOT NULL PRIMARY KEY,
	nome character varying(150),
	email character varying(100),
	senha character varying(20),
	data_cadastro date DEFAULT NOW()
);
```

```
CREATE TABLE finance.lancamento
(
id bigserial NOT NULL PRIMARY KEY,
descricao character varying(100) NOT NULL,
mes integer NOT NULL,
ano integer NOT NULL,
valor numeric(16,2),
tipo character varying(20) CHECK (tipo in ('RECEITA', 'DESPESA') ) NOT NULL,
status character varying(20) CHECK ( status in ('PENDENTE', 'CANCELADO, EFETIVADO') ) NOT NULL,
id_usuario bigint REFERENCES financas.usuario (id) NOT NULL,
data_cadastro date DEFAULT NOW()
);
```

3- Abra a pasta frontend no Visual studio Code ou sua IDE de preferencia!

4- Abra o terminal dentro da raiz no VS, instale o npm => npm install

5- depois dê o start com => npm start

