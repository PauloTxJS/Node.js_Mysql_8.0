# Node.js_Mysql_8.0
Resolução de problemas de conexão.

### Instalar o drive do mysql.
https://www.npmjs.com/package/mysql

### O ERRO!
A partir da versão 8 do mysql, ao tentar realizar a conexão, você receberá um erro sugerindo que o mysql deve ser atualizado. O problema na verdade é que você terá que criar um novo usuário no mysql e dar a esse novo usuário as permissões necessárias.

ex.:
### No MySQL siga os passos: 

1º Crie o usuário.

CREATE USER 'paulo'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';

2º Dê as permissões.

GRANT ALL PRIVILEGES ON * . * TO 'paulo'@'localhost';


Pronto! Tente conectar novamente e o problema não ocorrerá novamente.
