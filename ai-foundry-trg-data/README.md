# AI Foundry Training Data Repository

This repository contains diverse datasets for training and experimenting with Azure AI Foundry and other machine learning frameworks. The data includes food/restaurant information, hotel reviews, and NASA documentation.

## 📁 Repository Structure

```
ai-foundry-trg-data/
├── README.md                    # This file
├── food_items.json             # Restaurant menu items dataset
├── hotel_reviews_1000.csv      # Hotel reviews dataset
└── nasa-book-2019/             # NASA documentation pages (84 PDF files)
    ├── page-7.pdf
    ├── page-8.pdf
    ├── page-9.pdf
    └── ... (81 more PDF files)
```

## 📊 Dataset Details

### 1. Food Items Dataset (`food_items.json`)
- **Format**: JSON
- **Size**: ~150 food items across multiple categories
- **Categories**: Smoothies, Salads, Sushi, Sandwiches, and more
- **Fields**: 
  - `category`: Food category (e.g., "Smoothies", "Salad", "Sushi")
  - `name`: Item name
  - `description`: Detailed description of ingredients and preparation
  - `price`: Price in USD

**Example Entry**:
```json
{
    "category": "Smoothies",
    "name": "Ashunti`Way Smoothie",
    "description": "Fruit n greens, mango bananas, tropical fruit blend, dragon fruit mix, mango, bananas, pineapples, apples, and spinach. Special green with strawberry bananas juice blend . Our fruity tasty smoothies are blended to perfection.",
    "price": "5.49 USD"
}
```

**Use Cases**:
- Natural Language Processing (NLP) for menu item recommendations
- Text classification and categorization
- Price prediction models
- Ingredient extraction and analysis

### 2. Hotel Reviews Dataset (`hotel_reviews_1000.csv`)
- **Format**: CSV
- **Size**: 1,000 hotel reviews
- **Fields**: 
  - `id`: Unique identifier
  - `dateAdded`, `dateUpdated`: Timestamp information
  - `address`, `city`, `country`, `province`: Location data
  - `categories`, `primaryCategories`: Business classifications
  - `latitude`, `longitude`: Geographic coordinates
  - `name`: Hotel name
  - `reviews.date`, `reviews.rating`: Review metadata
  - `reviews.text`, `reviews.title`: Review content
  - `reviews.userCity`, `reviews.userProvince`, `reviews.username`: Reviewer info
  - `sourceURLs`, `websites`: Reference links

**Use Cases**:
- Sentiment analysis on customer reviews
- Geographic data analysis and visualization
- Review classification and rating prediction
- Customer feedback analysis
- Location-based recommendation systems

### 3. NASA Documentation (`nasa-book-2019/`)
- **Format**: PDF files
- **Size**: 84 individual page files from a NASA publication
- **Content**: Technical documentation, likely from a 2019 NASA publication
- **File Pattern**: `page-{number}.pdf`

**Use Cases**:
- Document processing and OCR
- Technical text extraction
- PDF parsing and content analysis
- Knowledge extraction from scientific documents
- Document classification and indexing

## 🚀 Getting Started

### Prerequisites
- Python 3.7+ (for data processing)
- Azure AI Foundry access (for cloud-based training)
- Required libraries: `pandas`, `json`, `PyPDF2` or similar for PDF processing

### Quick Start
```python
# Load food items
import json
with open('food_items.json', 'r') as f:
    food_data = json.load(f)

# Load hotel reviews
import pandas as pd
hotel_data = pd.read_csv('hotel_reviews_1000.csv')

# Process PDFs (example with PyPDF2)
import PyPDF2
with open('nasa-book-2019/page-11.pdf', 'rb') as f:
    pdf_reader = PyPDF2.PdfReader(f)
    # Process PDF content...
```

## 🔬 Potential ML/AI Applications

### Food Items Dataset
- **Menu Recommendation Systems**: Build recommenders based on ingredients and categories
- **Price Optimization**: Analyze pricing patterns across categories
- **Ingredient Analysis**: Extract and categorize ingredients for dietary recommendations
- **Text Generation**: Train models to generate food descriptions

### Hotel Reviews Dataset
- **Sentiment Analysis**: Classify reviews as positive/negative/neutral
- **Location Intelligence**: Analyze review patterns by geographic location
- **Quality Prediction**: Predict hotel ratings based on review text
- **Competitive Analysis**: Compare hotels across different metrics

### NASA Documentation
- **Document Intelligence**: Extract structured information from technical documents
- **Knowledge Graphs**: Build knowledge representations from scientific text
- **Technical Writing Analysis**: Study patterns in technical documentation
- **OCR and Text Extraction**: Practice document digitization techniques

## 📈 Data Quality and Characteristics

### Food Items
- Clean, structured JSON format
- Consistent field naming
- Rich descriptive text suitable for NLP
- Diverse price ranges and categories

### Hotel Reviews
- Comprehensive review metadata
- Geographic diversity across US locations
- Rating scale: 1-5 stars
- Temporal data spanning multiple years
- Mix of brief and detailed reviews

### NASA PDFs
- Professional technical documentation
- Consistent formatting across pages
- Mix of text, charts, and technical diagrams
- Varying file sizes indicating different content densities

## 🛠️ Tools and Frameworks

This dataset is suitable for use with:
- **Azure AI Foundry**: Cloud-based ML model training and deployment
- **Azure Cognitive Services**: Text analytics, form recognizer, etc.
- **Python ML Libraries**: scikit-learn, TensorFlow, PyTorch
- **Data Processing**: pandas, numpy, spaCy, NLTK
- **Visualization**: matplotlib, seaborn, plotly

## 📝 License and Usage

Please ensure compliance with data usage policies and consider privacy implications when working with review data containing user information.

## 🤝 Contributing

If you have suggestions for additional datasets or improvements to the existing data structure, please feel free to contribute.

## 📞 Support

For questions about Azure AI Foundry integration or data processing techniques, refer to the official Azure documentation or community forums.

---

*Last Updated: July 2025*