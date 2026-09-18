# Talk to Code Using RAG

Ask a codebase questions in plain English — get answers grounded in the
actual source, not hallucinated guesses.

This tool parses and embeds a repository's source files, retrieves the
most relevant code chunks for a given query, and feeds that context to
an LLM to generate accurate, source-grounded answers. Built to preserve
code structure across chunk boundaries, so responses reference real
functions and files instead of losing context at the seams.

## How it works
1. **Ingest** — parse source files from a target repo
2. **Embed & index** — chunk and embed code into a vector store
3. **Retrieve** — pull the most relevant chunks for a given question
4. **Generate** — LLM answers using retrieved code as grounded context
## Steps to Run

**Navigate to the Project Directory:**
Change to the directory where the `setup.sh`, `main.py`, `requirements.txt`, and `README.md` files are located.

### 1. Run the Setup File
Make the setup.sh Script Executable (if necessary):
On Linux or macOS, you might need to make the setup.sh script executable:
```shell
chmod +x setup.sh
```
Execute the setup.sh script to set up the environment and install dependencies:
```shell
./setup.sh
```
Now, fill in the `.env` file with your secrets.

### 2. Run the Python Script
```shell
source ~/.venvs/chat_with_code/bin/activate

streamlit run main.py
```
