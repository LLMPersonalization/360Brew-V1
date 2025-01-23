# <p align=center> 360Brew-V1 </p>
<p align=center><a href=''>Paper Link</a></p>

## 1. What is 360Brew
360Brew is a research project that aims to close the gap between general Large Language Models (LLM) and Personalization tasks including ranking and retreival tasks. The name 360Brew reflects the model’s aim to provide a 360-degree (all-encompassing) solution for personalization and recommendation tasks, while “Brew” conveys the idea of mixing or combining diverse tasks and data sources into a single, unified foundation.

## 2. Example of Model Input Prompt
<table style="background-color: lightgray; width: 100%; border-collapse: collapse;">
<tr>
  <td><b>Instruction:</b><br>
  You are provided a member's profile and a set of jobs, their description, and interactions that the member had with the jobs. For each past job, the member has taken one of the following actions: applied, viewed, dismissed, or did not interact.<br>
  Your task is to analyze the job interaction data along with the member's profile to predict whether the member will apply, view, or dismiss a new job referred to as the "Question" job.
  <b>Note:</b><br>
  Focus on skills, location, and years of experience more than other criteria. In your calculation, assign a 30% weight to the relevance between the member's profile and the job description, and a 70% weight to the member's historical activity.
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


## 5. Citation
Coming!!! Arxiv Submission is on-hold

## 6. Contact
If you have any questions, please raise an issue or contact us at mhfirooz@gmail.com, maziar.sanjabi@gmail.com
