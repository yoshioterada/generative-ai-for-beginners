# 生成 AI アプリケーション・ライフサイクル

すべての AI アプリにとって重要なのは、AI の機能がどれだけ役立つかです。AI は急速に進化しているので、アプリが常に役立ち、信頼でき、そしてしっかりと構築するためには、継続的に監視し、評価し、改善する必要があります。そこで生成 AI のライフサイクルが役立ちます。

生成 AI のライフサイクルは、生成 AI アプリケーションを構築、デプロイ、維持する段階を示す指針です。目標を定め、パフォーマンスを測り、課題を見つけ、解決策を実行するのに役立ちます。さらに、アプリを自分の業界や関係者の倫理や法的基準に合わせるのにも役立ちます。生成AIのライフサイクルに従えば、アプリケーションは常に価値を提供し、ユーザーを満足させます。

## はじめに

この章では、下記の内容を学びます：

- MLOps から LLMOps へのパラダイムシフトを理解
- LLM のライフサイクル
- ライフサイクルのツール

## MLOps から LLMOps へのパラダイムシフトを理解

LLM は AI の新しいツールで、アプリケーションの分析や生成タスクにおいて非常に強力です。しかし、この力は AI や従来の機械学習タスクの効率化に影響を及ぼします。

このツールをうまく使うためには、新しい考え方と適切なやり方が必要です。古い AI アプリは「ML アプリ」、新しい AI アプリは「生成 AI アプリ」または単に「AI アプリ」と呼ばれ、その時代で使われている技術や方法を反映しています。これにより、私たちの考え方がいろいろな面で変わっていきます。以下の比較をご覧ください。」

![LLMOps vs. MLOps comparison](../../images/01-llmops-shift.png?WT.mc_id=academic-105485-yoterada)

Notice that in LLMOps, we are more focused in the App Developers, using integrations as a key point, using "Models-as-a-Service" and thinking in the following points for metrics.

LLMOps では、アプリ開発者に重点を置き、統合を重要なポイントとして「モデル・アズ・ア・サービス」を活用します。メトリクスに関しては、次のポイントを検討します。

- 品質: 応答の質
- 有害性: 責任ある AI
- 誠実さ: 応答の信頼性（意味が通じるか？正しいか？）
- コスト: ソリューションの予算
- 遅延: トークン応答の平均時間

## LLM のライフサイクル

まず、ライフサイクルと変更点を理解するために、次の図をご覧ください。

![LLMOps infographic](../../images/02-llmops.png?WT.mc_id=academic-105485-yoterada)

ご覧のとおり、これは通常の MLOps のライフサイクルとは異なります。LLMには、プロンプト、品質向上のためのさまざまな技術（ファインチューニング、RAG、メタプロンプト）、責任あるAIに関する異なる評価と責任、そして新しい評価指標（品質、有害性、誠実さ、コスト、遅延）など、多くの新しい要件があります。

例えば、私たちがどのようにアイデアを出すか見てみましょう。プロンプト・エンジニアリングを利用して、いろいろな LLM で実験し、仮説が正しいかどうかを試してみたいと思います。

これは直線的な流れではなく、全体を包括するサイクルで繰り返し行われる統合されたループです。

その手順をどのように調べられるか考えてみましょう。ライフサイクルを作る方法を詳しく見てみましょう。

![LLMOps Workflow](../../images/03-llm-stage-flows.png?WT.mc_id=academic-105485-yoterada)

This may look a bit complicated, lets focus on the three big steps first.

少し複雑に見えるかもしれないため、まずは3つの大きなステップに注目しましょう。

1. アイデアを検討/探求: ここではビジネスのニーズに合わせて探求できます。プロトタイプを作成し、[PromptFlow](https://microsoft.github.io/promptflow/index.html?WT.mc_id=academic-105485-yoteradat)を作成して、仮説に対して十分効率的かどうかテストします。
1. ビルド/拡張: 実装、ここでは大きなデータセットに対してファインチューニングや RAG のような技術を使って、解決策の堅牢性を確認します。仮にうまくいかない場合は、フローに新しいステップを追加したり、データを再構築したりして再実装することで改善できるかもしれません。フローとスケールをテストし、動作してメトリクスを確認すると、次のステップに進めます。
1. 運用化: 統合、システムにモニタリングとアラートシステムを追加し、アプリケーションにデプロイと統合を行います。

次に、セキュリティ、コンプライアンス、ガバナンスに焦点を当てた全体的な管理サイクルがあります。

おめでとうございます、これで AI アプリの準備が整いました。実際に試してみたい場合は、[Contoso Chat Demo](https://nitya.github.io/contoso-chat/?WT.mc_id=academic-105485-yoterada) をご覧ください。

次に、どのようなツールを利用できるか確認してみましょう。

## ライフサイクルのツール

ツールとして、Microsoftは [Azure AI Platform](https://azure.microsoft.com/solutions/ai/?WT.mc_id=academic-105485-yoterada) と [PromptFlow](https://microsoft.github.io/promptflow/index.html?WT.mc_id=academic-105485-yoteradat) を提供しており、これらのツールはサイクルの実装を簡単にし、すぐに使えます。

[Azure AI Platform](https://azure.microsoft.com/solutions/ai/?WT.mc_id=academic-105485-yoterada)では[AI Studio](https://ai.azure.com/?WT.mc_id=academic-105485-yoterada)を利用できます。AI Studio はウェブポータルで、モデル、サンプル、ツールを検索できます。リソースの管理、UI開発フロー、コードファースト開発のための SDK や CLI もオプションで提供しています。

![Azure AI possibilities](../../images/04-azure-ai-platform.png?WT.mc_id=academic-105485-yoterada)

Azure AIを使うと、複数のリソースを利用して、運用、サービス、プロジェクト、ベクター検索、データベースのニーズを管理できます。

![LLMOps with Azure AI](../../images/05-llm-azure-ai-prompt.png?WT.mc_id=academic-105485-yoterada)

PromptFlow を利用して、概念実証（POC）から大規模アプリケーションまで構築しましょう。

- VS Code を使い、視覚的で機能的なツールを使いアプリを設計し、実装
- 簡単にアプリのテストとファインチューニング（微調整）を行い、高品質な AI アプリを実装
- Azure AI Studioを使ってクラウドと連携したり、素早く統合するためのプッシュやデプロイを行う

![LLMOps with PromptFlow](../../images/06-llm-promptflow.png?WT.mc_id=academic-105485-yoterada)

## お疲れ様でした!　学習を続ける

素晴らしいです。次は [Contoso Chat App](https://nitya.github.io/contoso-chat/?WT.mc_id=academic-105485-yoteradat) を使用して、アプリケーションの構造と概念の使い方を学びましょう。クラウド・アドボケイトがデモでどのようにそれらの概念を追加していくのか確認してください。さらに詳しい内容は、[Igniteのブレイクアウトセッション](https://www.youtube.com/watch?v=DdOylyrTOWg)をご覧ください。

Now, check Lesson 15, to understand how [Retrieval Augmented Generation and Vector Databases](../../../15-rag-and-vector-databases/translations/ja-jp/README.md?WT.mc_id=academic-105485-yoteradat) impact Generative AI and to make more engaging Applications!

続いて、レッスン 15 を確認し、[RAG (Retrieval Augmented Generation) と ベクトル・データベース]が生成 AI にどのような影響を与え、より魅力的なアプリケーションを作れるかヒントを学びましょう！
