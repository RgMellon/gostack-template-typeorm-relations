## Permitir criação de clientes

<table>
 <tr>  customers  </tr>
  <tr>
    <td> id  </td>
    <td> name</td>
    <td> email </td>
    <td> created_at </td>
    <td> updated_at </td>
  </tr>
</table>

<br>

**RF**

- Cliente pode gerar novos pedidos de compra;
- Enviar name, email na requisição;

**RN**

- Verificar antes de cadastrar um novo costumer se existe o email;
- Espero que, se exister um email ja cadastrado com o mesmo que estou enviando, retorne um erro;

## Permitir criação de produtos

<!--
@Column("decimal", { precision: 5, scale: 2 })
value: number; -->

**RF**

- Espero que o produto seja cadastrado no banco de dados ao enviar a requisição com
  name, price e quantity

**RN**

- Espero que retorne um erro, se ao cadastrar o produto ele ja exista no banco;
- Utilizar o type decimal na migration para o campo price, passando as propriedades (precision, scaling);

<table>
 <tr>  products  </tr>
  <tr>
    <td> id  </td>
    <td> name</td>
    <td> price </td>
    <td> quantity </td>
    <td> created_at </td>
    <td> updated_at </td>
  </tr>
</table>

## Permitir criação de pedidos (orders)

**RF**

- Espero receber no corpo da request o customer_id;
- Espero receber no corpo da request um array de produtos com a quantidade e o id;

<table>
 <tr>  orders  </tr>
  <tr>
    <td> id  </td>
    <td> customer_id</td>
    <td> created_at </td>
    <td> updated_at </td>
  </tr>
</table>

<br>
<br>

<table>
 <tr>  orders_products  </tr>
  <tr>
    <td> id  </td>
    <td> product_id</td>
    <td> order_id </td>
    <td> price </td>
    <td> quantity </td>
    <td> created_at </td>
    <td> updated_at </td>
  </tr>
</table>

## TO DO

[ x ] criar migrations
[ x ] Criar as entidades e relacionar
[ ] Salvar o usuário
