<div id="user-content-toc">
  <ul align="center" style="list-style: none;">
    <summary>
      <h1>360Brew-V1</h1>
    </summary>
  </ul>
  <ul align="center" style="list-style: none;">
    <summary>
      <a href='https://github.com/LLMPersonalization/360Brew-V1/blob/main/360brew_v1.pdf'>Paper Link</a> :eyes:
    </summary>
  </ul>  
</div>

## 1. What is 360Brew
360Brew is model that closes the gap between general Large Language Models (LLM) and Personalization tasks including ranking and retreival tasks. The name 360Brew reflects the model’s aim to provide a 360-degree (all-encompassing) solution for personalization, while “Brew” conveys the idea of mixing or combining diverse tasks and data sources into a single, unified foundation.

## 2. Example of the Model Input Prompt
The following is a toy example of 360Brew input for solving a job recommendation task. Note that the member and job data used in this example are entirely fictional.
<table style="background-color: lightgray; width: 100%; border-collapse: collapse;">
<tr>
  <td><b>Instruction:</b><br>
  You are provided a member's profile and a set of jobs, their description, and interactions that the member had with the jobs. For each past job, the member has taken one of the following actions: applied, viewed, dismissed, or did not interact.<br>
  Your task is to analyze the job interaction data along with the member's profile to predict whether the member will apply, view, or dismiss a new job referred to as the "Question" job.
  <b>Note:</b> Focus on skills, location, and years of experience more than other criteria.
  </td>
</tr>
<tr>
  <td><b>Member Profile:</b><br>
  Current position: software engineer, current company: Google, Location: Sunnyvale, California.
  </td>
</tr>
<tr>
  <td><b>Past job interaction data:</b><br>
  Member has applied to the following jobs: [Title: Software Engineer, Location: New York, Country: USA, Company: Meta, Description: …]<br>
  Member has viewed the following jobs: [Title: Software Engineer, Location: Texas, Country: USA, Company: AMD, Description: …]
  </td>
</tr>
<tr>
  <td><b>Question:</b><br>
  Will the member apply to the following job: [Title: Software Engineer, Location: Seattle, Country: USA, Company: Apple, Description: …]
  </td>
</tr>
<tr>
  <td><b>Answer:</b><br>
  The member will apply
  </td>
</tr>
</table>

## 3. Scaling Law - Data
As the data size (in tokens) increases, the average performance of the 360Brew model improves compared to the baselines across five releases over a 9-month period.
<p align="center">
  <img width="800" alt="brew_scaling" src="https://github.com/user-attachments/assets/fa69c492-f4bb-46a7-8658-95f8f408a64a" />
</p>

## 4. Scaling Law - Context Length
One of main benefit of 360Brew model is that it does not require manual feature engineering. In this research, we show that 360Brew model’s performance gets better as we increase the history by increasing the max context length.
![360brew_v1_context_len_scaling](https://github.com/user-attachments/assets/2fd99bb7-d6dc-4a60-a60d-557c655e0d95)

## 5. Scaling Law - Model Parameters
Building on recent works that demonstrate how increasing the size of large language models (LLMs) enhances their ability to understand context, we show that the same principle applies to personalization tasks. Specifically, the 360Brew model improves as we increase its size by leveraging larger and more powerful pre-trained architectures.

<img width="1288" alt="performance-size" src="https://github.com/user-attachments/assets/6c3506ef-d874-4a5a-be91-09b110e7b232" />


## 6. Citation
```
@article{360brew_v1,
  author = {Hamed Firooz, Maziar Sanjabi,  Adrian Englhardt, Aman Gupta, Ben Levine, Dre Olgiati, Gungor Polatkan, Iuliia Melnychuk, Karthik Ramgopal, Kirill Talanine, Kutta Srinivasan, Luke Simon, Natesh Sivasubramoniapillai, Necip Fazil Ayan, Qingquan Song, Samira Sriram, Souvik Ghosh, Tao Song, Vignesh Kothapalli, Xiaoling Zhai, Ya Xu, Yu Wang, and Yun Dai},
  title = {360Brew V1},
  journal = {arXiv preprint},  % Update this if there's a specific journal
  year = {2025},
  url = {https://github.com/LLMPersonalization/360Brew-V1/blob/main/360brew_v1.pdf},
  note = {Accessed: 2025-01-24}
}
```
## 7. Contact
If you have any questions, please raise an issue or contact us at mhfirooz@gmail.com, maziar.sanjabi@gmail.com
