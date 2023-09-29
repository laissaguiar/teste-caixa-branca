# teste-caixa-branca
1 – Na linha 13 depois de 127.0.0.1, deve conter o número 3306, que é a porta de entrada.
2 – A linha 12 deve ser removida.
3 - Na linha 15 deveria ser “}catch (SQLException e) {“. E também adicionar embaixo uma linha como por exemplo: “JOptionPane.showMessageDialog(null, “ConexaoDAO” + erro.getMessage());” para caso de erro, aparecer na tela um aviso. 
4 – Ao invés de ser: 
sql += "select nome from usuarios ";
        sql +="where login = " + "'" + login + "'";
        sql += " and senha = " + "'" + senha + "';";
Isso tudo poderia ser escrito na linha 20 como “String sql = “select nome from usuários Where login = ? and senha = ?;”;”.
5 – Na linha 32 também substituir por:
}catch  (SQLException e) {
JOptionPane.showMessageDialog(null, “ConexaoDAO” + erro.getMessage());
E assim finalizando com:
}
Return result;
}
