# Etapa 2: login Google e planilha (gratuito, sem chaves no código)

O painel usa o login oficial do Google e o escopo `drive.file`: ele só enxerga arquivos que ele mesmo criou. A planilha "Garimpei Pra Você - Dados" é criada automaticamente. Não existe senha nem "client secret" neste fluxo.

1. Acesse console.cloud.google.com com a sua conta Google e crie um projeto (ex.: `garimpei`). Não precisa ativar cobrança.
2. Em **APIs e serviços > Biblioteca**, ative **Google Sheets API** e **Google Drive API**.
3. Em **Google Auth platform** (ou "Tela de consentimento OAuth"):
   - Branding: nome do app e seu e-mail.
   - Público: **Externo**, mantenha em **Teste** e adicione **seu e-mail** como usuário de teste.
   - Acesso a dados: adicione o escopo `.../auth/drive.file`.
4. Em **Clientes > Criar cliente > Aplicativo da Web**. Em *Origens JavaScript autorizadas* coloque `https://SEU-USUARIO.github.io` (só o domínio, sem caminho). Não precisa de URI de redirecionamento.
5. Copie o **ID do cliente** (termina em `.apps.googleusercontent.com`). Ele não é segredo, mas não o publique no repositório.
6. No painel publicado: **Dados e backup > ID do cliente OAuth**, cole o ID e toque em **Conectar Google**. Na tela "app não verificado", use *Avançado > continuar* (é o seu próprio app).
7. Repita o passo 6 no celular (o ID é guardado em cada aparelho). A planilha existente é encontrada sozinha.

Os nomes dos menus do Google mudam de tempos em tempos. Se algo divergir, me diga o que aparece na tela.

Comportamento: a sessão Google dura cerca de 1 hora; depois toque em **Sincronizar agora**. Edite produtos e fila **no painel**, não na planilha. Na planilha, só o Make altera status, post_url, erro e atualizado_em.
