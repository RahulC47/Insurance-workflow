AI-Powered Insurance Eligibility Guard 
This is an n8n automation workflow designed to solve one of the most common bottlenecks in healthcare: manual insurance verification.
The ProblemHospital billing staff spend an average of 15–20 minutes per patient manually verifying insurance details. This leads to long wait times, data entry errors, and a high rate of insurance claim denials.
The SolutionI built a "Human-in-the-loop" automation that uses Local AI (Ollama) to extract data and Real-time APIs to verify eligibility.
How it WorksPatient Intake: A patient uploads their insurance card via a custom n8n Form.
Local AI Processing: The workflow sends the image to a local Llama 3.2 Vision model (via Ollama). 
This ensures data privacy as the image is processed on-site.Real-time Verification: The extracted Member ID is sent via HTTP Request to a medical clearinghouse API.
Smart Logic: If Active: The patient is automatically logged into Airtable as Verified
If Inactive/Error: The billing team receives an instant Telegram alert to handle the case manually.
Key ImpactPrivacy First: By using Ollama, patient PII (Personally Identifiable Information) stays within the local network.
Efficiency: Reduces manual verification time from 20 minutes to < 5 seconds.
Error Reduction: Eliminates typos and manual entry mistakes.
Setup Instructions
1.Install n8n and Ollama.
2.Run ollama pull llama3.2-vision.
3.Import the Insurance.json file into n8n.
4.Configure your Airtable and Telegram credentials.
