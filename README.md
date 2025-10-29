# Get-started-with-Agent-Development-Kit-ADK-

cloudshell workspace ~

export PATH=$PATH:"/home/${USER}/.local/bin"
python3 -m pip install google-adk

gcloud storage cp gs://qwiklabs-gcp-01-737587c14155-bucket/adk_project.zip ./adk_project.zip
unzip adk_project.zip

python3 -m pip install -r adk_project/requirements.txt

from . import agent

    tools=[google_search]

    GOOGLE_GENAI_USE_VERTEXAI=TRUE
GOOGLE_CLOUD_PROJECT=YOUR_GCP_PROJECT_ID
GOOGLE_CLOUD_LOCATION=GCP_LOCATION
MODEL=gemini-2.5-flash

cd ~/adk_project

adk web

export GOOGLE_GENAI_USE_VERTEXAI=TRUE
export GOOGLE_CLOUD_PROJECT=YOUR_GCP_PROJECT_ID
export GOOGLE_CLOUD_LOCATION=GCP_LOCATION
export MODEL=gemini-2.5-flash

python3 app_agent/agent.py

from pydantic import BaseModel, Field

class CountryCapital(BaseModel):
    capital: str = Field(description="A country's capital.")

            disallow_transfer_to_parent=True,
        disallow_transfer_to_peers=True,
        output_schema=CountryCapital,

        python3 app_agent/agent.py

        adk run my_google_search_agent

        cd ~/adk_project
cat << EOF > llm_auditor/.env
GOOGLE_GENAI_USE_VERTEXAI=TRUE
GOOGLE_CLOUD_PROJECT=YOUR_GCP_PROJECT_ID
GOOGLE_CLOUD_LOCATION=GCP_LOCATION
MODEL=gemini-2.5-flash
EOF

adk web

