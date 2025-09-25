# 深層強化学習講座2025Summer最終課題

## プロジェクト概要（仮作成/テーマも変更の可能性あり）

### テーマ: DQN拡張手法の組み合わせ評価（Ablation Study）

本プロジェクトでは、深層強化学習の基礎となるDQNアルゴリズムに対して、主要な拡張手法である**Double DQN**と**Prioritized Experience Replay**(**PER**)を実装し、それらの効果をベースラインと比較するAblation Study（除去実験）を行います。

### 実験設定

- **環境**: Atari Pong-v5
- **比較モデル**
  1. Vanilla DQN（ベースライン）
  2. DQN + Double DQN
  3. DQN + Double DQN + PER
- **評価指標**: 学習曲線（エピソード報酬の推移）、収束速度、最終性能
- **学習ステップ**: 各モデル100万タイムステップ

### 技術的貢献

1. **Double DQN**: Q値の過大評価問題を解決するため、行動選択と価値評価に異なるネットワークを使用
2. **Prioritized Experience Replay**: TD誤差に基づく重要度サンプリングにより学習効率を向上
3. **Sum Tree**: PER実装のための効率的なデータ構造

### 期待される成果

- 各拡張手法の個別効果の定量的評価
- 手法組み合わせ時の相乗効果の検証
- Atari環境での学習効率改善の実証

## プロジェクト構成

```
drl-2025-final-project/
├── README.md                     # プロジェクト概要
├── src/                          # ソースコード
├── experiments/                  # 実験結果
└── requirements.txt              # 依存関係
```

## 環境要件

- Python 3.12.4
- PyTorch
- Gymnasium
- OpenAI Gym (Atari)
- その他詳細は `requirements.txt` を参照

## ライセンス
このプロジェクトは特定のライセンスの下での公開はしていません。制作者yf591と依頼者以外の者の使用は固く禁じます。