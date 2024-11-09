# Automating Procurement Supply Chain with AI Agents

### Version 1.0 to be delivered on 25 December 2024

## Overview

In this repository, we explore how to leverage AI agents to automate various aspects of the procurement supply chain, making the entire process more efficient and responsive. The aim is to streamline procurement processes, improve efficiency, reduce costs, and enhance supplier relationships through intelligent automation. We use modern AI technologies such as NLP, LLMs, and RAG (Retrieval-Augmented Generation) to automate tasks like supplier onboarding, RFQ (Request for Quotation) processing, purchase order management, and vendor communication.

## Features Implemented

- **Master Data Management (MDM)**: Uses an all-mini-v6 model for semantic de-duplication to manage and clean master data efficiently.
- **Chatbot for Customer Support**: Uses Llama3 and PostgreSQL RAG for customer support and assistant chatbot capabilities, providing context-aware responses.
- **Conversation Chains**: Implements reusable conversation chains to manage multi-step interactions seamlessly.
- **OCR Capability**: Uses PyTesseract OCR and Llama3.2 for field mapping and invoice validation, allowing accurate extraction of information from documents.
- **Supplier Recommendation and Performance Prediction**: Uses multinomial linear regression to predict suppliers based on historical data, calculating TE, CE, award probability, participation probability, and supplier performance based on past history performances for similar line items.

## Features in Pipeline

- **Supplier Onboarding Automation**: Use NLP-powered AI agents to automate the onboarding process, extracting and validating supplier data from documents and performing compliance checks.
- **Intelligent RFQ Handling**: AI agents automate the generation and management of RFQs, leveraging RAG models to create RFQ documents, engage with suppliers, and gather quotes.
- **Vendor Communication**: Automate communication with vendors through conversational AI chatbots, providing a seamless interface for answering queries, issuing updates, and managing negotiations.
- **Purchase Order Management**: Use AI to manage purchase orders, automate approval workflows, and track order statuses, minimizing manual intervention.
- **Data-Driven Decision Making**: Implement LLM-based AI to analyze procurement data, generate insights, and provide recommendations for optimizing supply chain decisions.

## Technologies Used

- **Natural Language Processing (NLP)**: For extracting data from supplier documents and automating communication. Leveraging popular libraries such as SpaCy, NLTK, and Hugging Face Transformers.
- **Large Language Models (LLMs)**: To handle complex, context-aware conversations with suppliers and generate procurement documents. Examples include Llama3, GPT-4, and fine-tuned transformer models.
- **Retrieval-Augmented Generation (RAG)**: Used for generating context-rich responses and retrieving relevant data for procurement tasks, combining LLMs with document search capabilities to enhance response accuracy.
- **Python, TensorFlow, PyTorch**: For building and deploying AI models. TensorFlow and PyTorch are used for developing deep learning models, while Python is the primary language for backend development.
- **Microsoft Fabric, Azure, AWS**: Cloud platforms for hosting and managing the AI agents. Microsoft Fabric is used for data integration, while Azure and AWS provide scalable infrastructure for deployment.
- **MongoDB, PostgreSQL**: Database solutions for managing procurement data and documents. MongoDB is used for unstructured data, while PostgreSQL manages structured data and supports full-text search.
- **PyTesseract**: Optical Character Recognition (OCR) tool used for extracting text from images and scanned documents, integrated with AI models for field mapping and validation.
- **Docker & Docker Compose**: For containerizing the application to ensure consistency across different environments and simplify deployment.
- **LangChain**: A framework for building conversational agents and managing conversation flows, used to implement reusable conversation chains.
- **APIs for Integration**: RESTful APIs for interacting with various components like supplier databases, cloud services, and document processing modules.
## Getting Started

This section will help you set up the project locally, including prerequisites, installation steps, and usage instructions. Follow the detailed guidelines to ensure a smooth setup and deployment.

### Prerequisites

Before getting started, make sure you have the following installed and configured:
- **Python 3.8+**: This project requires Python to run the backend services.
- **Docker**: For containerizing the application.
- **Cloud Account**: Access to Azure, AWS, or Microsoft Fabric for deployment.
- **Database Setup**: MongoDB and PostgreSQL instances set up for managing procurement and vendor data.

### Installation

Follow these steps to set up the project locally:
1. **Clone the repository**
   ```sh
   git clone https://github.com/yourusername/procurement-ai-agents.git
   cd procurement-ai-agents
   ```

2. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   - Configure your cloud credentials, database URIs, and any required API keys in an `.env` file.

4. **Run the application**
   ```sh
   docker-compose up
   ```
   This command will start all necessary services in Docker containers, including the backend, databases, and any auxiliary services.

### Usage

- Access the web interface at `http://localhost:8000` to interact with the procurement chatbot.
- Use the API endpoints to automate RFQ generation, supplier onboarding, and communication workflows.

## Project Structure

The following directories and files make up the project:
- **/agents**: Contains code for AI agents responsible for tasks such as supplier onboarding, RFQ management, and vendor communication.
- **/models**: Pre-trained models and scripts for fine-tuning NLP, LLMs, and other AI models used in procurement automation.
- **/data**: Contains sample procurement data, RFQs, POs, and other documents used for testing and validation purposes.
- **/scripts**: Utility scripts for data preprocessing, integration, and automation of routine tasks, such as data cleaning and normalization.
- **/ui**: Contains the code for the frontend interface, allowing users to interact with AI agents for different procurement-related activities.

## Contributing

We welcome contributions to improve the automation of the procurement supply chain using AI. Please open issues to discuss features or bug reports, and feel free to submit pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or collaboration opportunities, feel free to reach out at [your-email@example.com].


