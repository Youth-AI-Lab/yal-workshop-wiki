# Workshop 5 - Organise what it knows (one page)

**Question of the day: how do you keep knowledge clean when it grows?**
Full page: [README.md](README.md). Setup and common problems: [SETUP.md](SETUP.md).

| Score | When |
|---|---|
| **2** | Right, and it says where it comes from. |
| **1** | Honest but not enough: "I don't know" although the answer exists, no source, or partly right. |
| **0** | Wrong or invented. |

## 1. Welcome (20 min)

1. Idle timeout not set yet on this account? First: [SETUP.md, step 1](SETUP.md#step-1---let-the-codespace-wait-for-you).
2. Open the Codespace: **https://codespaces.new/Youth-AI-Lab/yal-workshop-wiki** → **Create codespace**.
3. Terminal 1: `workshop-login`, paste the key once, Enter → you see `Key OK`. Then `workshop bare`:
   first screens, trust the folder (down arrow, `Yes, I trust this folder`), `Ctrl+C` twice.
4. Drag `my-work.zip` into the file list (the newest: maybe `my-work (1).zip`, then type its exact
   name between quotes). Terminal 1: `workshop-start 5 --from my-work.zip` (without a save:
   `workshop-start 5`) → `saved on …` is the end of workshop 4? Older: tell the facilitator. Then
   `Ready for workshop 5`. The first `workshop E` asks again to trust the folder: **down arrow**,
   `Yes, I trust this folder`, Enter.
5. Terminal 2: `openwebui start`. Do not wait: it ends by itself.

## 2. The wiki (30 min)

1. `wiki/index.md`, then `wiki/wildfire-prevention-ordinance-montoro.md`, with `Ctrl+Shift+V`:
   footnotes. Without the preview: `sources` and `generated` in the header.
2. `wiki/log.md`: choose one `Contradiction` line, find its two sources.
3. Your number: 81 (80 if your page was refused). In `summaries/index.md`, your line says
   (human-reviewed). Without a save, or no line there: Benevento, the number of
   `corpus/8N-benevento-aib-2026.pdf`, usually 80. Write down the pages you expect it to feed. Terminal 1: `wiki-graph --highlight 81` → `No page cites a document…`
4. `workshop E`: `ingest summaries/81-….md into the wiki` (without a save:
   `ingest corpus/80-benevento-aib-2026.pdf into the wiki`) → `Skill(ingest)`. Only what you signed,
   or the official text. Read each write, **1. Yes**, never 2. Read the report. Leave.
5. `wiki-graph --highlight 81` → `In orange: …`. `wiki/graph.md`, `Ctrl+Shift+V`: look at the orange.
6. Predict: 3, 10, 11, 12 better in E? A smaller gauge than in C? Terminal 2, once `openwebui start`
   has finished: `replay E`.

## 3. The lint (15 min)

1. New `workshop E`: `lint the wiki` → `Skill(lint)`. Watch the gauge. Once per session.
2. `Proposals`, at the end of the report. Open the page of one finding: a real problem, or taste?
3. Choose one or two, or none, and say why. Tell the model, read each change, **1. Yes**. Leave.

## 4. The graph (25 min)

1. Terminal 1, outside a conversation: `wiki-explore` → a new tab (if not: Ports tab, 8765, Open in
   Browser). Tick or untick the `Communities`, type `Montoro` in `Search nodes...`, click a node.
2. `wiki/graphify-out/GRAPH_REPORT.md`, `Ctrl+Shift+V`: `Corpus Check`, `Surprising Connections`.
3. `wiki-explore path "Montoro protection strips" "Obligations légales de débroussaillement"`, then
   `wiki-explore explain "Montoro protection strips"`. `[INFERRED]`: guessed by the model.
4. Check it, side by side, with `Ctrl+F`: `corpus/text/71-montoro-ordinanza-78-2026.md` (`metri venti`,
   `5 metri`) and `corpus/text/22-service-public-debroussaillement.md` (`50 mètres`, `200 mètres`). Who,
   around what? Not your language: find the figure, read the wiki page. **Your verdict, in one sentence.**
5. `wiki-explore path "Benevento" "Montoro"` → `No node matching 'Benevento' found.`: a snapshot.
   Does the graph make the chatbot faster? Discuss, then see the table in the README.

## 5. The chatbot you built (20 min)

1. `score E 3 10 11 12` (no question 12: `score E 3 10 11`).
2. `scores.md`: the rows, not the Total. 3, 11, 12: C against E. 10: earlier columns against E.
   As you predicted?
3. `chatbot-export --name "<your chatbot>"` → right-click on the `.zip` → **Download...**.
4. Terminal 2: `openwebui chatbot --name "<your chatbot>"` → ask your question 12.
5. `workshop-save` → right-click on `my-work.zip` → **Download...** (keep the newest). Then the exit card, alone. To go on: [the guides](https://github.com/Youth-AI-Lab/yal-workshop-kit#going-further).

**Leave a conversation:** `Ctrl+C` twice. **Copy / paste in the terminal:** `Ctrl+Shift+C` /
`Ctrl+Shift+V` (`Cmd+C` / `Cmd+V` on a Mac). **Never make port 3000 public.**
