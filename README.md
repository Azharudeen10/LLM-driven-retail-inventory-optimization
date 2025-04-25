# AtliQ Tees: Talk to a Database

This is an end-to-end LLM project based on Google PaLM and Langchain. We are building a system that can talk to a MySQL database. A store manager can ask questions in natural language, and the system will generate accurate SQL queries, execute them, and return the results.

## Use Case

AtliQ Tees is a T-shirt store that maintains inventory, sales, and discount data in a MySQL database. Managers can ask questions like:

- *How many white color Adidas T-shirts do we have left in the stock?*
- *How much sales will our store generate if we can sell all extra-small size T-shirts after applying discounts?*

The system intelligently converts such questions to SQL queries and returns the answer.

## Project Highlights

- AtliQ Tees sells T-shirts from Adidas, Nike, Van Heusen, and Levi's.
- Inventory, sales, and discounts data is stored in a MySQL database.
- This LLM-based question-answering system uses:
  - **Google PaLM LLM**
  - **Hugging Face embeddings**
  - **Streamlit** for UI
  - **Langchain** framework
  - **ChromaDB** as a vector store
  - **Few-shot learning**

Store managers can interact with the system via a user-friendly interface and receive instant responses to their queries.

---

## Installation

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/codebasics/langchain.git
    ```

2. Navigate to the project directory:

    ```bash
    cd 4_sqldb_tshirts
    ```

3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Acquire an API key from [makersuite.google.com](https://makersuite.google.com) and add it to a `.env` file:

    ```env
    GOOGLE_API_KEY="your_api_key_here"
    ```

5. For database setup, run `database/db_creation_atliq_t_shirts.sql` in MySQL Workbench.

---

## Usage

1. Run the Streamlit app:

    ```bash
    streamlit run main.py
    ```

2. The web app will open in your browser. You can now ask questions in natural language and get real-time answers.

---

## Sample Questions

- How many total T-shirts are left in total in stock?
- How many T-shirts do we have left for Nike in XS size and white color?
- How much is the total price of the inventory for all S-size T-shirts?
- How much sales amount will be generated if we sell all small-size Adidas shirts today after discounts?

---

## Project Structure

- `main.py`: Main Streamlit application script.
- `langchain_helper.py`: Contains all Langchain-related logic.
- `requirements.txt`: Required Python packages for the project.
- `few_shots.py`: Contains few-shot learning prompts.
- `.env`: Configuration file for storing your Google API key.
