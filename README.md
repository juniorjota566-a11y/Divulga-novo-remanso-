# Divulga Novo Remanso — V3

Esta versão adiciona notificações de novos cadastros no painel administrativo em tempo real.

## Como iniciar
1. Instale Node.js 18+.
2. Abra este diretório no terminal.
3. Execute `npm start`.
4. Abra `http://localhost:3000`.
5. Painel: `http://localhost:3000/admin.html`.

## Senha
A senha padrão é `troque-esta-senha`. Antes de publicar, defina uma senha forte:
`ADMIN_PASSWORD="SUA_SENHA" npm start`

## Notificações
- O painel mantém uma conexão em tempo real (SSE).
- Quando um cadastro chega, aparece um aviso visual imediatamente.
- O navegador pode mostrar uma notificação do sistema se você clicar em “Ativar notificações do navegador” e conceder permissão.
- O painel também permite ligar/desligar o som.

**Importante:** em `localhost`, isso serve para testes. Para receber notificações no celular mesmo quando o painel estiver fechado, o app precisa ser publicado em um domínio com HTTPS e usar um serviço de push (por exemplo, Web Push/FCM/OneSignal). Esta V3 deixa a base pronta para essa etapa, mas não inventa credenciais nem envia push externo sem configuração.

## Dados
Os cadastros ficam em `data.json`. Para produção, recomenda-se migrar para SQLite/PostgreSQL e usar autenticação de sessão em vez de senha enviada no cabeçalho.

Não há campo nem upload de fotos de empresas; somente a logo do Divulga Novo Remanso é usada.
