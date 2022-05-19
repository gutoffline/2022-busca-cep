# 2022-busca-cep
 Aplicação que consome uma API de CEP e retorna o endereço do CEP enviado

Essas duas linhas são iguais
- `document.querySelector("#pesquisar")`
- `document.getElementById("pesquisar")`

## Adicionando um evento
A linha abaixo fará com que um "ouvidor de eventos" seja criado e ao identificar o evento *click* para o botão, seja então executado a função desse ouvidor.

`document.getElementById("pesquisar").addEventListener("click",function(){
    BuscarCEP()
})`


## API de CEP

**URL:** https://viacep.com.br/

**Chamada:** viacep.com.br/ws/01001000/json/

**Retorno:**
```
{
  "cep": "13455-186",
  "logradouro": "Rua Noruega",
  "complemento": "de 1/2 a 99998/99999",
  "bairro": "Jardim Cândido Bertini",
  "localidade": "Santa Bárbara D'Oeste",
  "uf": "SP",
  "ibge": "3545803",
  "gia": "6063",
  "ddd": "19",
  "siafi": "7017"
}
```

## Desenvolvimento
1. Pegar o CEP do formulário
2. Fazer a chamada para a API passando o cep
3. Preencher o parágrafo com as informações de Rua/Avenida, Bairro, Cidade e Estado
