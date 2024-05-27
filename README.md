# LLMの事前学習コード

## 備忘録
[ropeの更新コードをmegatron-deepspeedに反映させる](codes/2_pretrain/original_codes/rotary_pos_embedding.py)


## 環境構築
- 標準コードを参考に構築する
- https://github.com/matsuolab/ucllm_nedo_prod

- カスタムコードの使用
~~~
#データ学習時に､読み込みがshuffleされるコードを無効化 (BTMは学習順序が大切なので｡)
cp codes/2_pretrain/original_codes/gpt_dataset.py codes/2_pretrain/Megatron-DeepSpeed/megatron/data/gpt_dataset.py

#ropeを使う
cp codes/2_pretrain/original_codes/pretrain_gpt.py codes/2_pretrain/Megatron-DeepSpeed/pretrain_gpt.py

~~~

## [2 事前学習](./codes/2_pretrain/)
- 以下の作業を行います｡
  - 事前学習
  - HuggingFace modelへの変換
