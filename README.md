# 📋 Texto Rápido — celular → PC

Página web simples para mandar texto do iPhone para o PC (e vice-versa) **sem login**.
Você abre o mesmo link nos dois aparelhos e pronto: o que digitar em um aparece no outro na hora.

## Como funciona

- É um único arquivo HTML estático — não precisa de servidor próprio nem banco de dados.
- As mensagens trafegam pelo [ntfy.sh](https://ntfy.sh), um serviço público e gratuito de mensagens em tempo real.
- Cada "canal" é um código secreto aleatório (ex.: `txt-a8k2j...`) que fica no link. Quem tem o link, participa do canal — funciona como uma senha.
- As mensagens de texto ficam guardadas no ntfy.sh por **~12 horas** e depois somem.
- **Imagens e documentos** também funcionam: use o botão 📎. Limites do servidor gratuito: **15 MB por arquivo** e o arquivo fica disponível por **~3 horas**. Imagens aparecem com preview; documentos, com botão "Baixar".
- Dica iPhone: fotos da Fototeca podem ir no formato HEIC, que o navegador do PC não exibe — nesse caso o app mostra o cartão do arquivo com "Baixar" em vez do preview. Para evitar, tire a foto pela opção de câmera do 📎 ou converta para JPEG.

## Hospedagem gratuita

Você só precisa hospedar 2 arquivos: `index.html` e `qrcode.min.js`.

### Opção A — GitHub Pages (recomendado)

1. Crie uma conta em [github.com](https://github.com) (se ainda não tiver).
2. Crie um repositório novo, ex.: `texto-rapido` (pode ser público).
3. Clique em **Add file → Upload files** e envie `index.html` e `qrcode.min.js`.
4. Vá em **Settings → Pages**, em "Branch" escolha `main` e clique **Save**.
5. Em ~1 minuto seu app estará em `https://SEU-USUARIO.github.io/texto-rapido/`.

## Como usar

1. **No PC:** abra o link do app. Um canal secreto é criado automaticamente.
2. Clique em **"Conectar aparelho"** e copie o link do canal.
3. **No iPhone:** abra esse mesmo link (mande para você mesmo por e-mail/AirDrop uma única vez, ou digite).
4. No iPhone, toque em **Compartilhar → Adicionar à Tela de Início** — vira um ícone de app, sem precisar abrir o Safari toda vez.
5. Digite no celular → aparece no PC (e cada mensagem tem botão **Copiar**). Use 📎 para fotos e documentos.

Dicas:

- Deixe a aba aberta no PC; se permitir notificações, você é avisado mesmo com a aba em segundo plano.
- **"Novo canal"** gera outro código secreto (use se suspeitar que alguém descobriu seu link). Depois é só escanear o QR de novo no celular.

## Privacidade

O texto passa pelo servidor público ntfy.sh sem criptografia de ponta a ponta — o código aleatório do canal é a única proteção (é praticamente impossível de adivinhar, mas não mande senhas ou dados sensíveis por aqui).
