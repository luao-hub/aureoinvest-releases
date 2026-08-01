# aureoinvest-releases

Canal de distribuicao do **AureoInvest**: e daqui que o `electron-updater` do app baixa as
atualizacoes automaticas.

## Onde ficam os instaladores

Nas **GitHub Releases** deste repositorio, como *assets* — nunca commitados na arvore do git.
Cada release `vX.Y.Z` carrega tres arquivos:

- `aureoinvest-setup-X.Y.Z.exe`
- `aureoinvest-setup-X.Y.Z.exe.blockmap`
- `latest.yml`

## Como publicar

Nao publique nada a mao. No repositorio de codigo (`luao-hub/aureoinvest`), envie uma tag
`vX.Y.Z`: o workflow `.github/workflows/release.yml` compila o instalador NSIS e o envia
para ca via `gh release`.

## Nao commite binarios aqui

Ate julho de 2026 os instaladores eram commitados na raiz deste repositorio. Isso acumulou
~613 MB de binario no historico do git sem servir para nada — os assets de release sao
armazenados separadamente e sao o que o updater consome. Os arquivos foram removidos da arvore.

Se voce precisa de um instalador antigo, pegue na aba **Releases**.