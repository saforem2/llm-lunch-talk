# LLMs on Polaris
Sam Foreman
2023-10-10

<script src="https://unpkg.com/shiki"></script>
<script>
  shiki
    .getHighlighter({
      theme: 'dracula',
    })
    const html = shiki.renderToHTML(tokens, {
    fg: highlighter.getForegroundColor('nord'), // Set a specific foreground color.
    bg: highlighter.getBackgroundColor('nord'), // Set a specific background color.
    // Specified elements override the default elements.
    elements: {
      pre({ className, style, children }) {
        return `${children}`
      },
      code({ className, style, children }) {
      return `${children}`
    }
  }
})
</script>


# 

<!-- # {.centeredslide background-image="./assets/massstar_science_highlights_2017_01.png" loading="lazy"} -->
<!-- # {.centeredslide background-image="./assets/p62_cover-edit_CMYK.jpg" loading="lazy"} -->
<!-- # {.centeredslide background-image="./assets/tribology_cover_test_image_06m.png" loading="lazy"} -->
<!-- # {.centeredslide background-image="./assets/6120702714_c9a4cf5d78_o.jpg" loading="lazy"} -->
<!-- # {.centeredslide background-image="./assets/ccm_s23-50_Ye_03B.png" loading="lazy"} -->

<div style="text-shadow: 0px 0px 10px RGBA(0, 0, 0, 0.45); background-color: rgba(8, 42, 123, 0.7); border-radius: 10px; text-align:left; padding: 1.5rem; margin-left: auto; margin-right: auto; line-height: 1.5em!important; box-shadow: RGBA(0, 0, 0, 0.25) 0px 5px 15px;">

<div style="display:flex;">

<span style="font-size: 1.75em; font-weight: 600; border-bottom: 1px solid white; color: #F8F8F8">October
10 – 12, 2023 $\hspace{5pt}$ </span>
<span style="display:inline-block;">![](./assets/anl_logo.svg)</span>

</div>

<span style="font-size: 3.0em; font-weight: 700; color: white">ALCF
Hands-on</span>  
<br>
<span style="font-size: 3.0em; font-weight: 700; color: #FFFFFF">HPC
Workshop</span>

</div>

# Status of Large Language Models

<div id="fig-llms">

![](https://github.com/Hannibal046/Awesome-LLM/raw/main/resources/image8.gif)

Figure 1: Large Language Models have (LLM)s have taken the ~~NLP
community~~ **world** by storm[^1]

</div>

# Emergent Abilities

<div width="66%" style="text-align: center;">

<img src="./assets/emergent-abilities.gif" height="75%" />

[Emergent abilities of Large Language
Models](https://arxiv.org/abs/2206.07682) Yao et al. (2023)

</div>

# Training LLMs

<div layout-valign="bottom">

<table>
<colgroup>
<col style="width: 60%" />
<col style="width: 40%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: center;"><div id="fig-evolution" width="60.0%"
data-layout-align="center" data-fig.extended="false">
<p><img
src="https://github.com/Mooler0410/LLMsPracticalGuide/raw/main/imgs/survey-gif-test.gif"
data-fig.extended="false" /></p>
<p>Figure 2: Visualization from <span class="citation"
data-cites="yang2023harnessing">Yang et al. (2023)</span></p>
</div></td>
<td style="text-align: center;"><div width="40.0%"
data-layout-align="center">
<p><img src="./assets/it_hungers.jpeg" data-fig.extended="false" /></p>
</div></td>
</tr>
</tbody>
</table>

</div>

# Landmark Papers (2017 – Now)

<div class="table-responsive" width="100%"
style="max-height: 550px!important; font-size: 0.9rem;"
data-quarto-disable-processing="true">

<div id="tbl-papers">

|  Date   |       keywords       |     Institute      | Paper                                                                                                                                                                                                              |                                                                                                                       Publication                                                                                                                       |
|:-------:|:--------------------:|:------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| 2017-06 |     Transformers     |       Google       | [Attention Is All You Need](https://arxiv.org/pdf/1706.03762.pdf)                                                                                                                                                  | NeurIPS<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F204e3073870fae3d05bcbc2f6a8e263d9b72e776%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)  |
| 2018-06 |       GPT 1.0        |       OpenAI       | [Improving Language Understanding by Generative Pre-Training](https://www.cs.ubc.ca/~amuham01/LING530/papers/radford2018improving.pdf)                                                                             |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fcd18800a0fe0b668a1cc19f2ec95b5003d0a5035%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2018-10 |         BERT         |       Google       | [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://aclanthology.org/N19-1423.pdf)                                                                                          |  NAACL <br>![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fdf2b0e26d0599ce3e70df8a9da02e51594e0e992%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)   |
| 2019-02 |       GPT 2.0        |       OpenAI       | [Language Models are Unsupervised Multitask Learners](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)                                          |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F9405cc0d6169988371b2755e573cc28650d14dfe%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2019-09 |     Megatron-LM      |       NVIDIA       | [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/pdf/1909.08053.pdf)                                                                                      |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F8323c591e119eb09b28b29fd6c7bc76bd889df7a%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2019-10 |          T5          |       Google       | [Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer](https://jmlr.org/papers/v21/20-074.html)                                                                                       |   JMLR<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F3cfb319689f06bf04c2e28399361f414ca32c4b3%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)   |
| 2019-10 |         ZeRO         |     Microsoft      | [ZeRO: Memory Optimizations Toward Training Trillion Parameter Models](https://arxiv.org/pdf/1910.02054.pdf)                                                                                                       |    SC<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F00c957711b12468cb38424caccdf5291bb354033%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)    |
| 2020-01 |     Scaling Law      |       OpenAI       | [Scaling Laws for Neural Language Models](https://arxiv.org/pdf/2001.08361.pdf)                                                                                                                                    |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fe6c561d02500b2596a230b341a8eb8b921ca5bf2%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2020-05 |       GPT 3.0        |       OpenAI       | [Language models are few-shot learners](https://papers.nips.cc/paper/2020/file/1457c0d6bfcb4967418bfb8ac142f64a-Paper.pdf)                                                                                         | NeurIPS <br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F6b85b63579a916f705a8e10a49bd8d849d91b1fc%3Ffields%3DcitationCount&query=%24.citationCount&label=citation) |
| 2021-01 | Switch Transformers  |       Google       | [Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity](https://arxiv.org/pdf/2101.03961.pdf)                                                                               |   JMLR<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Ffdacf2a732f55befdc410ea927091cad3b791f13%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)   |
| 2021-08 |        Codex         |       OpenAI       | [Evaluating Large Language Models Trained on Code](https://arxiv.org/pdf/2107.03374.pdf)                                                                                                                           |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Facbdbf49f9bc3f151b93d9ca9a06009f4f6eb269%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2021-08 |  Foundation Models   |      Stanford      | [On the Opportunities and Risks of Foundation Models](https://arxiv.org/pdf/2108.07258.pdf)                                                                                                                        |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F4f68e07c6c3173480053fd52391851d6f80d651b%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2021-09 |         FLAN         |       Google       | [Finetuned Language Models are Zero-Shot Learners](https://openreview.net/forum?id=gEZrGCozdqR)                                                                                                                    |   ICLR <br>![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fff0b2681d7b05e16c46dfb71d980cc2f605907cd%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)   |
| 2021-10 |          T0          | HuggingFace et al. | [Multitask Prompted Training Enables Zero-Shot Task Generalization](https://arxiv.org/abs/2110.08207)                                                                                                              |   ICLR <br>![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F17dd3555fd1ccf1141cf984347fa1b3fd6b009ca%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)   |
| 2021-12 |         GLaM         |       Google       | [GLaM: Efficient Scaling of Language Models with Mixture-of-Experts](https://arxiv.org/pdf/2112.06905.pdf)                                                                                                         |   ICML<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F80d0116d77beeded0c23cf48946d9d10d4faee14%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)   |
| 2021-12 |        WebGPT        |       OpenAI       | [WebGPT: Browser-assisted question-answering with human feedback](https://www.semanticscholar.org/paper/WebGPT%3A-Browser-assisted-question-answering-with-Nakano-Hilton/2f3efe44083af91cef562c1a3451eee2f8601d22) |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F2f3efe44083af91cef562c1a3451eee2f8601d22%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2021-12 |        Retro         |      DeepMind      | [Improving language models by retrieving from trillions of tokens](https://www.deepmind.com/publications/improving-language-models-by-retrieving-from-trillions-of-tokens)                                         |   ICML<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F002c256d30d6be4b23d365a8de8ae0e67e4c9641%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)   |
| 2021-12 |        Gopher        |      DeepMind      | [Scaling Language Models: Methods, Analysis & Insights from Training Gopher](https://arxiv.org/pdf/2112.11446.pdf)                                                                                                 |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F68f141724814839d556a989646194be88641b143%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-01 |         COT          |       Google       | [Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/pdf/2201.11903.pdf)                                                                                                      |  NeurIPS<br>![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F1b6e810ce0afd0dd093f789d2b2742d047e316d5%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)  |
| 2022-01 |        LaMDA         |       Google       | [LaMDA: Language Models for Dialog Applications](https://arxiv.org/pdf/2201.08239.pdf)                                                                                                                             |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fb3848d32f7294ec708627897833c4097eb4d8778%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-01 |       Minerva        |       Google       | [Solving Quantitative Reasoning Problems with Language Models](https://arxiv.org/abs/2206.14858)                                                                                                                   | NeurIPS<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fab0e3d3e4d42369de5933a3b4c237780b41c0d77%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)  |
| 2022-01 | Megatron-Turing NLG  |  Microsoft&NVIDIA  | [Using DeepSpeed and Megatron to Train Megatron-Turing NLG 530B, A Large-Scale Generative Language Model](https://arxiv.org/pdf/2201.11990.pdf)                                                                    |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F7cbc2a7843411a1768ab762930707af0a3c33a19%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-03 |     InstructGPT      |       OpenAI       | [Training language models to follow instructions with human feedback](https://arxiv.org/pdf/2203.02155.pdf)                                                                                                        |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fd766bffc357127e0dc86dd69561d5aeb520d6f4c%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-04 |         PaLM         |       Google       | [PaLM: Scaling Language Modeling with Pathways](https://arxiv.org/pdf/2204.02311.pdf)                                                                                                                              |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F094ff971d6a8b8ff870946c9b3ce5aa173617bfb%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-04 |      Chinchilla      |      DeepMind      | [An empirical analysis of compute-optimal large language model training](https://www.deepmind.com/publications/an-empirical-analysis-of-compute-optimal-large-language-model-training)                             | NeurIPS<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fbb0656031cb17adf6bac5fd0fe8d53dd9c291508%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)  |
| 2022-05 |         OPT          |        Meta        | [OPT: Open Pre-trained Transformer Language Models](https://arxiv.org/pdf/2205.01068.pdf)                                                                                                                          |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F13a0d8bb38f739990c8cd65a44061c6534f17221%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-05 |         UL2          |       Google       | [Unifying Language Learning Paradigms](https://arxiv.org/abs/2205.05131v1)                                                                                                                                         |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Ff40aeae3e522ada1f6a9f326841b01ef5c8657b6%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-06 |  Emergent Abilities  |       Google       | [Emergent Abilities of Large Language Models](https://openreview.net/pdf?id=yzkSU5zdwD)                                                                                                                            |   TMLR<br>![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fdac3a172b504f4e33c029655e9befb3386e5f63a%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)    |
| 2022-06 |      BIG-bench       |       Google       | [Beyond the Imitation Game: Quantifying and extrapolating the capabilities of language models](https://github.com/google/BIG-bench)                                                                                |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F34503c0b6a615124eaf82cb0e4a1dab2866e8980%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-06 |        METALM        |     Microsoft      | [Language Models are General-Purpose Interfaces](https://arxiv.org/pdf/2206.06336.pdf)                                                                                                                             |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fa8fd9c1625011741f74401ff9bdc1c584e25c86d%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-09 |       Sparrow        |      DeepMind      | [Improving alignment of dialogue agents via targeted human judgements](https://arxiv.org/pdf/2209.14375.pdf)                                                                                                       |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F74eae12620bd1c1393e268bddcb6f129a5025166%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-10 |     Flan-T5/PaLM     |       Google       | [Scaling Instruction-Finetuned Language Models](https://arxiv.org/pdf/2210.11416.pdf)                                                                                                                              |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F5484d228bfc50efbac6e86677bc2ec2ee4ede1a6%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-10 |       GLM-130B       |      Tsinghua      | [GLM-130B: An Open Bilingual Pre-trained Model](https://arxiv.org/pdf/2210.02414.pdf)                                                                                                                              |   ICLR<br> ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F1d26c947406173145a4665dd7ab255e03494ea28%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)   |
| 2022-11 |         HELM         |      Stanford      | [Holistic Evaluation of Language Models](https://arxiv.org/pdf/2211.09110.pdf)                                                                                                                                     |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F5032c0946ee96ff11a292762f23e6377a6cf2731%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-11 |        BLOOM         |     BigScience     | [BLOOM: A 176B-Parameter Open-Access Multilingual Language Model](https://arxiv.org/pdf/2211.05100.pdf)                                                                                                            |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F964bd39b546f0f6625ff3b9ef1083f797807ef2e%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-11 |      Galactica       |        Meta        | [Galactica: A Large Language Model for Science](https://arxiv.org/pdf/2211.09085.pdf)                                                                                                                              |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F7d645a3fd276918374fd9483fd675c28e46506d1%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2022-12 |       OPT-IML        |        Meta        | [OPT-IML: Scaling Language Model Instruction Meta Learning through the Lens of Generalization](https://arxiv.org/pdf/2212.12017)                                                                                   |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fe965e93e76a9e6c4e4863d145b5c007b540d575d%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-01 | Flan 2022 Collection |       Google       | [The Flan Collection: Designing Data and Methods for Effective Instruction Tuning](https://arxiv.org/pdf/2301.13688.pdf)                                                                                           |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Ff2b0017ddd77fa38760a18145e63553105a1a236%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-02 |        LLaMA         |        Meta        | [LLaMA: Open and Efficient Foundation Language Models](https://research.facebook.com/publications/llama-open-and-efficient-foundation-language-models/)                                                            |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F57e849d0de13ed5f91d086936296721d4ff75a75%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-02 |       Kosmos-1       |     Microsoft      | [Language Is Not All You Need: Aligning Perception with Language Models](https://arxiv.org/abs/2302.14045)                                                                                                         |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Ffbfef4723d8c8467d7bd523e1d0b703cce0e0f9c%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-03 |        PaLM-E        |       Google       | [PaLM-E: An Embodied Multimodal Language Model](https://palm-e.github.io)                                                                                                                                          |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F38fe8f324d2162e63a967a9ac6648974fc4c66f3%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-03 |        GPT 4         |       OpenAI       | [GPT-4 Technical Report](https://openai.com/research/gpt-4)                                                                                                                                                        |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F8ca62fdf4c276ea3052dc96dcfd8ee96ca425a48%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-04 |        Pythia        | EleutherAI et al.  | [Pythia: A Suite for Analyzing Large Language Models Across Training and Scaling](https://arxiv.org/abs/2304.01373)                                                                                                |   ICML<br>![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fbe55e8ec4213868db08f2c3168ae666001bea4b8%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)    |
| 2023-05 |      Dromedary       |     CMU et al.     | [Principle-Driven Self-Alignment of Language Models from Scratch with Minimal Human Supervision](https://arxiv.org/abs/2305.03047)                                                                                 |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fe01515c6138bc525f7aec30fc85f2adf028d4156%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-05 |        PaLM 2        |       Google       | [PaLM 2 Technical Report](https://ai.google/static/documents/palm2techreport.pdf)                                                                                                                                  |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Feccee350691708972370b7a12c2a78ad3bddd159%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-05 |         RWKV         |      Bo Peng       | [RWKV: Reinventing RNNs for the Transformer Era](https://arxiv.org/abs/2305.13048)                                                                                                                                 |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F026b3396a63ed5772329708b7580d633bb86bec9%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-05 |         DPO          |      Stanford      | [Direct Preference Optimization: Your Language Model is Secretly a Reward Model](https://arxiv.org/pdf/2305.18290.pdf)                                                                                             |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F0d1c76d45afa012ded7ab741194baf142117c495%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |
| 2023-07 |       LLaMA 2        |        Meta        | [Llama 2: Open Foundation and Fine-Tuned Chat Models](https://arxiv.org/pdf/2307.09288.pdf)                                                                                                                        |       ![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F104b0bb1da562d53cbda87aec79ef6a2827d191a%3Ffields%3DcitationCount&query=%24.citationCount&label=citation)        |

Table 1: Papers, 2017–\*

</div>

</div>

# Life-Cycle of the LLM

<div layout-valign="center">

<table>
<colgroup>
<col style="width: 45%" />
<col style="width: 55%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: center;"><div id="column-one" width="45.0%"
data-layout-align="center">
<ol type="1">
<li><p>Data collection + preprocessing</p></li>
<li><p><strong>Pre-training</strong></p>
<ul>
<li>Architecture decisions:<br />
<code>{model_size, hyperparameters,</code><br />
<code>parallelism, lr_schedule, ...}</code></li>
</ul></li>
<li><p>Supervised Fine-Tuning</p>
<ul>
<li>Instruction Tuning</li>
<li>Alignment</li>
</ul></li>
<li><p>Deploy (+ monitor, re-evaluate, etc.)</p></li>
</ol>
</div></td>
<td style="text-align: center;"><div id="fig-pretrain-two" width="55.0%"
data-layout-align="center" data-fig.extended="false">
<p><img
src="https://jalammar.github.io/images/gpt3/03-gpt3-training-step-back-prop.gif"
data-fig.extended="false" /></p>
<p>Figure 3: <span class="dim-text"><strong>Pre-training</strong>:
Virtually all of the compute used during pretraining phase.</span></p>
</div></td>
</tr>
</tbody>
</table>

</div>

<div class="footer">

<div style="font-size: 0.7em;">

1.  [Better Language Models and their
    Implications](https://openai.com/research/better-language-models)  
2.  <span class="green-text"></span> [Progress / Artefacts / Outcomes
    from 🌸 Bloom
    BigScience](https://bigscience.notion.site/ebe3760ae1724dcc92f2e6877de0938f?v=2faf85dc00794321be14bc892539dd4f)

</div>

</div>

# Life-Cycle of the LLM: Pre-training

<div id="fig-pretrain-two">

![](https://jalammar.github.io/images/gpt3/03-gpt3-training-step-back-prop.gif)

Figure 4: **Pre-training**: Virtually all of the compute used during
pretraining phase

</div>

# Life-Cycle of the LLM: Fine-Tuning

<div id="fig-pretrain-two">

![](https://jalammar.github.io/images/gpt3/10-gpt3-fine-tuning.gif)

Figure 5: **Fine-tuning**: Fine-tuning actually updates the model’s
weights to make the model better at a certain task.

</div>

# 

<!-- # {.centeredslide} -->

![](./assets/diagrams/transformer.svg)

Vaswani et al. (2017)

# Transformer Architecture

<div layout-valign="center">

<table>
<colgroup>
<col style="width: 43%" />
<col style="width: 2%" />
<col style="width: 54%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: center;"><div id="column-one" width="43.5%"
data-layout-align="center">
<ul>
<li><p>Sequence-to-sequence mapping with <code>matmul</code>s:</p>
<div class="sourceCode" id="cb1"><pre
class="sourceCode python"><code class="sourceCode python"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a>inputs.shape  <span class="op">=</span> [batch, d_model, length]</span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true" tabindex="-1"></a>outputs.shape <span class="op">=</span> [batch, d_model, length]</span></code></pre></div></li>
</ul>
</div></td>
<td style="text-align: center;"><div class="quarto-figure-spacer"
width="2.2%" data-layout-align="center">
<p> </p>
</div></td>
<td style="text-align: center;"><div id="column-two" width="54.4%"
data-layout-align="center">
<p><img src="./assets/diagrams/transformer.svg" /> Transformer
Architecture (<span class="citation"
data-cites="vaswani2017attention">Vaswani et al. (2017)</span>)</p>
</div></td>
</tr>
</tbody>
</table>

</div>

# Data: Input / Output[^2]

- Inputs:
  - text represented by a sequence of integers that map the **tokens**
    in the text

    ``` python
    # integers represent tokens in our text, e.g.
    # text = "not all heroes wear capes"
    # tokens = ["not", "all", "heroes", "wear", "capes"]
    inputs =   [1,     0,     4,        4,      6      ]
    ```

# Data: Input / Output

- Tokens are sub-pieces of the text, which are produced using some kind
  of **tokenizer**[^3].

- We can map tokens to integers using a **vocabulary**:

  ``` python
  vocab = ["all", "not", "heroes", "the", "wear", ".", "capes"]
  # a pretend tokenizer that tokenizes on whitespace
  tokenizer = WhitespaceTokenizer(vocab)
  # encode(s: str) -> list[int]
  ids = tokenizer.encode("not all heroes wear") # ids = [1, 0, 2, 4]
  # we can see what the actual tokens are via our vocab mapping
  # tokens = ["not", "all", "heroes", "wear"]
  tokens = [tokenizer.vocab[i] for i in ids]
  # the decode() method converts back a list[int] -> str
  text = tokenizer.decode(ids) # text = "not all heroes wear"
  ```

# Data: Input / Output

- In short:
  - There is a `vocab` that maps string tokens to integer indicees
  - There is an `encode: str -> list[int]`
  - There is a `decode: list[int] -> str`
- Output:
  - The output is a **2D Array** where `output[i][j]` is the model’s
    **predicted probability** that the token at `vocab[j]` is the next
    token `inputs[i+1]`

# Data: Output

``` python
vocab = ["all", "not", "heroes", "the", "wear", ".", "capes"]
inputs = [1, 0, 2, 4] # "not" "all" "heroes" "wear"
output = gpt(inputs)
# ------------ ["all", "not", "heroes", "the", "wear", ".", "capes"]
# output[0] =  [0.75    0.1     0.0       0.15    0.0   0.0    0.0  ]
# • given just "not", the model predicts the word
#   "all" with the highest probability
# ------------ ["all", "not", "heroes", "the", "wear", ".", "capes"]
# output[1] =  [0.0     0.0      0.8     0.1    0.0    0.0   0.1  ]
# • given the sequence ["not", "all"], the model predicts the word
#   "heroes" with the highest probability
# ------------ ["all", "not", "heroes", "the", "wear", ".", "capes"]
# output[-1] = [0.0     0.0     0.0     0.1     0.0    0.05  0.85  ]
# • given the whole sequence ["not", "all", "heroes", "wear"],
#   the model predicts the word
#   "capes" with the highest probability
```

# Data: Output

- To get a **next token prediction** for the whole sequence, we simply
  take the token with the highest probability in `output[-1]`[^4]:

  ``` python
  vocab = ["all", "not", "heroes", "the", "wear", ".", "capes"]
  inputs = [1, 0, 2, 4] # "not" "all" "heroes" "wear"
  output = gpt(inputs)
  next_token_id = np.argmax(output[-1]) # next_token_id = 6
  next_token = vocab[next_token_id] # next_token = "capes"
  ```

# Generating Text

- Auto-regressive
  - We can generate complete sentences by iteratively generating the
    next token prediction from our model.
  - At each iteration,we append the predicted token back into the input:

``` python
def generate(inputs, n_tokens_to_generate):
    # auto-regressive decode loop
    for _ in range(n_tokens_to_generate):
        # model forward pass
        output = gpt(inputs)
        # greedy sampling
        next_id = np.argmax(output[-1])
        # append prediction to input
        inputs.append(int(next_id))
    # only return generated ids
    return inputs[len(inputs) - n_tokens_to_generate :]
```

# Generating Text (cont’d)

``` python
# "not" "all"
input_ids = [1, 0]
# output_ids = [2, 4, 6]
output_ids = generate(input_ids, 3)
# "heroes" "wear" "capes"
output_tokens = [vocab[i] for i in output_ids]
```

# Training

``` python
def lm_loss(inputs: list[int], params) -> float:
    # the labels y are just the input shifted 1 to the left
    #
    # inputs = [not,     all,   heros,   wear,   capes]
    #      x = [not,     all,   heroes,  wear]
    #      y = [all,  heroes,     wear,  capes]
    #
    # of course, we don't have a label for inputs[-1], so we exclude it from x
    #
    # as such, for N inputs, we have N - 1 langauge modeling example pairs
    x, y = inputs[:-1], inputs[1:]

    # forward pass
    # all the predicted next token probability distributions at each position
    output = gpt(x, params)

    # cross entropy loss
    # we take the average over all N-1 examples
    loss = np.mean(-np.log(output[y]))

    return loss
```

# Parallelism Overview

<div>

> **Current Strategies**
>
> Modern parallelism techniques enable the training of large language
> models

</div>

# Parallelism Concepts[^5]

- **DataParallel (DP)**:
  - The same setup is replicated multiple times, and each being fed a
    slice of the data. The processing is done in parallel and all setups
    are synchronized at the end of each training step.
- **TensorParallel (TP)**:
  - Each tensor is split up into multiple chunks, so instead of having
    the whole tensor reside on a single gpu, each shard of the tensor
    resides on its designated gpu. During processing each shard gets
    processed separately and in parallel on different GPUs and the
    results are synced at the end of the step. This is what one may call
    horizontal parallelism, as the splitting happens on horizontal
    level.

# Parallelism Concepts[^6]

- **PipelineParallel (PP)**:
  - Model is split up vertically (layer-level) across multiple GPUs, so
    that only one or several layers of the model are places on a single
    gpu. Each gpu processes in parallel different stages of the pipeline
    and working on a small chunk of the batch.
- **Zero Redundancy Optimizer (ZeRO)**:
  - Also performs sharding of the tensors somewhat similar to TP, except
    the whole tensor gets reconstructed in time for a forward or
    backward computation, therefore the model doesn’t need to be
    modified. It also supports various offloading techniques to
    compensate for limited GPU memory.
- **Sharded DDP**:
  - Another name for the foundational ZeRO concept as used by various
    other implementations of ZeRO.

# Data Parallelism

- **Data Parallelism**:
  - The simplest and most common parallelism technique. Workers maintain
    *identical copies* of the *complete* model and work on a *subset of
    the data*.
  - `DDP` supported in PyTorch native.
- ZeRO Data Parallel
  - ZeRO powered data parallelism is shown below[^7]

<div style="text-align: center;">

<img src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/parallelism-zero.png" width="75%" />

</div>

# Tensor Parallelism[^8]

- In **Tensor Paralleism** each GPU processes only a slice of a tensor
  and only aggregates the full tensor for operations that require the
  whole thing.

  - The main building block of any transformer is a fully connected
    nn.Linear followed by a nonlinear activation GeLU.

    - `Y = GeLU(XA)`, where X and Y are the input and output vectors,
      and A is the weight matrix.

  - If we look at the computation in matrix form, it’s easy to see how
    the matrix multiplication can be split between multiple GPUs:

# Tensor Parallelism

<div style="text-align: center;">

<img src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/parallelism-tp-parallel_gemm.png" width="66%" style="text-align: center;" />

</div>

<div class="footer">

This information is based on (the much more in-depth) [TP
Overview](https://github.com/huggingface/transformers/issues/10321#issuecomment-783543530)
by [(**anton-l?**)](https://github.com/anton-l)

</div>

# 3D Parallelism

- `DP` + `TP` + `PP` (3D) Parallelism

<div id="fig-3d-parallel-1">

![](https://www.microsoft.com/en-us/research/uploads/prod/2020/09/Blog_DeepSpeed3_Figure-1_highres-2048x1230.png)

Figure 6: **?(caption)**

</div>

# 3D Parallelism

- `DP` + `TP` + `PP` (3D) Parallelism

<div id="3dparallel">

![](https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/parallelism-deepspeed-3d.png)

Figure taken from [3D parallelism: Scaling to trillion-parameter
models](https://www.microsoft.com/en-us/research/blog/deepspeed-extreme-scale-model-training-for-everyone/)

</div>

# Loooooooooong Sequence Lengths

<img src="https://saforem2.github.io/assets/ds4sci.svg"
style="width:100.0%" />

<div id="tbl-results">

| Sequence Length |     Old Megatron-DeepSpeed (TFLOPS)      |      New Megatron-DeepSpeed (TFLOPS)      |
|:---------------:|:----------------------------------------:|:-----------------------------------------:|
|       2k        | <span style="text-weight:600;">25</span> | <span style="text-weight:600;">68</span>  |
|       4k        | <span style="text-weight:600;">28</span> | <span style="text-weight:600;">80</span>  |
|       8k        |    <span class="red-text">OOM</span>     | <span style="text-weight:600;">86</span>  |
|       16k       |    <span class="red-text">OOM</span>     | <span style="text-weight:600;">92</span>  |
|       32k       |    <span class="red-text">OOM</span>     | <span style="text-weight:600;">100</span> |
|       64k       |    <span class="red-text">OOM</span>     | <span style="text-weight:600;">106</span> |
|      128k       |    <span class="red-text">OOM</span>     | <span style="text-weight:600;">119</span> |
|      256k       |    <span class="red-text">OOM</span>     | <span style="text-weight:600;">94</span>  |

Table 2: Long sequence length support from
[`microsoft/Megatron-DeepSpeed`](https://github.com/microsoft/Megatron-DeepSpeed)

</div>

# Loooooooooong Sequence Lengths

- Working with [ Microsoft
  DeepSpeed](https://github.com/microsoft/DeepSpeed) team to enable
  longer sequence lengths (context windows) for LLMs[^9]

<div id="fig-ds4sci" style="text-align:center;">

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: center;"><div width="100.0%"
data-layout-align="center">
<p><img src="https://saforem2.github.io/assets/ds4sci.svg"
style="width:100.0%" /> <img
src="https://saforem2.github.io/qmd/dsblog_files/figure-html/cell-4-output-1.svg"
style="width:49.0%" alt="25B" /> <img
src="https://saforem2.github.io/qmd/dsblog_files/figure-html/cell-4-output-2.svg"
style="width:49.0%" alt="33B" /></p>
</div></td>
</tr>
</tbody>
</table>

Figure 7: Maximum (achievable) `SEQ_LEN` for both `25B` and `33B` models
<span class="red-text">$[$WIP$]$</span>

</div>

<div class="footer">

[
`argonne-lcf/Megatron-DeepSpeed`](https://github.com/argonne-lcf/Megatron-DeepSpeed)

</div>

# 

<img
src="https://saforem2.github.io/qmd/dsblog_files/figure-html/cell-4-output-1.svg"
style="width:49.0%" alt="25B" /> <img
src="https://saforem2.github.io/qmd/dsblog_files/figure-html/cell-4-output-2.svg"
style="width:49.0%" alt="33B" />

# Loooooooooong Sequence Lengths

- We can evaluate the performance of our model by looking at two
  different metrics for throughput: `samples_per_sec` and `TFLOPS`.
  - Explicitly, we see that we are able to scale up to significantly
    longer sequences:  
    (`420k / 128k ~ 3.3x`) with only a minimal impact on throughput  
    performance: (`81 / 105 ~ 77%`)[^10].

<div style="font-size:0.8em;">

<div id="tbl-seqlen">

|  Name  | Sequence Length (k) |         (`seq_len / min_seq_len`)          |  TFLOPS  |            TFLOPS (% of peak)             |
|:------:|:-------------------:|:------------------------------------------:|:--------:|:-----------------------------------------:|
| GPT25B |         420         | <span class="blue-text">**3.28125**</span> | 81.77225 | <span class="blue-text">**77.867**</span> |
| GPT25B |         400         |                   3.125                    |  90.62   |                  86.297                   |
| GPT25B |         360         |                   2.8125                   | 81.6325  |                  77.7348                  |
| GPT25B |         360         |                   2.8125                   | 82.6824  |                  78.7346                  |
| GPT25B |         192         |                    1.5                     | 115.8228 |                 110.2927                  |
| GPT25B |         128         |                     1                      | 106.672  |                 101.5788                  |
| GPT25B |         128         |                     1                      | 105.014  |                  100.00                   |

Table 3: Impact on TFLOPS as a function of increasing sequence length.
Table from:
[`throughput/TFLOPS`](https://api.wandb.ai/links/l2hmc-qcd/awklywn7)

</div>

</div>

# Getting Started

- Installation:
  1.  Clone GitHub repo:

  ``` bash
  git clone https://github.com/argonne-lcf/Megatron-DeepSpeed
  ```

  2.  Load Conda module:
      - ThetaGPU:

        ``` bash
        if [[ "$(hostname)==theta*" ]]; then
           export MACHINE="ThetaGPU"
           export CONDA_DATE="2023-01-10"
           module load conda/${CONDA_DATE}
           conda activate base
        fi
        ```

      - Polaris:

        ``` bash
        if [[ "$(hostname)==x3*" ]]; then
           export MACHINE="ThetaGPU"
           export CONDA_DATE="2023-10-04"
           module load conda/${CONDA_DATE}
           conda activate base
        fi
        ```

# Getting Started

3.  Setup virtual environment:

    ``` bash
    cd Megatron-DeepSpeed
    # create a new virtual environment
    mkdir -p "venvs/${MACHINE}/${CONDA_DATE}"
    python3 -m  venv "venvs/${MACHINE}/${CONDA_DATE}" --system-site-packages
    source "venvs/${MACHINE}/${CONDA_DATE}/bin/activate"
    ```

4.  Create a new folder where we’ll install dependencies:

    ``` bash
    mkdir -p "deps/${MACHINE}"
    cd "deps/${MACHINE}"
    ```

# Install Dependencies

<div class="panel-tabset"
style="font-size: 0.8em; width: 100%!important; height: 100%!important;">

### saforem2/ezpz

<div id="ezpz">

- [ `saforem2/ezpz`](https://github.com/saforem2/ezpz)

  ``` bash
  pip install -e "git+https://github.com/saforem2/ezpz.git#egg=ezpz"
  ```

</div>

### NVIDIA/apex

- [ `NVIDIA/apex`](https://github.com/NVIDIA/apex)

``` bash
git clone https://github.com/NVIDIA/apex
cd ../apex/
pip install -v --disable-pip-version-check --no-cache-dir --no-build-isolation --global-option="--cpp_ext" --global-option="--cuda_ext" -e ./
```

### pybind/pybind11

- [ `pybind/PyBind11`](https://github.com/pybind/pybind11)

``` bash
pip install pybind11
```

### Dao-AILab/flash-attention

- [
  `Dao-AILab/flash-attention`](https://github.com/Dao-AILab/flash-attention)

- The new release supports three different implementations of
  FlashAttention: (`v1.0.4`, `v2.x`, `triton`)

- FlashAttention `v2.x` may have numerical instability issues. For the
  best performance, we recommend using FlashAttention + Triton

- [
  `Dao-AILab/flash-attention`](https://github.com/Dao-AILab/flash-attention):

  - `v1.0.4`:

    ``` bash
    python3 -m pip install flash-attn==1.0.4
    ```

  - `v2.x`:

    ``` bash
    git clone https://github.com/Dao-AILab/flash-attention
    cd flash-attention
    python3 setup.py install
    ```

  - `openai/triton`:

    ``` bash
    git clone -b legacy-backend https://github.com/openai/triton
    cd triton/python
    python3 -m pip install cmake
    python3 -m pip install .
    ```

</div>

# Running

- The
  [`ALCF/`](https://github.com/argonne-lcf/Megatron-DeepSpeed/tree/main/ALCF)
  directory contains shell scripts for setting up the environment and
  specifying options to be used for training.

- Various options can be specified dynamically at runtime by setting
  them in your environment, e.g.:

  ``` bash
  # Set env. vars to use:
  MODEL_SIZE_KEY="GPT25B" SEQ_LEN=128000 USE_FLASH_ATTN=1
  MICRO_BATCH=1 GAS=1 SP_TYPE="megatron" ZERO_STAGE=1
  # Launch training:
  ./ALCF/train-gpt3.sh
  ```

# Details

Explicitly:

- [`ALCF/train-gpt3.sh`](https://github.com/argonne-lcf/Megatron-DeepSpeed/ALCF/train-gpt3.sh):
  **Main entry point for training**. This script will:
  - Source the rest of the required
    [`ALCF/*.sh`](https://github.com/argonne-lcf/Megatron-DeepSpeed/ALCF/)
    scripts below <!-- - Launch `mpiexec <mpiexec-args> python3` -->
    <!--   [`pretrain_gpt.py`](https://github.com/argonne-lcf/Megatron-DeepSpeed/ALCF/pretrain_gpt.py`) -->
    <!--   `<gpt-args>` -->
- [`ALCF/models.sh`](https://github.com/argonne-lcf/Megatron-DeepSpeed/ALCF/models.sh):
  Contains some example model architectures for GPT3-style models
- [`ALCF/args.sh`](https://github.com/argonne-lcf/Megatron-DeepSpeed/ALCF/args.sh):
  Logic for parsing / setting up runtime options for Megatron and
  DeepSpeed
- [`ALCF/setup.sh`](https://github.com/argonne-lcf/Megatron-DeepSpeed/ALCF/args.sh):
  Locate and activate virtual environment to be used, ensure MPI
  variables are set properly
- [`ALCF/launch.sh`](https://github.com/argonne-lcf/Megatron-DeepSpeed/ALCF/launch.sh):
  Identify available resources and build the command to be executed
  - i.e. figure out how many: `{nodes, GPUs per node, GPUs total}`, to
    pass to `mpi{run,exec}`
  - then, use this to launch `mpiexec <mpiexec-args> python3`
    [`pretrain_gpt.py`](https://github.com/argonne-lcf/Megatron-DeepSpeed/ALCF/pretrain_gpt.py%60)
    `<gpt-args>`

# References

1.  [
    Hannibal046/Awesome-LLM](https://github.com/Hannibal046/Awesome-LLM/blob/main/README.md)
    <span class="inline-image">[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)</span>
2.  [
    Mooler0410/LLMsPracticalGuide](https://github.com/Mooler0410/LLMsPracticalGuide)
3.  [Large Language Models (in
    2023)](https://docs.google.com/presentation/d/1636wKStYdT_yRPbJNrf8MLKpQghuWGDmyHinHhAKeXY/edit#slide=id.g238b2698243_0_734https://docs.google.com/presentation/d/1636wKStYdT_yRPbJNrf8MLKpQghuWGDmyHinHhAKeXY/edit#slide=id.g238b2698243_0_734)
4.  [The Illustrated
    Transformer](http://jalammar.github.io/illustrated-transformer/)
5.  [Generative AI Exists because of the
    Transformer](https://ig.ft.com/generative-ai/)
6.  [GPT in 60 Lines of
    Numpy](https://jaykmody.com/blog/gpt-from-scratch/)

# Backup Slides

# Background

<div>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 6%" />
<col style="width: 43%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: center;"><div id="first-column" width="50.0%"
data-layout-align="center">
<ul>
<li>Large Language models work <em>autoregressively</em></li>
</ul>
</div></td>
<td style="text-align: center;"><div class="quarto-figure-spacer"
width="6.3%" data-layout-align="center">
<p> </p>
</div></td>
<td style="text-align: center;"><div id="fig-autoregression"
width="43.8%" data-layout-align="center" data-fig.extended="false">
<p><img
src="https://miro.medium.com/v2/resize:fit:640/1*3S_Td7UNBT-u8pRnNiZ53w.gif"
data-fig.extended="false" /></p>
<p>Figure 8: Autoregressive generation of tokens by a language model.
GIF by <a href="https://www.linkedin.com/in/echoxlu/">Echo Lu</a>,
containing a modification of an image by <a
href="https://developer.nvidia.com/blog/author/anniesurla/">Annie
Surla</a>, adapted from <span class="citation"
data-cites="Montgomery_2023">Montgomery (2023)</span></p>
</div></td>
</tr>
</tbody>
</table>

</div>

## Training

- Let’s assume our output vocab has only six words:
  <img src="http://jalammar.github.io/images/t/vocabulary.png" width="80%">

- How do you compare two probability distributions?

  - `[cross_entropy, KL-Divergence, ...]`

- One-hot encoding of the word “am”:
  <img src="http://jalammar.github.io/images/t/one-hot-vocabulary-example.png" width="80%" />

## Training: Loss Function

- Output:  
  <img src="http://jalammar.github.io/images/t/transformer_logits_output_and_label.png" width="80%" />

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Montgomery_2023" class="csl-entry">

Montgomery, Samuel. 2023. “Mastering Language Models.” *Medium*. Towards
Data Science.
<https://towardsdatascience.com/mastering-language-models-32e1d891511a>.

</div>

<div id="ref-vaswani2017attention" class="csl-entry">

Vaswani, Ashish, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion
Jones, Aidan N. Gomez, Lukasz Kaiser, and Illia Polosukhin. 2017.
“Attention Is All You Need.” <https://arxiv.org/abs/1706.03762>.

</div>

<div id="ref-yang2023harnessing" class="csl-entry">

Yang, Jingfeng, Hongye Jin, Ruixiang Tang, Xiaotian Han, Qizhang Feng,
Haoming Jiang, Bing Yin, and Xia Hu. 2023. “Harnessing the Power of LLMs
in Practice: A Survey on ChatGPT and Beyond.”
<https://arxiv.org/abs/2304.13712>.

</div>

<div id="ref-yao2023tree" class="csl-entry">

Yao, Shunyu, Dian Yu, Jeffrey Zhao, Izhak Shafran, Thomas L. Griffiths,
Yuan Cao, and Karthik Narasimhan. 2023. “Tree of Thoughts: Deliberate
Problem Solving with Large Language Models.”
<https://arxiv.org/abs/2305.10601>.

</div>

</div>

[^1]: [
    `Hannibal046/Awesome-LLM`](https://github.com/Hannibal046/Awesome-LLM)

[^2]: [GPT in 60 Lines of
    Numpy](https://jaykmody.com/blog/gpt-from-scratch/)

[^3]: The task of predicting the next logical word in a sequence is
    called **language modeling**.

[^4]: Taking the token with the highest probability as our prediction is
    known as [*greedy
    decoding*](https://docs.cohere.ai/docs/controlling-generation-with-top-k-top-p#1-pick-the-top-token-greedy-decoding)
    or *greedy sampling*.

[^5]: [🤗 Model
    Parallelism](https://huggingface.co/docs/transformers/v4.15.0/parallelism)

[^6]: [🤗 Model
    Parallelism](https://huggingface.co/docs/transformers/v4.15.0/parallelism)

[^7]: [Blog
    Post](https://www.microsoft.com/en-us/research/blog/zero-deepspeed-new-system-optimizations-enable-training-models-with-over-100-billion-parameters/)

[^8]: [Efficient Large-Scale Language Model Training on GPU
    Clusters](https://arxiv.org/abs/2104.04473)

[^9]: The described experiments were performed on 4 NVIDIA DGX A100-40GB
    nodes, all using TPSIZE=32\[^tpsize\], connected through 8 HDR
    InfiniBand (200Gb/s per HDR).↩︎

[^10]: [`throughput/TFLOPS`](https://api.wandb.ai/links/l2hmc-qcd/awklywn7)