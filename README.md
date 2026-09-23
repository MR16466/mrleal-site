# MR Leal Serviços Contábeis — Site institucional

Site institucional da MR Leal Serviços Contábeis (Teresina e Sul do Piauí), publicado via GitHub Pages.

## Como publicar

1. Vá em **Settings → Pages** neste repositório
2. Em "Source", selecione a branch `main` e a pasta `/root`
3. Salve. Em alguns minutos o site fica disponível em:
   `https://<seu-usuario>.github.io/<nome-do-repositorio>/`

## Como atualizar o site

Sempre que quiser publicar uma nova versão:

1. Substitua o arquivo `index.html` pela versão atualizada
2. Faça commit e push para a branch `main`
3. O GitHub Pages atualiza automaticamente em 1–2 minutos

## Domínio próprio (opcional)

Se quiser usar um domínio como `mrlealcontabilidade.com.br` em vez do link do GitHub:

1. Crie um arquivo chamado `CNAME` (sem extensão) na raiz do repositório, contendo apenas:
   ```
   mrlealcontabilidade.com.br
   ```
2. No painel do seu domínio (ex: registro.br), aponte os registros DNS para o GitHub Pages:
   - Registro tipo `A` apontando para: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Ou um registro `CNAME` apontando para `<seu-usuario>.github.io`
3. Em Settings → Pages, adicione o domínio customizado

## Verificação de integridade (segurança)

Este repositório tem um workflow (`.github/workflows/verify-contact.yml`) que roda a cada 6 horas e confere se o telefone e o e-mail de contato publicados no site ainda são os esperados. Se alguém alterar esses dados sem passar por aqui (ex: defacement ou sequestro do painel de hospedagem), o workflow falha e o GitHub envia um e-mail de alerta automaticamente.
