# Swarm Agent

This Python script is designed to function as a set of agents that perform various tasks, including fetching LinkedIn profile information, generating SEO reports, composing personalized cold outreach emails, and sending emails. It leverages APIs, such as the LinkedIn Data API and Ahrefs API, and integrates with OpenAI's GPT models for generating reports and emails.

## Features

- **LinkedIn Agent**: Fetches information from LinkedIn profiles using the LinkedIn Data API. It retrieves details like job title, company, and the user's last post.
- **SEO Agent**: Gathers SEO data from Ahrefs, such as traffic history, domain rating, URL rating, backlinks, and referring domains. It generates an SEO report using OpenAI GPT models.
- **Email Writing Agent**: Composes cold outreach emails using data from LinkedIn profiles and SEO reports, then sends emails using SMTP.
- **User Interface Agent**: Acts as the main interface for interactions, combining the functionality of the LinkedIn and SEO agents to provide a streamlined process for generating and sending emails.

## Dependencies

- **Python 3.x**
- **Libraries**:
  - `requests`
  - `openai`
  - `smtplib`
  - **APIs**:
    - LinkedIn Data API (via RapidAPI)
    - Ahrefs API (via RapidAPI)
  
## How to Run

1. Clone or download this repository.
2. Install the required libraries:
   ```bash
   pip install requests openai
   ```
3. Set up your environment variables for API keys:
   - `OPENAI_API_KEY`: OpenAI API Key
   - `Rapid_API`: RapidAPI key for accessing LinkedIn and Ahrefs data
   - `Email_Password`: Password for the email account used to send emails
4. Run the script:
   ```bash
   python swarm_agent.py
   ```

## Functionality

### LinkedIn Agent

The LinkedIn Agent retrieves profile information such as the user's first and last name, job title, company, and their last LinkedIn post.

```python
def profile_info(linkedin_url):
    # Fetch LinkedIn profile information
```

### SEO Agent

The SEO Agent uses Ahrefs data to fetch traffic history, domain rating, and backlink profile. It then generates an SEO report using OpenAI's GPT model.

```python
def get_SEO_data(website_url):
    # Fetch SEO data and generate report
```

### Email Writing Agent

This agent composes and sends cold outreach emails using insights from LinkedIn and SEO reports.

```python
def compose_email_body(seo_report, linkedin_data):
    # Compose personalized email
```

### Running Demo

The script includes a demo loop that allows interaction with the User Interface Agent:

```python
from swarm.repl import run_demo_loop

if __name__ == "__main__":
    run_demo_loop(user_interface_agent, stream=True)
```
