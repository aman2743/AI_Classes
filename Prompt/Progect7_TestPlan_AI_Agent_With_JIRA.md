 ## User provided the below prompt  
I want you to design an Intelligent Test Plan Agent. This is going to be a UI with a frontend where the user will enter the details of JIRA. It will add a connection to JIRA. For example, it will add or provide the API key to connect with JIRA in the UI. After adding the JIRA connection, I want you to ask the user to provide details about the JIRA ID. Suppose it is given VWO1, this is the JIRA ID, you will fetch the details of this JIRA.

And after that, what you are going to do is call an LLM. I am going to provide you my groq.com key, where you will use this LLM to add this JIRA into the context of the LLM.

I am going to share with you a test plan template. You need to create a test plan by using that JIRA ID and the template which I am going to share with you, which is present in the folder. So the template I have already shared in the folder of the parent. You will see testplan.pdf.

So you need to design this overall web application. It should run locally, where it will fetch the LLM that you are using from groq.com, or you should also allow the use of llama. So the user can add the ollama integration also in the settings, and that setting will allow the user to use a local LLM as well.
