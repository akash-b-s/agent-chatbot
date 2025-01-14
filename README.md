# **CDP Support Chatbot**

A chatbot designed to assist users with "how-to" questions about four popular Customer Data Platforms (CDPs): Segment, mParticle, Lytics, and Zeotap. The chatbot simplifies complex tasks by providing step-by-step guidance derived directly from official documentation, enabling users to achieve their goals efficiently.

---

## **Core Features**

### **1. Task Guidance**
- Answers user queries such as:
  - *"How do I configure a webhook in Segment?"*  
  - *"How do I create an event stream in mParticle?"*  
- Provides clear, actionable steps to perform tasks.

### **2. Dynamic Documentation Reference**
- Retrieves and indexes relevant sections from official documentation.
- Quickly navigates complex resources to locate precise information.

### **3. Intelligent Query Understanding**
- Interprets different phrasings and variations of questions.
- Handles ambiguous or irrelevant queries gracefully.

### **4. Advanced Functionalities**
- **Cross-Platform Comparisons**: Explains distinctions and similarities between Segment, mParticle, Lytics, and Zeotap functionalities.
- **Expert Guidance**: Handles advanced scenarios like integration setups and workflow configurations.

---

## **Technology Stack**

### **Backend**
- **Python**: Core programming language.
- **Flask**: Framework for developing the chatbot server.

### **Natural Language Processing**
- **spaCy**: Text parsing and query interpretation.
- **LangChain**: For chaining NLP tasks.
- **FAISS/Whoosh**: Efficient indexing and search.

### **Frontend (Optional)**
- **HTML/CSS**: For web-based interaction.
- **JavaScript**: Enhancing interactivity.

### **Additional Tools**
- **BeautifulSoup**: For scraping documentation.
- **Requests**: For HTTP interactions.

---

## **Setup and Deployment**

### **1. Repository Setup**
```bash
git clone https://github.com/yourusername/cdp-support-chatbot.git
cd cdp-support-chatbot
```

### **2. Environment Setup**
- Create a virtual environment:
  ```bash
  python -m venv venv
  source venv/bin/activate  # Windows: venv\Scripts\activate
  ```
- Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```

### **3. Documentation Indexing**
Preprocess and index documentation:
```bash
python preprocess_docs.py
```

### **4. Launch the Chatbot**
Start the server:
```bash
python app.py
```
Access the chatbot at: `http://localhost:5000`.

---

## **How to Use**
1. **Launch the Application**: Run locally or deploy to a cloud platform (e.g., AWS, Heroku).
2. **Interact with the Chatbot**:
   - Use the web interface or API.
   - Example query: *"How do I integrate Lytics with a CRM system?"*

### **API Sample Request**
```json
POST /chat
{
  "query": "How to set up a destination in Segment?"
}
```

---

## **Evaluation Metrics**
- **Accuracy**: Delivers precise steps for tasks.  
- **Robustness**: Handles invalid or vague queries effectively.  
- **Comparative Support**: Enables cross-platform functionality insights.  
- **Extensibility**: Easily adds support for new platforms.

---

## **Planned Improvements**
- **Automatic Updates**: Periodic syncing with updated CDP documentation.  
- **User Personalization**: Store user preferences for a customized experience.  
- **Multi-language Queries**: Support for non-English queries.

---

## **License**
This project is licensed under the [MIT License](LICENSE).
