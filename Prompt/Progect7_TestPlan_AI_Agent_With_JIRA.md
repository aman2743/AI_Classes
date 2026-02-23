 ## User provided the below prompt  
I want you to design an Intelligent Test Plan Agent. This is going to be a UI with a frontend where the user will enter the details of JIRA. It will add a connection to JIRA. For example, it will add or provide the API key to connect with JIRA in the UI. After adding the JIRA connection, I want you to ask the user to provide details about the JIRA ID. Suppose it is given VWO1, this is the JIRA ID, you will fetch the details of this JIRA.

And after that, what you are going to do is call an LLM. I am going to provide you my groq.com key, where you will use this LLM to add this JIRA into the context of the LLM.

I am going to share with you a test plan template. You need to create a test plan by using that JIRA ID and the template which I am going to share with you, which is present in the folder. So the template I have already shared in the folder of the parent. You will see testplan.pdf.

So you need to design this overall web application. It should run locally, where it will fetch the LLM that you are using from groq.com, or you should also allow the use of llama. So the user can add the **gpt-oss-120b** integration also in the settings, and that setting will allow the user to use a local LLM as well.

## User provided the below prompt in chatGPT or KIMi to Imporove this prompt and got the below output  

## Improved Prompt  

Design and architect an **Intelligent Test Plan Agent** as a local web application.  

### Objective  
The application should automatically generate a structured Test Plan using:  

* A JIRA issue ID
* A predefined Test Plan template (testplan.pdf)
* An LLM (via Groq API or a local LLM)  

## Functional Requirements  

### 1. User Interface (Frontend)  

* Provide a clean UI where the user can:

  * Configure JIRA connection settings  
  * Enter JIRA API credentials (API key, base URL, email if required)  
  * Save and manage integration settings   
  * Enter a JIRA Issue ID (e.g., VWO-1)  

---

### 2. JIRA Integration    

* Allow users to securely connect to JIRA via API.
* After connection:

  * Accept a JIRA Issue ID as input.
  * Fetch complete issue details (summary, description, acceptance criteria, attachments, etc.).
  * Handle errors (invalid API key, invalid issue ID, network issues).

### 3. LLM Integration  

The application must support multiple LLM options:

#### Option A: Groq API  

* User provides their Groq API key.
* Use the configured Groq model to:

  * Inject the fetched JIRA issue details into the LLM context.
  * Generate a structured Test Plan based on the template.

#### Option B: Local LLM  

* Allow configuration for:

  * Ollama
  * gpt-oss-120b (or other supported local models)
* The user should be able to select the LLM provider from the Settings page.
* The system should dynamically route requests based on selected provider.

### 4. Test Plan Generation  

* Use the provided testplan.pdf as the structural template.
* Map JIRA issue details into relevant sections of the template.
* Generate:

  * Scope
  * Test scenarios
  * Test cases
  * Assumptions
  * Risks
  * Dependencies
* Output should be downloadable (PDF or Markdown).

## Technical Requirements  

* Application must run locally.
* Backend should:

  * Fetch JIRA data
  * Manage LLM communication
  * Inject context properly into prompts
* Modular architecture:

  * JIRA Service Layer
  * LLM Service Layer
  * Template Processor
  * UI Layer
* Secure handling of API keys (no hardcoding).

## Expected Output  

Deliver:

1. High-level architecture diagram
2. Suggested tech stack
3. API flow design
4. Data schema
5. Prompt design for LLM
6. Error handling strategy
