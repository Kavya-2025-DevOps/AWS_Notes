
How will you expose Lambda URL to public.
o expose an AWS Lambda Function URL to the public, you must configure its authentication type to NONE.
This tells AWS to assign a public HTTPS endpoint to your function and creates a resource-based policy that allows unauthenticated public access.Here is how you can set this up via the AWS console or the AWS CLI.  
Option 1: Using the AWS Management Console
For a New Lambda Function  
1. Open the AWS Lambda console.
2. Choose Create function and select Author from scratch.
3. Fill in your basic information (Name, Runtime, etc.).
4. Expand the Advanced settings section at the bottom.
5. Check Enable function URL.
6. For Auth type, select NONE.
7. Optional: Check Configure cross-origin resource sharing (CORS) if you need to call this URL directly from a web browser application on another domain.
8. Click Create function.
For an Existing Lambda Function
1. Navigate to your function in the AWS Lambda console.
2. Click on the Configuration tab.
3. On the left sidebar, click Function URL, then click Create function URL (or Edit if one already exists).
4. Select NONE as the Auth type.
5. Save your settings.
The console will instantly generate a unique HTTPS endpoint (e.g., https://<url-id>.lambda-url.<region>.on.aws/) that anyone on the internet can call.  
Option 2: Using the AWS CLI

##

