# Decoded Pathway

## Overview
Using generative AI to chat with local documents has become a safer entry point for integrating artificial technology into various settings. This methodology helps maintain privacy and reduce hallucinations by grounding an AI's response in user-created documents. As the subject-matter-expert, you can accurately evaluate the responses, which is the position we want to be in when interacting with a technology we do not understand.

These models are built around splitting text into chunks and converting it to vectors. I created a process to convert raw data analysis results into a human-readable format so that the explanations around the results provide curated insights rather than exposing an LLM to raw data tables.

The goal was to create a way for anyone to ask questions about attributes associated with any [O*Net](https://www.onetcenter.org/dictionary/28.1/excel/occupation_data.html) occupation. I added context of how occupations are related and educational institutions that provide training as needed.

## Quick Start

GPT4ALL is a free tool that you can download, which is optimized to run LLMs on your local machine. I successfully ran everything on my 2020 M1 Mac with 16GB of memory. You can follow the steps below to get started:

1. Download [GPT4ALL](https://gpt4all.io/index.html).
2. Install the following models: [mistral-7b-openorca.Q4_0.gguf](https://mistral.ai/news/mixtral-of-experts/) and SBert model.
3. Create a folder to store your local documents.
4. Move the localDocs/ONET.txt file into your new directory.
5. In GPT4All, go to Settings > LocalDocs tab, find your directory, give the resource a name, and press "Add." 
6. Wait for it to index your files.
7. Once indexing is complete, return to the chat window.
8. Start a new chat and select the "database" icon from the top-right. This should open a popup with your local document.
9. Select the resource. Now, all future responses will consider the local document for context.

If you get lost, you can refer to this [documentation](https://docs.gpt4all.io/gpt4all_chat.html).

### Example Chat

**Prompt:**

I am a dishwasher. What path should I follow to become an operations research analyst?

**Response:** 

To become an Operations Research Analyst from the position of a Dishwasher, you would need to follow this career progression: 1. Gain experience and education in mathematics or related fields such as Computer Science, Statistics, or Engineering. This can be done through community college courses while working as a dishwasher.
2. Pursue an Associate's degree in Mathematics, Operations Research, Industrial Engineering, or a related field from a community college or online institution.
3. Obtain relevant work experience by seeking internships or entry-level positions in data analysis, logistics, or operations research departments within various industries.
4. Pursue further education and obtain a Bachelor's degree in Operations Research, Industrial Engineering, Mathematics, Statistics, or a related field from a university.
5. Gain professional experience by working as an Operations Research Analyst for several years to develop expertise in the field. This may involve working on various projects within different industries, such as manufacturing, logistics, healthcare, or finance.
6. Consider obtaining certifications and professional credentials relevant to your work, such as Certified Analytics Professional (CAP) from INFORMS or other industry-specific certifications.
7. Continuously develop skills in data analysis, modeling, problem-solving, communication, and leadership through professional development courses, workshops, and conferences.
8. Network with professionals within the field to establish connections that may lead to job opportunities or mentorship.
9. Eventually, you can advance your career by pursuing a higher degree (such as Master's or Ph.D.) in Operations Research or a related field if desired. This will open up more advanced positions and research opportunities.

**Prompt:**

What schools should I consider for the Bachelor's degree?

**Response:**

Some top schools to consider for a Bachelor's degree in Operations Research or related fields include: Massachusetts Institute of Technology (MIT), Stanford University, Harvard University, Carnegie Mellon University, California Institute of Technology (Caltech), and Georgia Institute of Technology. These institutions are known for their strong programs in mathematics, engineering, and data analysis, which can be beneficial for pursuing a career as an Operations Research Analyst.

**Prompt:**

Are those schools aligned with the occupation education requirements?

**Response:**

Yes, these schools are known for granting credentials that align well with the educational requirements related to this occupation. These institutions offer programs in mathematics, engineering, and data analysis, which can be beneficial for pursuing a career as an Operations Research Analyst.

## Data Files
- **O*NET Resource Center**
  - [Occupation Data](https://www.onetcenter.org/dl_files/database/db_28_1_text/Occupation%20Data.txt)
  - [Task Statements](https://www.onetcenter.org/dl_files/database/db_28_1_text/Task%20Statements.txt)
  - [Technology Skills](https://www.onetcenter.org/dl_files/database/db_28_1_text/Technology%20Skills.txt)
  - [Tools Used](https://www.onetcenter.org/dl_files/database/db_28_1_text/Tools%20Used.txt)
  - [Abilities](https://www.onetcenter.org/dl_files/database/db_28_1_text/Abilities.txt)
  - [Interests](https://www.onetcenter.org/dl_files/database/db_28_1_text/Interests.txt)
  - [Work Styles](https://www.onetcenter.org/dl_files/database/db_28_1_text/Work%20Styles.txt)
  - [Work Values](https://www.onetcenter.org/dl_files/database/db_28_1_text/Work%20Values.txt)
  - [Knowledge](https://www.onetcenter.org/dl_files/database/db_28_1_text/Knowledge.txt)
  - [Skills](https://www.onetcenter.org/dl_files/database/db_28_1_text/Skills.txt)
  - [Work Activities](https://www.onetcenter.org/dl_files/database/db_28_1_text/Work%20Activities.txt)
  - [Work Context](https://www.onetcenter.org/dl_files/database/db_28_1_text/Work%20Context.txt)
  - [Job Zones](https://www.onetcenter.org/dl_files/database/db_28_1_text/Job%20Zones.txt)
  - [Education, Training, and Experience](https://www.onetcenter.org/dl_files/database/db_28_1_text/Education%2C%20Training%2C%20and%20Experience.txt)
  - [Education, Training, and Experience Categories](https://www.onetcenter.org/dl_files/database/db_28_1_text/Education%2C%20Training%2C%20and%20Experience%20Categories.txt)
- **National Center for Education Statistics**
  - [Completions 2010 (Final) - 2022 (Provisional)](https://nces.ed.gov/ipeds/datacenter/DataFiles.aspx?year=2022&surveyNumber=-1&sid=2359a156-d43c-4fba-a779-70fd437871de&rtid=7)
  - [2020 CIP/SOC Crosswalk](https://nces.ed.gov/ipeds/cipcode/Files/CIP2020_SOC2018_Crosswalk.xlsx)
  - [2022 Institutional Characteristics](https://nces.ed.gov/ipeds/datacenter/datafiles.aspx?sid=2359a156-d43c-4fba-a779-70fd437871de&rtid=7)
  - [CIP 2-Digit Taxonomy](https://nces.ed.gov/ipeds/cipcode/searchresults.aspx?y=56&sw=1,2,3&ct=1,3&ca=1,2,5,3,4)
- **U.S. Census Bureau**
  - [2018 Occupation Code Lists](https://www2.census.gov/programs-surveys/demo/guidance/industry-occupation/2018-occupation-code-list-and-crosswalk.xlsx)
