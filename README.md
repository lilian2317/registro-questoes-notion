# registro-questoes-notion[README.md](https://github.com/user-attachments/files/24200467/README.md)
# Registro rápido de % de acertos (Notion + Vercel)

## 1) Variáveis de ambiente (Vercel)
Crie estas variáveis (Project → Settings → Environment Variables):

- `NOTION_TOKEN` = secret da sua integração Notion

IDs das databases (uma por base):
- `DB_TRT_ID`
- `DB_TRE_ID`
- `DB_PGE_ID`

## 2) Compartilhar as databases com a integração
No Notion, abra cada database → Share → convide a integração.

## 3) Propriedades esperadas (nomes exatamente como no Notion)
### TRT
- `Assunto` (title)
- `porcentagem(1)` (number ou text com %)
- `Última Revisão` (date)

### TRE
- `Assunto` (title)
- `Revisão (data do 1 estudo)` (date)
- (opcional) `porcentagem(1)` se existir nessa base (se não existir, o app só atualiza a data)

### PGE
- `Assunto` (title)
- `3° revisão` (text/number com %)
- `Revisão (data do 1 estudo)` (date)

> Se o nome de alguma propriedade for diferente aí no seu Notion, ajuste em `api/_config.js`.

## 4) Rodar local (opcional)
```bash
npm install
npx vercel dev
```

## 5) Deploy
Suba este projeto para o GitHub e importe na Vercel.
