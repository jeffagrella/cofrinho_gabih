# Cofrinho secreto

Página estática de uma página só com senha numérica, contagem regressiva de 60 segundos e reprodução do vídeo `clipe.mp4` depois do acerto.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie `index.html`, `clipe.mp4` e este `README.md` para a raiz do repositório.
3. Em **Settings → Pages**, selecione **Deploy from a branch**, escolha `main` e a pasta `/ (root)`, e salve.
4. Aguarde a publicação e abra a URL mostrada na seção **Pages** das configurações.

O vídeo está referenciado por caminho relativo (`clipe.mp4`), portanto mantenha-o ao lado de `index.html`. O arquivo tem cerca de 28,4 MiB e fica abaixo do limite de 100 MB por arquivo do GitHub. Para evitar o limite de 25 MiB de envio pelo navegador, use Git pela linha de comando ou GitHub CLI para enviar o vídeo.

## Personalizar a senha

A senha atual é `230526`. Para alterá-la, edite `const code='230526'` no script de `index.html` antes de publicar.

**Nota:** a senha é uma brincadeira visual, não controle de acesso. Como a verificação acontece no navegador, qualquer pessoa pode inspecionar o código da página e descobrir a senha.

## Arquivos

- `index.html` — interface, estilos, cronômetro e lógica da senha.
- `clipe.mp4` — vídeo reproduzido após o acerto.



## Contagem de tentativas

A página guarda no localStorage deste navegador o número de tentativas enviadas. Essa contagem não é centralizada, não identifica visitantes e não coleta endereços IP. Ela pode ser reiniciada ao limpar os dados do site no navegador.

