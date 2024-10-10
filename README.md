# NLP_Extract_Country_Info
Extracting county information from publication's title listed on WBG

## Description:
This project is designed to extract metadata from the World Bank Documents & Reports section using their API. It focuses on retrieving documents related to Economic and Sector Work (ESW) from January 1st, 2010, to July 1st, 2024. After fetching the data, it processes the document titles to extract country information and generates visualizations of document counts and percentages over time, grouped by country and year.

## Main Features:
1. **API Data Fetching**:
   - Fetches documents from the World Bank API with filters for Economic and Sector Work (ESW) reports, English language, and a specified date range.
   - Handles pagination by fetching data in batches of 500 records and continues until all records are retrieved.
   
2. **Data Preprocessing**:
   - Cleans and processes the data, including handling missing values and text preprocessing.
   - Uses SpaCy to extract country names from document titles.
   
3. **Data Analysis**:
   - Groups documents by year and country, and calculates both the number and the percentage of documents per country for each year.
   - Creates multiple visualizations using Plotly, including bar charts and pie charts showing the evolution of document distribution over time.

4. **Visualizations**:
   - **Bar Charts**: Display the evolution of the number and percentage of documents by country and year.
   - **Pie Charts**: Represent the document distribution by country for each year.

5. **Validation**:
   - Performs validation checks to ensure the percentage sums for each year add up to 100%.

## Requirements:
- Python 3.x
- Libraries: \`requests\`, \`pandas\`, \`tqdm\`, \`spacy\`, \`plotly\`, \`matplotlib\`

## Setup Instructions:
1. Clone the repository and navigate to the project directory.
2. Install the required libraries:
   \`\`\`bash
   pip install requests pandas tqdm spacy plotly matplotlib
   \`\`\`
3. Download SpaCy's large language model for named entity recognition (NER):
   \`\`\`bash
   python -m spacy download en_core_web_trf
   \`\`\`
4. Run the script to fetch the data from the World Bank API, clean it, and generate visualizations.

## How to Use:
- **Data Fetching**: The script automatically fetches the documents and stores the metadata in a Pandas DataFrame.
- **Visualization**: After processing, animated bar and pie charts visualize the evolution of document distribution by country and year.

## Key Functions:
- **\`clean_text()\`**: Cleans document titles by removing extra spaces and line breaks.
- **Named Entity Recognition (NER)**: Extracts country information from document titles using SpaCy.
- **Visualization**: Creates dynamic visualizations with Plotly.

## Future Enhancements:
- Extend the functionality to handle documents in multiple languages.
- Add functionality for more in-depth document content analysis.

EOL

