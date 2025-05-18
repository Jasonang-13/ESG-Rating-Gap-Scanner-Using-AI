# ESG-Rating-Gap-Scanner-Using-AI
A prototype tool to analyze ESG reports and identify disclosure gaps for ESG rating enhancement (e.g., MSCI for prototype testing in May 2025)
_________________________________________________________________________

🌍**About the Project**
This project demonstrates how AI can be used to scan ESG or Sustainability Reports, identify missing or weak disclosures, and provide targeted suggestions based on ESG rating frameworks like MSCI. It is designed for sustainability professionals, analysts preparing for ESG reporting enhancements and students or early professionals building an AI-ESG portfolio

**🎯 Objectives**
✅ Scan corporate ESG reports (PDF) using AI
✅ Detect disclosures related to ESG rating criteria 
✅ Score the quality and completeness of disclosure
✅ Suggest improvements to enhance ESG scores (if any)

**💬 Key Steps of Codes**
🔐 Step 0: Set Your API Key Securely
-Use getpass() to enter your OpenAI API key without exposing it.
-The key is stored in the environment using os.environ.

📄 Step 1: Upload & Extract Text from ESG Report (PDF)
-Use Google Colab’s files.upload() to upload a PDF.
-Extract text using PyPDF2 library.
-Text from all pages is combined into one string for analysis.

📊 Step 2: Upload ESG Criteria (Excel)
-Upload an Excel file (.xlsx or .xls) that contains a list of ESG criteria (in the first column).
-Convert the column into a list using pandas.

🤖 Step 3: Analyze ESG Disclosure Using OpenAI
-Use OpenAI’s SDK to access gpt-3.5-turbo (free model).
-Send both the report text and the ESG criteria to the model.
-The model returns: (1) whether each criterion is Fully / Partially / Not Disclosed & (2) Suggestions for improvement

⚠️ Safety Check Before Running Analysis
-Only run the analysis if both: (1) PDF text was successfully extracted & (2) ESG criteria list was loaded

**📬 Lesson Learnt**
18/05/2025: 
-Learnt how to develop simple, beginner-friendly ESG analysis code using Google Colab — suitable for non-coders and ESG analysts. The prompt only sends the first 3000 characters of the report to avoid input limits.
-Successfully combined manual uploads (PDF for reports + Excel for ESG criteria) with automated AI analysis.
-Explored how to use OpenAI’s gpt-3.5-turbo model, which is available for free, to perform ESG gap assessments and disclosure analysis.

**🔜 Next Steps**
-Explore the use of Hugging Face (https://huggingface.co/spaces) as an alterntaive to Open AI in this model. The prompt only sends the first 2000 characters of the report and the first 10 criteria to avoid input limits.
-Enhance MSCI ESG criteria for a more comprehensive analysis
