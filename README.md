# Trabalho Final: Urna Eletrônica

Página educacional da disciplina de **Estruturas de Dados**, do curso de Análise e Desenvolvimento de Sistemas do **Unilavras**. Reúne as instruções, exemplos, entregáveis e desafios do trabalho final de implementação de uma urna eletrônica em Python.

O site é uma página estática em português do Brasil, com HTML, CSS e JavaScript no `index.html`. Não utiliza framework de aplicação, backend, banco de dados ou etapa de build. O conteúdo e a identidade visual do material original são preservados.

## Executar localmente

Abra `index.html` em um navegador moderno. Para testar a área de transferência em uma origem local confiável, execute na pasta do projeto:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Acesse <http://127.0.0.1:8000>. O Python é apenas uma opção de servidor de desenvolvimento; não é necessário na hospedagem.

É necessário acesso à internet para carregar Tailwind CSS, Font Awesome, Google Fonts, Prism.js e as imagens externas. Os botões de copiar utilizam a área de transferência do navegador; em produção, use HTTPS.

A foto original da urna, obtida no site do TSE, está incorporada ao HTML para evitar o bloqueio de carregamento externo. A origem está registrada em um comentário junto à imagem.

## Publicar na Vercel

1. Acesse <https://vercel.com/new> e importe o repositório `deyvideugenio/trabalho-final-urna-eletronica`.
2. Use o nome de projeto `trabalho-final-urna-eletronica` e a branch de produção `main`.
3. Selecione **Framework Preset: Other** e mantenha **Root Directory: ./**.
4. Em **Build and Output Settings**, ative o override de **Build Command** e deixe o campo vazio. Defina **Output Directory** como `.`. Não é necessário comando de instalação nem variável de ambiente.
5. Clique em **Deploy**. Após conectar o GitHub, novos pushes em `main` atualizam a produção automaticamente.

Configuração baseada na [documentação de sites sem build da Vercel](https://vercel.com/docs/builds/configure-a-build#skip-build-step).

## Verificação funcional

Confira o carregamento das imagens e seções, a troca automática e os controles do carrossel, os sete botões de copiar, o destaque dos exemplos Python e a lupa do fluxograma em desktop. Verifique também a leitura em telas móveis. No celular, o fluxograma pode ser aberto em uma nova aba.

Validação local automatizada em Chrome: estrutura HTML, sintaxe JavaScript, imagens, carrossel automático e manual, sete operações de cópia, destaque Python, exibição/ocultação da lupa e layout em 320, 390, 768, 1024 e 1440 pixels. O texto do material foi comparado com o original e permanece integralmente preservado.

O Tailwind Play CDN emite uma recomendação de build para produção. Ele foi mantido para preservar a implementação original sem introduzir uma etapa de build; o aviso não bloqueia a página. Os recursos externos continuam sujeitos à disponibilidade de seus provedores.
