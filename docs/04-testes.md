# Roteiro de testes

**A. Painel publicado**
1. Abra o endereço do GitHub Pages no notebook. Importe seu backup JSON e confira produtos e fila.
2. Abra no celular: deve carregar igual, vazio de dados (normal antes da sincronização).

**B. Login e planilha**
3. Dados e backup > cole o ID do cliente > Conectar Google. Esperado: "Sincronizado às HH:MM" e link "Abrir planilha".
4. Na planilha, confira as abas `produtos` e `fila` com os dados.
5. No celular: cole o ID, conecte. Esperado: seus produtos aparecem.

**C. Sincronização nos dois sentidos**
6. No celular, crie uma publicação. No notebook, toque em Sincronizar agora: ela aparece.
7. Exclua um produto no notebook, sincronize, depois sincronize no celular: some nos dois.
8. Edite o mesmo item nos dois aparelhos: vale a edição mais recente.

**D. Segurança**
9. Procure no repositório do GitHub por senhas ou tokens: não deve haver.
10. Desconectar: a sincronização deve parar até conectar de novo.

**E. Make (depois da etapa 3)**: teste com uma linha Aprovada falsa e conta de teste antes do uso real.
