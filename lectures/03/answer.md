# 第3回 解答

## 演習

- 第1回（素のLLM）とエージェントの回答の違い：
- `--trace` で見えたツール呼び出し（ツール名と引数）：
- 1つの質問での LLM 呼び出し回数（`requests`）：
- 追加したツールと、docstring に書いた説明：

## 宿題

- 取り組んだレベル：基礎

- やったこと：
　def search_glossaryのdocstringについて、「query には調べたい用語を１つだけ入れる」→ 「query には調べたい用語をまとめて入れる」に修正

- 結果：
（変更前）
[tool call]   search_glossary({'query': 'LoRA'})
[tool call]   search_glossary({'query': 'QLoRA'})
（変更後）
[tool call]   search_glossary({'query': 'LoRA QLoRA'})

上記のように、LoRAとQLoRAを１回でまとめて検索するように対応が変化した。

- 気づき・疑問：
今回の演習で、Agentがtoolを呼び出している事実、呼び出した回数もフォローできること、呼び出し方も指示ができることを理解した。回答内容自体はほぼ変化しなかった。