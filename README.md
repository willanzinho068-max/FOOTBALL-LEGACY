# FOOTBALL LEGACY — projeto Android

Projeto inicial do aplicativo, com interface em português, dados importados dos três dossiês, registro de partidas, backup JSON e armazenamento local.

## Compilar APK pela nuvem (GitHub Actions)
1. Crie um repositório GitHub e envie todos os arquivos desta pasta.
2. Em Actions, permita executar workflows.
3. O workflow `Android APK` compila um APK de depuração.
4. Baixe o artefato `FOOTBALL-LEGACY-debug-apk` na execução concluída.

O projeto usa Vite + Capacitor 7. O APK de depuração serve para instalação pessoal e testes. Para distribuição pública, será necessário configurar assinatura de release.

## Desenvolvimento local
`npm install`
`npm run build`
`npx cap add android`
`npx cap sync android`

## Limitações desta versão
- Dados são guardados no aparelho via localStorage; exporte backups JSON.
- Sincronização em nuvem ainda não está conectada.
- O service worker habilita cache offline quando hospedado por HTTPS. No APK, os recursos web são empacotados localmente.
- Estatísticas de temporada não especificadas nos dossiês permanecem em branco/zero apenas na apresentação, sem afirmar que sejam dados históricos.
