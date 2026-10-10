# Amigo de Merda BR

Site de jogo de festa em português, com salas por código, perguntas personalizadas, votos por jogador e placar final.

## Arquivos
- `index.html`: site.
- `schema.sql`: estrutura inicial do banco de dados e políticas de acesso para protótipo.

## Para publicar gratuitamente

### 1. Criar o banco online
1. Crie um projeto em https://supabase.com/
2. Abra **SQL Editor**, cole o conteúdo de `schema.sql` e execute.
3. Em **Project Settings → API**, copie a **Project URL** e a chave **anon/public**.
4. Abra `index.html` e substitua:
   - `COLE_AQUI_A_URL_DO_SEU_PROJETO`
   - `COLE_AQUI_A_CHAVE_ANON_PUBLICA`
5. Em Database → Publications, confira se `rooms`, `players`, `questions` e `votes` estão habilitadas em `supabase_realtime`.

### 2. Publicar o site
1. Crie uma conta em https://github.com/ e um repositório novo.
2. Envie `index.html` para o repositório (e os outros arquivos se quiser guardar o projeto).
3. Crie uma conta em https://vercel.com/, escolha **Add New → Project**, importe o repositório e clique em **Deploy**.
4. O Vercel fornecerá uma URL pública para mandar aos amigos.

## Importante
Este é um MVP/protótipo. O SQL inclui políticas permissivas para facilitar testes e não é adequado para um serviço público sem endurecimento de segurança. Antes de abrir para qualquer pessoa, adicione autenticação ou códigos de acesso seguros, políticas RLS restritas, validação de votos no servidor e limites contra spam. A chave `anon/public` é destinada ao cliente; nunca coloque uma `service_role` key no site. O modo de votação usa a mesma tela por participante e requer que o anfitrião avance as perguntas. Teste com um grupo pequeno antes de divulgar.
