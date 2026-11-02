# FOOTBALL LEGACY v1.1

O registro definitivo das suas lendas. Aplicativo offline-first para organizar carreiras de futebol do FIFA e PES.

## Funcionalidades
- Dossiês de Sommer, Renzo Varela e Alex Kuroaxi.
- Abas por jogador: visão geral, temporadas, competições, partidas, conquistas e recordes.
- Registro rápido e completo de partidas. Jogos oficiais e partidas da Seleção atualizam os totais automaticamente; amistosos e pré-temporada ficam identificados separadamente.
- Exclusão de partidas registradas reverte os números que aquela partida adicionou.
- Hall da Fama com rankings automáticos por gols e títulos e ranking personalizado.
- Comparação de duas ou três carreiras.
- Cadastro de temporadas, competições, títulos, prêmios e recordes.
- Backup e restauração em JSON.
- Armazenamento local no aparelho.

## Desenvolvimento
- Vite + Capacitor 7.
- `npm install` instala dependências.
- `npm run build` gera a versão web em `dist/`.
- GitHub Actions pode gerar APK Android de depuração.

## Instalação e atualização
A v1.1 usa um identificador Android separado (`com.footballlegacy.app.v11`) para permitir manter a v1.0 instalada enquanto os dados são transferidos por backup JSON. O workflow mantém a chave de assinatura de depuração em cache para permitir atualizações futuras da v1.1 sem trocar a assinatura.

## Dados
Os dados são guardados em `localStorage` na chave `fl_db`. Faça backup antes de atualizar. A migração da versão 1.0 atualiza os dados-base antigos de Alex Kuro para o dossiê mais recente, sem remover o histórico de partidas já salvo.

## Observação
A versão 1.1 ainda não possui sincronização em nuvem. O backup JSON é o meio de transportar os dados entre aparelhos.
