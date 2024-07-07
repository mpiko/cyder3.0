
Output - Generic Input
[[Set up Scenario in Make.com#^8c5339]]
Output - Upworks input
[[Set up Scenario in Make.com#^c3edab]]
Output - Upworks with and RSS feed
[[Set up Scenario in Make.com#^1fc732]]
Blueprint
[[Set up Scenario in Make.com#^5434e7]]

## Prompt
I would like to leverage make.com to provide a feed to ChatGPT to analyse and tell me what pain points people are experiencing, what we can offer them to resolve those issues, and what services we can offer. I am not looking for a response to every post. I am looking for a good summary and, importantly, a good fit for Cyder Solutions. Can you please provide a make.com blueprint?

### Output - Generic Input
^8c5339
Certainly! To create a Make.com blueprint that leverages ChatGPT to analyze customer pain points from various data sources and suggest relevant services, we need to set up a workflow that collects, processes, and summarizes the data. Here's a step-by-step guide to create this blueprint:
### Make.com Blueprint: Automated Customer Pain Point Analysis
#### Overview:
1. **Data Collection**: Gather data from various sources (e.g., forums, social media, feedback forms).
2. **Data Processing**: Clean and structure the collected data.
3. **ChatGPT Integration**: Analyze the data using ChatGPT to identify pain points and suggest solutions.
4. **Summarization**: Summarize the findings into a comprehensive report.
5. **Delivery**: Send the summarized report to relevant stakeholders.

#### Step-by-Step Workflow:
1. **Trigger: Scheduled Data Collection**
   - **Module**: Scheduler
   - **Details**: Set up a scheduler to run the workflow at regular intervals (e.g., daily, weekly).
2. **Action: Collect Data from Sources**
   - **Module**: HTTP Request / API Module
   - **Details**: 
     - Connect to data sources using APIs (e.g., social media platforms, forums, feedback forms).
     - Collect data such as posts, comments, and reviews.
3. **Action: Process and Clean Data**
   - **Module**: Text Parser / Data Transformer
   - **Details**:
     - Parse the collected data to extract relevant information.
     - Clean the data by removing noise (e.g., HTML tags, irrelevant text).
4. **Action: Format Data for Analysis**
   - **Module**: Text Formatter / JSON Module
   - **Details**:
     - Structure the cleaned data into a format suitable for ChatGPT analysis (e.g., JSON format).
5. **Action: Analyze Data with ChatGPT**
   - **Module**: HTTP Request / API Module
   - **Details**:
     - Send the structured data to the ChatGPT API for analysis.
     - Prompt ChatGPT to identify pain points, suggest solutions, and recommend relevant services.

   **Sample Prompt**:
   ```
   Analyze the following customer feedback and identify the main pain points. Suggest solutions and relevant services that Cyder Solutions can offer to address these issues.

   Feedback:
   [Insert structured data here]
   ```

6. **Action: Summarize Findings**
   - **Module**: Text Aggregator
   - **Details**:
     - Aggregate the responses from ChatGPT into a comprehensive summary.
     - Highlight key pain points, suggested solutions, and recommended services.
7. **Action: Create and Send Report**
   - **Module**: Email Module / Google Docs Module
   - **Details**:
     - Create a report containing the summarized findings.
     - Send the report to relevant stakeholders via email or save it to a shared Google Docs folder.

### Example Blueprint Diagram:
1. **Scheduler** (Trigger)
   - Runs daily at 9:00 AM
2. **HTTP Request** (Collect Data)
   - API Call to Social Media/Forums/Feedback forms
   - Collect posts, comments, reviews
3. **Text Parser** (Process Data)
   - Extract relevant information
   - Clean data
4. **JSON Module** (Format Data)
   - Structure data for ChatGPT
5. **HTTP Request** (ChatGPT Analysis)
   - Send data to ChatGPT API
   - Receive analysis (pain points, solutions, services)
6. **Text Aggregator** (Summarize Findings)
   - Aggregate responses
   - Create summary
7. **Email/Google Docs Module** (Create & Send Report)
   - Compile report
   - Send via email or save to Google Docs

### Sample JSON Data for ChatGPT Analysis:
```json
{
  "feedback": [
    {
      "source": "Twitter",
      "post": "I'm having trouble integrating my e-commerce site with my CRM. It's a nightmare!",
      "timestamp": "2024-07-08T10:00:00Z"
    },
    {
      "source": "Forum",
      "post": "Our automation system keeps failing, and customer support is unresponsive.",
      "timestamp": "2024-07-07T14:30:00Z"
    },
    {
      "source": "Feedback Form",
      "comment": "The website is too slow, and the checkout process is confusing.",
      "timestamp": "2024-07-06T09:15:00Z"
    }
  ]
}
```

### Sample Summary Report:
```
### Customer Pain Point Analysis Report

**Date**: 2024-07-08

**Summary of Pain Points**:
1. Integration issues between e-commerce sites and CRM systems.
2. Frequent failures in automation systems and lack of responsive customer support.
3. Website performance issues and confusing checkout processes.

**Suggested Solutions**:
1. Provide a comprehensive integration service for e-commerce and CRM systems.
2. Offer robust automation solutions with 24/7 customer support.
3. Optimize website performance and streamline the checkout process.

**Recommended Services**:
1. **E-commerce and CRM Integration Service**: Ensure seamless data flow between platforms.
2. **Advanced Automation with 24/7 Support**: Reliable automation with dedicated support.
3. **Website Optimization and UX Improvement**: Enhance site speed and user experience.

**Next Steps**:
- Discuss with the team to prioritize these service offerings.
- Schedule a meeting to develop marketing strategies for the new services.

---

Prepared by Cyder Solutions
```

By implementing this Make.com blueprint, you can automate the process of collecting and analyzing customer feedback, providing valuable insights and actionable recommendations to enhance your service offerings.

---
## Output - Upworks input
^c3edab
Certainly! Here's a revised version of the Make.com blueprint to collect and analyze job requests from Upwork. This version focuses on automating the collection of job posts, analyzing them using ChatGPT, and summarizing the findings into a comprehensive report. 
### Make.com Blueprint: Automated Analysis of Upwork Job Requests
#### Overview:
1. **Data Collection**: Gather job requests from Upwork.
2. **Data Processing**: Clean and structure the collected data.
3. **ChatGPT Integration**: Analyze the data using ChatGPT to identify pain points and suggest solutions.
4. **Summarization**: Summarize the findings into a comprehensive report.
5. **Delivery**: Send the summarized report to relevant stakeholders.

#### Step-by-Step Workflow:
1. **Trigger: Scheduled Data Collection**
   - **Module**: Scheduler
   - **Details**: Set up a scheduler to run the workflow at regular intervals (e.g., daily, weekly).
2. **Action: Collect Data from Upwork**
   - **Module**: HTTP Request / API Module
   - **Details**:
     - Connect to Upwork's API to retrieve job requests.
     - Collect job post details such as title, description, and date posted.
3. **Action: Process and Clean Data**
   - **Module**: Text Parser / Data Transformer
   - **Details**:
     - Parse the collected data to extract relevant information.
     - Clean the data by removing noise and irrelevant text.
4. **Action: Format Data for Analysis**
   - **Module**: Text Formatter / JSON Module
   - **Details**:
     - Structure the cleaned data into a format suitable for ChatGPT analysis (e.g., JSON format).
5. **Action: Analyze Data with ChatGPT**
   - **Module**: HTTP Request / API Module
   - **Details**:
     - Send the structured data to the ChatGPT API for analysis.
     - Use a consistent and detailed prompt for analysis.

   **Full ChatGPT Prompt**:
   ```plaintext
   Analyze the following job requests from Upwork and identify the main pain points that clients are experiencing. Based on these pain points, suggest solutions and recommend relevant services that Cyder Solutions can offer to address these issues. Provide a summary that highlights key pain points, suggested solutions, and recommended services.

   Job Requests:
   [Insert structured data here]

   Please ensure the output is structured as follows:
   1. Summary of Pain Points
   2. Suggested Solutions
   3. Recommended Services
   ```

6. **Action: Summarize Findings**
   - **Module**: Text Aggregator
   - **Details**:
     - Aggregate the responses from ChatGPT into a comprehensive summary.
     - Highlight key pain points, suggested solutions, and recommended services.

7. **Action: Create and Send Report**
   - **Module**: Email Module / Google Docs Module
   - **Details**:
     - Create a report containing the summarized findings.
     - Send the report to relevant stakeholders via email or save it to a shared Google Docs folder.

### Example Blueprint Diagram:

1. **Scheduler** (Trigger)
   - Runs daily at 9:00 AM

2. **HTTP Request** (Collect Data)
   - API Call to Upwork
   - Collect job titles, descriptions, and dates

3. **Text Parser** (Process Data)
   - Extract relevant information
   - Clean data

4. **JSON Module** (Format Data)
   - Structure data for ChatGPT

5. **HTTP Request** (ChatGPT Analysis)
   - Send data to ChatGPT API
   - Receive analysis (pain points, solutions, services)

6. **Text Aggregator** (Summarize Findings)
   - Aggregate responses
   - Create summary

7. **Email/Google Docs Module** (Create & Send Report)
   - Compile report
   - Send via email or save to Google Docs

### Sample JSON Data for ChatGPT Analysis:
```json
{
  "job_requests": [
    {
      "title": "Need a Go High Level (GHL) assistant",
      "description": "I am working on a business that provides automation services, web design, google review management to clients in Australia. I need someone to help with GHL, ideally good with Zapier or Make.com etc too for automations.",
      "date_posted": "2024-07-07"
    },
    {
      "title": "Help with Make.com scenario",
      "description": "I'm looking for help to complete a Make.com scenario that assigns click & collect purchases from our online store to a Google Sheet database that a particular click and collect locker. The scenario should then get the lock codes for those lockers from another database that correlate to that order's lockers and then send them to the customer.",
      "date_posted": "2024-07-06"
    }
  ]
}
```

### Sample Summary Report:
```
### Customer Pain Point Analysis Report

**Date**: 2024-07-08

**Summary of Pain Points**:
1. Difficulty integrating Go High Level (GHL) with other automation tools like Zapier and Make.com.
2. Challenges in completing and optimizing Make.com scenarios for specific business processes.
3. Managing click & collect locker assignments and automating the distribution of locker codes.

**Suggested Solutions**:
1. Provide a comprehensive integration service for GHL with other automation tools.
2. Offer expert assistance and optimization for Make.com scenarios.
3. Develop custom solutions for managing click & collect processes and automating locker code distribution.

**Recommended Services**:
1. **GHL and Automation Integration Service**: Ensure seamless integration of GHL with Zapier and Make.com.
2. **Make.com Scenario Optimization**: Expert help in creating and optimizing Make.com scenarios for specific business needs.
3. **Click & Collect Management Service**: Custom solutions for managing locker assignments and automating code distribution.

**Next Steps**:
- Discuss with the team to prioritize these service offerings.
- Schedule a meeting to develop marketing strategies for the new services.

---

Prepared by Cyder Solutions
```

By implementing this Make.com blueprint, you can automate the process of collecting and analyzing job requests from Upwork, providing valuable insights and actionable recommendations to enhance your service offerings.

---
## Output - Upworks with and RSS feed
^1fc732
Certainly! Including an RSS feed to initiate the flow will ensure that the latest job postings from Upwork are captured and analyzed automatically. Here’s the revised Make.com blueprint that includes the RSS feed as the trigger.

### Make.com Blueprint: Automated Analysis of Upwork Job Requests with RSS Feed
#### Overview:
1. **Data Collection**: Gather job requests from Upwork using an RSS feed.
2. **Data Processing**: Clean and structure the collected data.
3. **ChatGPT Integration**: Analyze the data using ChatGPT to identify pain points and suggest solutions.
4. **Summarization**: Summarize the findings into a comprehensive report.
5. **Delivery**: Send the summarized report to relevant stakeholders.

#### Step-by-Step Workflow:
1. **Trigger: RSS Feed for Upwork Job Requests**
   - **Module**: RSS Watch Feeds
   - **Details**: Set up an RSS feed to monitor new job postings from Upwork. This will trigger the workflow whenever a new job post is published.
2. **Action: Collect Data from RSS Feed**
   - **Module**: RSS Feed Module
   - **Details**:
     - Retrieve job post details such as title, description, and publication date.
3. **Action: Process and Clean Data**
   - **Module**: Text Parser / Data Transformer
   - **Details**:
     - Parse the collected data to extract relevant information.
     - Clean the data by removing noise and irrelevant text.
4. **Action: Format Data for Analysis**
   - **Module**: Text Formatter / JSON Module
   - **Details**:
     - Structure the cleaned data into a format suitable for ChatGPT analysis (e.g., JSON format).
5. **Action: Analyze Data with ChatGPT**
   - **Module**: HTTP Request / API Module
   - **Details**:
     - Send the structured data to the ChatGPT API for analysis.
     - Use a consistent and detailed prompt for analysis.

   **Full ChatGPT Prompt**:
   ```plaintext
   Analyze the following job requests from Upwork and identify the main pain points that clients are experiencing. Based on these pain points, suggest solutions and recommend relevant services that Cyder Solutions can offer to address these issues. Provide a summary that highlights key pain points, suggested solutions, and recommended services.

   Job Requests:
   [Insert structured data here]

   Please ensure the output is structured as follows:
   1. Summary of Pain Points
   2. Suggested Solutions
   3. Recommended Services
   ```

6. **Action: Summarize Findings**
   - **Module**: Text Aggregator
   - **Details**:
     - Aggregate the responses from ChatGPT into a comprehensive summary.
     - Highlight key pain points, suggested solutions, and recommended services.
7. **Action: Create and Send Report**
   - **Module**: Email Module / Google Docs Module
   - **Details**:
     - Create a report containing the summarized findings.
     - Send the report to relevant stakeholders via email or save it to a shared Google Docs folder.

### Example Blueprint Diagram:

1. **RSS Watch Feeds** (Trigger)
   - Monitors new job postings on Upwork

2. **RSS Feed Module** (Collect Data)
   - Retrieve job titles, descriptions, and publication dates

3. **Text Parser** (Process Data)
   - Extract relevant information
   - Clean data

4. **JSON Module** (Format Data)
   - Structure data for ChatGPT

5. **HTTP Request** (ChatGPT Analysis)
   - Send data to ChatGPT API
   - Receive analysis (pain points, solutions, services)

6. **Text Aggregator** (Summarize Findings)
   - Aggregate responses
   - Create summary

7. **Email/Google Docs Module** (Create & Send Report)
   - Compile report
   - Send via email or save to Google Docs

### Sample JSON Data for ChatGPT Analysis:
```json
{
  "job_requests": [
    {
      "title": "Need a Go High Level (GHL) assistant",
      "description": "I am working on a business that provides automation services, web design, google review management to clients in Australia. I need someone to help with GHL, ideally good with Zapier or Make.com etc too for automations.",
      "date_posted": "2024-07-07"
    },
    {
      "title": "Help with Make.com scenario",
      "description": "I'm looking for help to complete a Make.com scenario that assigns click & collect purchases from our online store to a Google Sheet database that a particular click and collect locker. The scenario should then get the lock codes for those lockers from another database that correlate to that order's lockers and then send them to the customer.",
      "date_posted": "2024-07-06"
    }
  ]
}
```

### Sample Summary Report:
```
### Customer Pain Point Analysis Report

**Date**: 2024-07-08

**Summary of Pain Points**:
1. Difficulty integrating Go High Level (GHL) with other automation tools like Zapier and Make.com.
2. Challenges in completing and optimizing Make.com scenarios for specific business processes.
3. Managing click & collect locker assignments and automating the distribution of locker codes.

**Suggested Solutions**:
1. Provide a comprehensive integration service for GHL with other automation tools.
2. Offer expert assistance and optimization for Make.com scenarios.
3. Develop custom solutions for managing click & collect processes and automating locker code distribution.

**Recommended Services**:
1. **GHL and Automation Integration Service**: Ensure seamless integration of GHL with Zapier and Make.com.
2. **Make.com Scenario Optimization**: Expert help in creating and optimizing Make.com scenarios for specific business needs.
3. **Click & Collect Management Service**: Custom solutions for managing locker assignments and automating code distribution.

**Next Steps**:
- Discuss with the team to prioritize these service offerings.
- Schedule a meeting to develop marketing strategies for the new services.

---

Prepared by Cyder Solutions
```

By implementing this Make.com blueprint, you can automate the process of collecting and analyzing job requests from Upwork, providing valuable insights and actionable recommendations to enhance your service offerings.

---
## Blueprint

^5434e7

Creating a Make.com blueprint involves defining the entire scenario step by step in a format that can be imported into Make.com. Below is the JSON structure of the Make.com blueprint. You'll need to copy this JSON structure and import it into your Make.com account.

### Make.com Blueprint JSON

```json
{
  "name": "Upwork Job Request Analysis",
  "description": "Automatically collect and analyze Upwork job requests to identify pain points and suggest solutions for Cyder Solutions.",
  "version": 1,
  "team_id": "your_team_id",
  "items": [
    {
      "name": "Watch RSS Feed",
      "module": "rss",
      "action": "watchFeed",
      "parameters": {
        "url": "https://www.upwork.com/ab/feed/jobs/rss?contractor_tier=1%2C2%2C3&verified_payment_only=1&sort=recency&paging=0%3B10&api_params=1&q=automation&securityToken=your_security_token&userUid=your_user_uid&orgUid=your_org_uid",
        "polling_interval": 900
      },
      "output": {
        "bundle": {
          "content": {
            "title": "{{title}}",
            "description": "{{description}}",
            "pubDate": "{{pubDate}}"
          }
        }
      }
    },
    {
      "name": "Text Parser",
      "module": "tools",
      "action": "parseText",
      "parameters": {
        "data": "Description: {{description}}",
        "parser": "your_parser_id"
      },
      "output": {
        "bundle": {
          "content": {
            "parsed_description": "{{parsed_description}}"
          }
        }
      }
    },
    {
      "name": "Format Data for ChatGPT",
      "module": "tools",
      "action": "jsonBuilder",
      "parameters": {
        "json": {
          "job_requests": [
            {
              "title": "{{title}}",
              "description": "{{parsed_description}}",
              "date_posted": "{{pubDate}}"
            }
          ]
        }
      },
      "output": {
        "bundle": {
          "content": {
            "json": "{{json}}"
          }
        }
      }
    },
    {
      "name": "Analyze Data with ChatGPT",
      "module": "http",
      "action": "post",
      "parameters": {
        "url": "https://api.openai.com/v1/engines/davinci-codex/completions",
        "headers": {
          "Authorization": "Bearer your_openai_api_key",
          "Content-Type": "application/json"
        },
        "payload": {
          "prompt": "Analyze the following job requests from Upwork and identify the main pain points that clients are experiencing. Based on these pain points, suggest solutions and recommend relevant services that Cyder Solutions can offer to address these issues. Provide a summary that highlights key pain points, suggested solutions, and recommended services.\n\nJob Requests:\n{{json}}\n\nPlease ensure the output is structured as follows:\n1. Summary of Pain Points\n2. Suggested Solutions\n3. Recommended Services",
          "max_tokens": 500
        }
      },
      "output": {
        "bundle": {
          "content": {
            "choices[0].text": "{{analysis}}"
          }
        }
      }
    },
    {
      "name": "Create Summary Report",
      "module": "tools",
      "action": "textAggregator",
      "parameters": {
        "texts": [
          "### Customer Pain Point Analysis Report\n\n**Date**: {{now}}\n\n**Summary of Pain Points**:\n{{analysis}}\n\n---\n\nPrepared by Cyder Solutions"
        ],
        "separator": "\n\n"
      },
      "output": {
        "bundle": {
          "content": {
            "aggregated_text": "{{aggregated_text}}"
          }
        }
      }
    },
    {
      "name": "Send Report via Email",
      "module": "email",
      "action": "sendEmail",
      "parameters": {
        "to": "stakeholders@cyder.solutions",
        "subject": "Customer Pain Point Analysis Report",
        "html": "{{aggregated_text}}"
      }
    }
  ]
}
```

### Steps to Import the Blueprint into Make.com

1. **Login to Make.com**: Sign in to your Make.com account.

2. **Create a New Scenario**:
   - Navigate to the dashboard.
   - Click on "Create a new scenario."

3. **Import the JSON Blueprint**:
   - Click on the three dots in the upper right corner.
   - Select "Import blueprint."
   - Paste the JSON structure provided above into the import window.
   - Click "Import."

4. **Configure Specific Details**:
   - Replace placeholder values such as `your_team_id`, `your_security_token`, `your_user_uid`, `your_org_uid`, `your_openai_api_key` with your actual credentials.
   - Ensure the RSS feed URL is correctly formatted to fetch job posts relevant to your needs.
   - Adjust any module parameters as needed to fit your specific requirements.

5. **Activate the Scenario**:
   - Once everything is set up and configured, activate the scenario to start the automated process.

This blueprint sets up an automated flow to monitor Upwork job posts via RSS, process the job descriptions, analyze them using ChatGPT, and send a summarized report via email to the relevant stakeholders at Cyder Solutions.