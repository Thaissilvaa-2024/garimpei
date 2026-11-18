# Etapa 3: automação no Make (plano gratuito)

Cenário único: **Planilha "fila" → filtro → Instagram ou Pinterest → grava resultado na planilha**.

Regras que o painel já cumpre:
- Só linhas com `status = Aprovado` e `removido` vazio devem ser publicadas.
- `publicar_em_utc` traz o horário em UTC; publicar quando for menor ou igual ao momento atual.
- O Make deve, **antes** de publicar, mudar a linha para `Na fila` (evita duplicidade) e depois para `Publicado` (com `post_url`) ou `Erro` (com `erro`), sempre gravando `atualizado_em` em formato ISO UTC (ex.: `2026-11-12T12:00:00Z`).

Consumo estimado no plano gratuito (1.000 créditos/mês, mín. 15 min entre execuções): 1 crédito por execução para buscar linhas + cerca de 3 por publicação. Execuções a cada 3 horas somam ~240/mês, o que deixa folga. A publicação sai na primeira execução após o horário marcado.

Antes de ativar, precisamos decidir a hospedagem das imagens (o Instagram não aceita links do Google Drive). Veja a conversa.
