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

## Publicação na Vercel

Produção: <https://trabalho-final-urna-eletronica.vercel.app>.

Repositório público: <https://github.com/deyvideugenio/trabalho-final-urna-eletronica>, branch `main`.

O projeto `trabalho-final-urna-eletronica` foi publicado pela Vercel CLI. Configuração: **Framework Preset: Other**, raiz do repositório, **Output Directory: .**, comandos de build e instalação vazios, sem variáveis de ambiente de aplicação.

**Pendente: conectar o GitHub para deploys automáticos.** A tentativa de conexão pela CLI foi recusada pela Vercel; isso não impede o acesso ao site publicado. Para concluir:

1. Abra [Settings → Git do projeto](https://vercel.com/deyvids-projects-21a8200b/trabalho-final-urna-eletronica/settings/git).
2. Conecte o GitHub e selecione `deyvideugenio/trabalho-final-urna-eletronica`. Se o repositório não aparecer, confira em **GitHub → Settings → Applications → Installed GitHub Apps → Vercel → Configure** se o aplicativo tem acesso a esse repositório.
3. Confirme `main` como branch de produção. Após o vínculo, novos pushes nessa branch podem publicar automaticamente.

Enquanto o vínculo estiver pendente, atualize a produção a partir desta pasta autenticada e vinculada:

```sh
npx vercel deploy --prod
```

Referências: [sites sem build](https://vercel.com/docs/builds/configure-a-build#skip-build-step) e [integração com GitHub](https://vercel.com/docs/git/vercel-for-github).

## Verificação funcional

Confira o carregamento das imagens e seções, a troca automática e os controles do carrossel, os sete botões de copiar, o destaque dos exemplos Python e a lupa do fluxograma em desktop. Verifique também a leitura em telas móveis. No celular, o fluxograma pode ser aberto em uma nova aba.

Validação local automatizada em Chrome: estrutura HTML, sintaxe JavaScript, imagens, carrossel automático e manual, sete operações de cópia, destaque Python, exibição/ocultação da lupa e layout em 320, 390, 768, 1024 e 1440 pixels. O texto do material foi comparado com o original e permanece integralmente preservado.

O Tailwind Play CDN emite uma recomendação de build para produção. Ele foi mantido para preservar a implementação original sem introduzir uma etapa de build; o aviso não bloqueia a página. Os recursos externos continuam sujeitos à disponibilidade de seus provedores.
