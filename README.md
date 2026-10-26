# Image Converter Pro — Android

App Android nativo em Kotlin para escolher imagens, definir dimensões em pixels e salvar arquivos PNG na galeria, em `Pictures/ImageConverterPro`.

## Tamanhos rápidos
125×125, 128×128, 140×200, 256×256, 512×512 e 1920×1080. Também permite largura e altura personalizadas.

## Criar APK sem computador (GitHub Actions)
1. Entre em github.com pelo navegador do celular e crie um repositório novo, preferencialmente privado.
2. Envie **o conteúdo da pasta `ImageConverterPro`** para a raiz do repositório, inclusive a pasta oculta `.github`. No celular, pode ser mais fácil usar a opção de upload de arquivos no navegador em modo desktop, ou um app Git compatível com pastas.
3. Abra a aba **Actions**, selecione **Gerar APK Android** e toque em **Run workflow** (se o envio para main já iniciou uma execução, basta aguardar).
4. Quando a execução estiver verde, abra-a e baixe o artefato **ImageConverterPro-APK**.
5. Extraia o ZIP do artefato e instale `app-debug.apk`. O Android pode solicitar permissão para instalar apps desse navegador/gerenciador de arquivos.

O APK é uma compilação *debug*, adequada a testes pessoais, não uma versão assinada para distribuição em loja. A execução depende da disponibilidade do GitHub Actions e de suas dependências.

## Compilar no PC
Use JDK 17, SDK Android 35 e Gradle 8.10.2. Execute `gradle :app:assembleDebug`.

## Limitações
Não há APK já compilado neste pacote. Exportação limitada a 20 megapixels por imagem; dimensões até 8192 px. Tamanhos rápidos alteram a proporção quando necessário. Orientação EXIF e formatos menos comuns podem precisar de melhorias futuras.
