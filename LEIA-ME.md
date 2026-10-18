# Post Studio para Android

App Android que abre o Post Studio (a página `app/src/main/assets/index.html`) em tela cheia.
O APK é compilado na nuvem pelo GitHub Actions, então você não precisa instalar o Android Studio.

## Como gerar o APK

1. Crie uma conta e um repositório novo no GitHub (pode ser privado). Ex.: `poststudio-android`.
2. Envie **todo o conteúdo desta pasta** para o repositório, mantendo as subpastas.
   - No computador: no repositório, **Add file → Upload files** e arraste as pastas `app` e `.github` e os arquivos soltos.
   - Se a pasta `.github` não subir, use **Add file → Create new file**, digite
     `.github/workflows/build-apk.yml` como nome e cole o conteúdo do arquivo de mesmo nome.
3. Abra a aba **Actions**. O fluxo "Compilar APK" roda sozinho (de 3 a 6 minutos).
   Se não rodar, escolha "Compilar APK" e clique em **Run workflow**.
4. Quando ficar verde, abra a aba **Releases** (lado direito do repositório) e baixe o **PostStudio.apk**.
5. No celular, abra o arquivo e permita "instalar apps desconhecidos" para o navegador, se o Android pedir.

## O que o app faz a mais que a página

- Botão **Baixar capa**: salva a imagem na galeria, na pasta `PostStudio`.
- Botão **Compartilhar**: abre a janela do Android para enviar a capa direto ao LinkedIn.
- A página roda em endereço seguro (https), então o botão Copiar post funciona.
- Links externos abrem no navegador do celular.

## Observações

- É um APK de teste (assinado com a chave de depuração): serve para instalar no seu celular, não para a Play Store.
- Para trocar o visual ou o texto, edite `app/src/main/assets/index.html` e envie de novo ao GitHub: um novo APK é gerado.
- É preciso internet: o app busca o artigo e as fontes online.
