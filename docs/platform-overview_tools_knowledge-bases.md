[Skip to main content](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#content-area)
[Vogent home page![light logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/light.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=4bdeb0d3b2f061ef727c095d1cbccfeb)![dark logo](https://mintcdn.com/elto-1/ooEImm5m-H0BmxUg/logo/dark.svg?fit=max&auto=format&n=ooEImm5m-H0BmxUg&q=85&s=9cb454e44058d36d3032ca5b13a24149)](http://docs.vogent.ai/)
Search...
⌘K
  * Support
  * [Discord](https://discord.gg/An5z6xhYfS)
  * [Dashboard](https://app.vogent.ai)
  * [Dashboard](https://app.vogent.ai)


Search...
Navigation
Tools
Knowledge Bases
[Guides](http://docs.vogent.ai/introduction)[API Reference](http://docs.vogent.ai/api-reference/introduction)[SDK](http://docs.vogent.ai/sdk/web-sdk)[Voicelab](http://docs.vogent.ai/voicelab/introduction)
##### Get Started
  * [Introduction](http://docs.vogent.ai/introduction)
  * Quickstart


##### Platform Overview
  * [Introduction](http://docs.vogent.ai/platform-overview/introduction)
  * Agents
  * Voices
  * Tools
    * [Function Calling](http://docs.vogent.ai/platform-overview/tools/function-calling)
    * [Knowledge Bases](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
  * [Live Dials](http://docs.vogent.ai/platform-overview/live-dials)
  * [Batch Dial Jobs](http://docs.vogent.ai/platform-overview/batch-dial-jobs)
  * [API Settings](http://docs.vogent.ai/platform-overview/api-settings)
  * [Team](http://docs.vogent.ai/platform-overview/team)
  * [Billing](http://docs.vogent.ai/platform-overview/billing)
  * [Prompting Guide](http://docs.vogent.ai/platform-overview/prompting-guide)


##### Phone Numbers
  * [Overview](http://docs.vogent.ai/telephony/overview)
  * Importing via SIP
  * [Using a SIP Domain](http://docs.vogent.ai/telephony/sip-domain/overview)


##### Self Learning
  * [Self Learning Overview](http://docs.vogent.ai/platform-overview/self-learning/overview)
  * [Auto-Create Agents](http://docs.vogent.ai/platform-overview/self-learning/create)
  * [Optimize Agents](http://docs.vogent.ai/platform-overview/self-learning/optimize)


##### For Developers
  * Webhooks
  * [Dials and Dial Sessions](http://docs.vogent.ai/developers/dials-dialsessions)
  * [Dials Statuses](http://docs.vogent.ai/developers/dial-statuses)
  * [Flow Builder Schemas](http://docs.vogent.ai/developers/schemas)


On this page
  * [Overview](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#overview)
  * [Creating a Knowledge Base](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#creating-a-knowledge-base)
  * [Adding Documents](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#adding-documents)
  * [Managing Files](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#managing-files)
  * [How It Works](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#how-it-works)
  * [Supported File Types](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#supported-file-types)
  * [Using Knowledge Bases](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#using-knowledge-bases)
  * [Best Practices](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#best-practices)
  * [Troubleshooting](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#troubleshooting)


Tools
# Knowledge Bases
Enable agents to access and reference custom documentation
## 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#overview)
Overview
Knowledge bases allow your agents to access and reference custom documentation during conversations. By uploading files to a knowledge base, you can give your agents access to company-specific information, documentation, or any other content they need to provide accurate responses.
## 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#creating-a-knowledge-base)
Creating a Knowledge Base
1
[](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
Navigate to Knowledge Bases
Select **Knowledge Bases** from the left sidebar navigation menu.
2
[](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
Create new
Click the “New Knowledge Base” button in the top-right corner of the screen.
3
[](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
Name your knowledge base
Enter a name for your knowledge base in the provided input field.
4
[](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
Save
Click the “Save” button to create your knowledge base.
## 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#adding-documents)
Adding Documents
Once you’ve created a knowledge base, you can start adding documents:
1
[](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
Access your knowledge base
Click on the knowledge base name from the list to open it.
2
[](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
Upload files
  1. Click the “Upload” button in the top-left corner of the Files section
  2. In the Import File dialog that appears, click “Choose File” to select a file from your computer
  3. Click the “Upload” button to start the upload process


3
[](http://docs.vogent.ai/platform-overview/tools/knowledge-bases)
Monitor processing
After upload, your file will show a “Processing” status while it’s being indexed. Wait for this process to complete.
### 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#managing-files)
Managing Files
  * **File Status** : Each file shows its current status (e.g., “Processing”)
  * **Deleting Files** : Use the “Delete” button next to each file to remove it from your knowledge base
  * **Testing** : Use the “Test” button in the top-right corner to verify your knowledge base is working correctly


## 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#how-it-works)
How It Works
When you upload files to a knowledge base:
  1. Documents are automatically processed and chunked into smaller segments
  2. These chunks are embedded and stored in a vector database
  3. During conversations, when your agent queries the knowledge base, we use Retrieval Augmented Generation (RAG) to: 
     * Find the most relevant document chunks for the query
     * Generate an accurate answer based on the retrieved information
     * Return this contextualized response to your agent


### 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#supported-file-types)
Supported File Types
Currently, knowledge bases support PDF (.pdf) files only. Make sure your PDFs contain readable text - scanned documents should be processed with OCR before uploading.
## 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#using-knowledge-bases)
Using Knowledge Bases
To enable your agent to use a knowledge base, you’ll need to create a Knowledge Base function. See our [Function Calling guide](http://docs.vogent.ai/platform-overview/tools/function-calling) for detailed instructions.
### 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#best-practices)
Best Practices
  * Upload focused, relevant content to improve retrieval accuracy
  * Break down large documents into topic-specific files
  * Regularly update your knowledge base to ensure information stays current
  * Test the knowledge base functionality after adding new documents


## 
[​](http://docs.vogent.ai/platform-overview/tools/knowledge-bases#troubleshooting)
Troubleshooting
If you encounter issues with your knowledge base:
  * **File Processing** : If a file stays in “Processing” status for too long, try deleting and re-uploading it
  * **File Format** : Ensure your files are PDFs with readable text content
  * **File Access** : Verify that the text in your PDFs is selectable/copyable before uploading


For additional help or if you encounter persistent issues, contact our support team through the dashboard.
[Function Calling](http://docs.vogent.ai/platform-overview/tools/function-calling)[Live Dials](http://docs.vogent.ai/platform-overview/live-dials)
⌘I
[twitter](https://x.com/vogentai)[linkedin](https://www.linkedin.com/company/vogent)[discord](https://discord.gg/An5z6xhYfS)
[Powered by](https://www.mintlify.com?utm_campaign=poweredBy&utm_medium=referral&utm_source=elto-1)
