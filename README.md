\documentclass[12pt]{article}
\usepackage{hyperref}
\usepackage{graphicx}
\usepackage{listings}
\usepackage{xcolor}
\usepackage{enumitem}
\usepackage{geometry}
\usepackage{fancyhdr}

% Configure page geometry
\geometry{
    a4paper,
    left=2.5cm,
    right=2.5cm,
    top=2.5cm,
    bottom=2.5cm
}

% Configure code listings
\definecolor{codegreen}{rgb}{0,0.6,0}
\definecolor{codegray}{rgb}{0.5,0.5,0.5}
\definecolor{codepurple}{rgb}{0.58,0,0.82}
\definecolor{backcolour}{rgb}{0.95,0.95,0.92}

\lstdefinestyle{mystyle}{
    backgroundcolor=\color{backcolour},   
    commentstyle=\color{codegreen},
    keywordstyle=\color{magenta},
    numberstyle=\tiny\color{codegray},
    stringstyle=\color{codepurple},
    basicstyle=\ttfamily\footnotesize,
    breakatwhitespace=false,         
    breaklines=true,                 
    captionpos=b,                    
    keepspaces=true,                 
    numbers=left,                    
    numbersep=5pt,                  
    showspaces=false,                
    showstringspaces=false,
    showtabs=false,                  
    tabsize=2
}

\lstset{style=mystyle}

% Configure headers and footers
\pagestyle{fancy}
\fancyhf{}
\rhead{Cold Mail Generator}
\lhead{Documentation}
\rfoot{Page \thepage}

\begin{document}

\title{\textbf{Cold Mail Generator}}
\author{Your Name}
\date{\today}

\maketitle

\tableofcontents
\newpage

\section{Introduction}
The Cold Mail Generator is an AI-powered email generation tool built with Groq, LangChain, and Streamlit. This tool streamlines the process of analyzing job postings and generating personalized cold emails by leveraging advanced language models and intelligent portfolio matching.

\section{Key Features}
\begin{itemize}
    \item \textbf{Smart Job Analysis:} Automatically extracts and analyzes job listings from company career pages
    \item \textbf{Intelligent Email Crafting:} Generates contextually relevant and personalized cold emails
    \item \textbf{Portfolio Matching:} Automatically includes relevant portfolio examples based on job requirements
    \item \textbf{User-Friendly Interface:} Clean and intuitive Streamlit-based interface
    \item \textbf{Real-Time Processing:} Quick job extraction and email generation
\end{itemize}

\section{Tech Stack}
\subsection{Frontend}
\begin{itemize}
    \item Streamlit
\end{itemize}

\subsection{AI/ML}
\begin{itemize}
    \item Groq (Language Model)
    \item LangChain (AI Orchestration)
\end{itemize}

\subsection{Data Storage}
\begin{itemize}
    \item Vector Database for portfolio matching
\end{itemize}

\subsection{Additional Tools}
\begin{itemize}
    \item Python 3.9+
    \item Environment management with python-dotenv
\end{itemize}

\section{Prerequisites}
\begin{itemize}
    \item Python 3.9 or higher
    \item Groq API key
    \item Internet connection for API access
    \item Basic understanding of command line operations
\end{itemize}

\section{Installation}
\subsection{Clone the Repository}
\begin{lstlisting}[language=bash]
git clone https://github.com/yourusername/cold-mail-generator.git
cd cold-mail-generator
\end{lstlisting}

\subsection{Set Up Virtual Environment}
\begin{lstlisting}[language=bash]
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
\end{lstlisting}

\subsection{Install Dependencies}
\begin{lstlisting}[language=bash]
pip install -r requirements.txt
\end{lstlisting}

\subsection{Configure Environment Variables}
\begin{lstlisting}[language=bash]
# Create .env file
cp .env.example .env

# Add your Groq API key to .env
GROQ_API_KEY=your_api_key_here
\end{lstlisting}

\section{Quick Start}
\subsection{Start the Application}
\begin{lstlisting}[language=bash]
streamlit run app/main.py
\end{lstlisting}

\subsection{Access the Interface}
Open your browser and navigate to \url{http://localhost:8501}

\section{Usage Example}
\subsection{Input}
\begin{lstlisting}
Career Page URL: https://company.com/careers
\end{lstlisting}

\subsection{Output}
\subsubsection{Extracted Job Data}
\begin{lstlisting}[language=json]
{
  "job_title": "Senior Frontend Developer",
  "required_skills": [
    "React",
    "TypeScript",
    "CSS3"
  ],
  "experience_level": "5+ years",
  "job_description": "Looking for an experienced frontend developer..."
}
\end{lstlisting}

\subsubsection{Generated Email}
\begin{lstlisting}
Subject: Experienced Frontend Developer Ready to Drive Innovation at [Company]

Dear [Hiring Manager],

I came across your Senior Frontend Developer position and was immediately drawn to 
the opportunity to contribute to [Company]'s innovative projects. With 6+ years of 
experience in React and TypeScript, I've successfully delivered robust frontend 
solutions for [Previous Company], achieving a 40% improvement in application 
performance.

You can view my relevant work here:
- [Portfolio Link 1]: React-based e-commerce platform
- [Portfolio Link 2]: TypeScript component library

I'd welcome the chance to discuss how my frontend expertise aligns with your team's needs.

Best regards,
[Name]
\end{lstlisting}

\section{Contributing}
\begin{enumerate}
    \item Fork the repository
    \item Create a feature branch (\texttt{git checkout -b feature/AmazingFeature})
    \item Commit changes (\texttt{git commit -m 'Add AmazingFeature'})
    \item Push to branch (\texttt{git push origin feature/AmazingFeature})
    \item Open a Pull Request
\end{enumerate}

\section{License}
Distributed under the MIT License. See \texttt{LICENSE} for more information.

\section{Contact}
Project Link: \url{https://github.com/yourusername/cold-mail-generator}

\section{Support}
If you find this project helpful, please consider giving it a star!

\end{document}
