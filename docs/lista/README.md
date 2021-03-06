# Lista Resource

Esta API permite o controle total das listas de contato. Veja as instruções de como realizar a integração abaixo.

Instruções para realizar a integração:

URL
http://app.nectarcrm.com.br/crm/api/1/lista/

Parâmetros de listagem:
* &page=x (integer) Organiza a listagem de objetos por páginas (se colocar -1, lista o máximo de objetos: 200)
* &contact=x (boolean) Retornar tags relacionadas à contato e contato/oportunidade
* &opportunity=x (boolean) Retornar tags relacionadas à oportunidade e contato/oportunidade
* &isFilter=x (boolean) Retornar tags que o usuário pode visualizar junto com inclusão/edição

[Para mais informações, consulte a documentação completa clicando aqui](http://docs.nectarcrm.apiary.io)

Schema Info | [Schema JSON](schema.json)

Propriedade | Tipo | Descricao
------------ | ------------- | -------------
ativo | (boolean) | Marca se essa lista está ativa para utilização
autor | (object) | Autor da criação dessa lista
cor | (string) | Cor da lista para apresentação na lista (HTML Hex: #ffffff)
dataCriacao | (date) | Data de criação dessa lista
descricao | (string) | Descrição dessa lista
id | (long) | Identificador no sistema
nome | (string) | Nome da lista
relacionada | (int) | Constante para indicar qual a relação da TAG. 0 = Contato, 1 = Oportunidade, 2 = Contato/Oportunidade
podeIncluir | (boolean) | Permissão para incluir e utilizar a tag nos objetos
podeVisualizar | (boolean) | Permissão para visualizar e utilizar as tags em filtros

Exemplo
```js
    [
      {
        "ativo": true,
        "autor": {
          "id": 12,
          "login": "contato1@teste.com.br",
          "nome": "Usuario 1"
        },
        "cor": "#0080FC",
	    "dataCriacao":"2016-03-11T10:00:00-03:00",
        "descricao": "Lista que veio do ultimo evento que realizamos"
        "id": 1,
        "nome": "Coffee Break Janeiro/16",
	"relacionada" : 1,
  	"podeIncluir" : true,
  	"podeVisualizar" : true
      }
    ]
```
