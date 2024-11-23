# Cold Mail Generator

A Cold Email Generator for service-based companies, built using **Groq**, **LangChain**, and **Streamlit**. This tool allows users to input the URL of a company's careers page, extract job listings, and generate personalized cold emails tailored to specific job descriptions. The generated emails also include relevant portfolio links, intelligently sourced from a vector database.

## Features

- **Job Listing Extraction**: Extracts job postings directly from the company's careers page in JSON format.
- **Job-Specific Email Generation**: Automatically generates personalized cold emails based on the job description.
- **Portfolio Integration**: Pulls relevant portfolio links from a vector database, ensuring high relevance to the extracted job listing.
- **Easy-to-Use Interface**: Built with Streamlit for an interactive and user-friendly experience.

---

## Architecture

### Workflow

1. **Input**: The user provides the URL of a company's careers page.
2. **Job Extraction**:
   - A Language Model (LLM) processes the careers page and extracts job listings in JSON format with fields like:
     - `job_title`
     - `skills`
     - `experience`
     - `job_description`
3. **Portfolio Matching**: A vector database retrieves relevant portfolio links based on the job description.
4. **Email Generation**:
   - Another LLM generates tailored cold emails using the extracted job information and portfolio links.
5. **Output**: The generated cold emails are displayed to the user.

---

## Technologies Used

- **Groq**: For efficient job extraction and processing.
- **LangChain**: Orchestrates LLM interactions and data pipelines.
- **Streamlit**: Provides an interactive front-end for user input and display of generated cold emails.
- **Vector Database**: Stores and retrieves portfolio links relevant to specific job descriptions.
## Getting Started

Follow these steps to set up and run the application:

### 1. Set Up API Key

- Obtain an API key from Groq.
- Navigate to `app/.env` and update the `GROQ_API_KEY` value with your API key.

### 2. Install Dependencies

Run the following command to install the required dependencies:

```bash
pip install -r requirements.txt

### 3. Run the Streamlit App

Start the Streamlit application with:

```bash
streamlit run app/main.py

Example Output
Input
A sample input is a URL to a company's careers page.

Output
Extracted Job Listings
After processing the URL, the tool extracts job listings in JSON format. For example:

[
  {
    "job_title": "Software Engineer",
    "skills": ["Python", "Machine Learning", "Django"],
    "experience": "2-4 years",
    "job_description": "Build and deploy scalable web applications..."
  }
]
**Generated Cold Email**
Using the extracted job information and relevant portfolio links, the tool generates a personalized cold email like this:

Subject: Excited to Contribute to Your Team as a Software Engineer

Dear [Hiring Manager's Name],

I recently came across the Software Engineer position on your careers page and was captivated by the opportunity to contribute to your team's mission. Having worked extensively with Python, Machine Learning, and Django, I am confident in my ability to build scalable web applications that align with your company’s goals. Attached are some of my portfolio links showcasing relevant projects.

Looking forward to the possibility of discussing this role further.

Best Regards,  
[Your Name]
