## Multi-P<sup>2</sup>A: A Multi-perspective Benchmark on Privacy Assessment for Large Vision-Language Models

## Overview🔍

![Overview of Multi-P<sup>2</sup>A](./docs/overall.png)

**Figure 1. Privacy evaluation framework. The framework consists of two key components: Privacy Awareness and Privacy Leakage. Privacy Awareness assesses the model's ability to identify the sensitivity of input data, including the privacy risks associated with images, requests, and the flow of private information in various scenarios. Privacy Leakage focuses on evaluating privacy risks in the model's outputs, classifying potential leakage into three categories: (1) extraction of private information from images, (2) inference of privacy from images, and (3) leakage of sensitive data originating from training data.**

**Abstract -** Large Vision-Language Models (LVLMs) exhibit impressive potential across various tasks but also face significant privacy risks, limiting their practical applications. Current researches on privacy assessment for LVLMs is limited in scope, with gaps in both assessment dimensions and privacy categories. To bridge this gap, we propose Multi-P<sup>2</sup>A, a comprehensive benchmark for evaluating the privacy preservation capabilities of LVLMs in terms of privacy awareness and leakage. Privacy awareness measures the model's ability to recognize the privacy sensitivity of input data, while privacy leakage assesses the risk of the model unintentionally disclosing privacy information in its output. We design a range of sub-tasks to thoroughly evaluate the model's privacy protection offered by LVLMs. Multi-P<sup>2</sup>A covers 26 categories of personal privacy, 15 categories of trade secrets, and 18 categories of state secrets, totaling 31,962 samples. Based on Multi-P<sup>2</sup>A, we evaluate the privacy preservation capabilities of 21 open-source and 2 closed-source LVLMs. Our results reveal that current LVLMs generally pose a high risk of facilitating privacy breaches, with vulnerabilities varying across personal privacy, trade secret, and state secret.

## VQA Generation

![VQA Generation Process](./docs/figure2.png)

**Figure 2. VQA Generation Process. We build Image Database and Attribute Database by collecting images and designing attributes for each privacy category. For each task, we create a variety of question templates which will be randomly selected to generate samples. Each VQA sample is the combination of an image from Image Database and a question from Question Templates.**

## Comparison with Existing Benchmarks📊

<table border="1" style="width:100%; border-collapse:collapse; text-align:center;">
  <caption>Comparisons between existing privacy benchmarks. '-' indicates that the benchmark is not open-source. '*' The scale of our released benchmark is 617K, however Dysca is able to generate unlimited data to be tested.</caption>
  <thead>
    <tr>
      <th>Benchmark</th>
      <th>Privacy Awareness</th>
      <th>Privacy Leakage</th>
      <th>Personal Privacy</th>
      <th>Trade Secret</th>
      <th>State Secret</th>
      <th>Models</th>
      <th>Data Scale</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>CONFAIDE</td>
      <td>√</td>
      <td>×</td>
      <td>√</td>
      <td>×</td>
      <td>×</td>
      <td>6</td>
      <td>766</td>
    </tr>
    <tr>
      <td>VIP dataset</td>
      <td>×</td>
      <td>√</td>
      <td>√</td>
      <td>×</td>
      <td>×</td>
      <td>7</td>
      <td>-</td>
    </tr>
    <tr>
      <td>MLLMGUARD</td>
      <td>×</td>
      <td>√</td>
      <td>√</td>
      <td>√</td>
      <td>√</td>
      <td>13</td>
      <td>323</td>
    </tr>
    <tr>
      <td>MultiTrust</td>
      <td>√</td>
      <td>√</td>
      <td>√</td>
      <td>×</td> 
      <td>×</td>
      <td>21</td>
      <td>3,415</td>
    </tr>
    <tr>
      <td>Multi-P<sup>2</sup>A(Ours)</td>
      <td>√</td>
      <td>√</td>
      <td>√</td>
      <td>√</td>
      <td>√</td>
      <td>23</td>
      <td>31,962</td>
    </tr>
  </tbody>
</table>

## Key statistics of VLBiasBench📊

<table border="1" style="width:100%; border-collapse:collapse; text-align:center;">
  <caption>In total, Multi-P<sup>2</sup>A comprises 31,962 samples. The sample scales for each task are shown below.</caption>
  <thead>
    <tr>
      <th>Task</th>
      <th>Dimension</th>
      <th>Data Scale</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Privacy Image Recognition</td>
      <td>Privacy Awareness</td>
      <td>3,202</td>
    </tr>
    <tr>
      <td>Privacy Question Detection</td>
      <td>Privacy Awareness</td>
      <td>14,184</td>
    </tr>
    <tr>
      <td>Privacy InfoFlow Assessment</td>
      <td>Privacy Awareness</td>
      <td>392</td>
    </tr>
    <tr>
      <td>Perception Leakage</td>
      <td>Privacy Leakage</td>
      <td>2,232</td>
    </tr>
    <tr>
      <td>Reasoning Leakage</td>
      <td>Privacy Leakage</td>
      <td>2,682</td>
    </tr>
    <tr>
      <td>Memory Leakage</td>
      <td>Privacy Leakage</td>
      <td>3,798</td>
    </tr>
    <tr>
      <td>Insensitive Questions</td>
      <td>Privacy Leakage</td>
      <td>5,472</td>
    </tr> 
  </tbody>
</table>


## Examples of VLBiasBench📸

### Privacy Awareness
![Samples of Privacy Awareness](./docs/awareness.png)

### Privacy Leakage
![Samples of Privacy Leakage](./docs/leakage.png)


## Related projects🔗
- [BLIP-2](https://github.com/salesforce/LAVIS/tree/main/projects/blip2)
- [InstructBLIP](https://github.com/salesforce/LAVIS/blob/main/projects/instructblip)
- [LLaVA-1.5](https://github.com/haotian-liu/LLaVA)
- [miniGPT4](https://github.com/Vision-CAIR/MiniGPT-4)
- [Otter](https://github.com/Vision-CAIR/MiniGPT-4)
- [Qwen-VL](https://github.com/QwenLM/Qwen-VL)
- [Shikra](https://github.com/shikras/shikra)
- [InternLM-XComposer](https://github.com/InternLM/InternLM-XComposer)

## Links🔗

🔗The link to our project is [\[github\]](https://github.com/Xiangkui-Cao/Multi-P2A)

🔗The link to our paper is [\[arxiv\]](https://arxiv.org/abs/2406.14194)

🔗The link to our dataset is [\[Google Drive\]](https://drive.google.com/file/d/1TxPxdEFFP2HBKnJX9q2eiJ3530PPxNkZ/view?usp=sharing)

🔗The link to our dataset is [\[Baidu NetDisk\]](https://pan.baidu.com/s/1bp4wfwF6HIYECmd-WOwDlA?pwd=8mqx)
