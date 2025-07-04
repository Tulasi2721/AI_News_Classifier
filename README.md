# AI-Powered News Classification System


## 🎯 Project Overview

An intelligent news article classification system that automatically categorizes news articles into predefined categories using advanced machine learning and natural language processing techniques.

### 🏆 Objective
Build a system to classify news articles into categories like politics, technology, sports, business, entertainment, health, and science using machine learning algorithms.

### 📚 Learning Objectives
- Learn text classification and machine learning concepts
- Understand natural language processing (NLP) techniques
- Implement web-based deployment with Flask
- Experience cloud deployment and scalability

## ✨ Features

- **🤖 AI-Powered Classification**: Advanced ML algorithms for accurate categorization
- **📊 Multi-Category Support**: 7 news categories (Politics, Technology, Sports, Business, Entertainment, Health, Science)
- **⚡ Real-time Processing**: Sub-second classification with confidence scores
- **📁 Batch Processing**: Upload and process multiple articles simultaneously
- **📈 Analytics Dashboard**: Comprehensive statistics and insights
- **🔌 RESTful API**: Programmatic access for integration
- **☁️ Cloud Ready**: Designed for AWS, IBM Cloud, or Heroku deployment
- **📱 Responsive Design**: Mobile-friendly web interface

## 🛠️ Technology Stack

### Backend
- **Python 3.8+**: Core programming language
- **Flask**: Web framework
- **scikit-learn**: Machine learning library
- **NLTK**: Natural language processing
- **SQLite**: Database for storing results
- **Pandas**: Data manipulation and analysis

### Frontend
- **HTML5 & CSS3**: Structure and styling
- **Bootstrap 5**: Responsive design framework
- **JavaScript (ES6+)**: Interactive functionality
- **Chart.js**: Data visualization
- **Font Awesome**: Icons

### Machine Learning
- **TF-IDF Vectorization**: Text feature extraction
- **Naive Bayes**: Primary classification algorithm
- **Logistic Regression**: Alternative classifier
- **Cross-validation**: Model evaluation

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- pip (Python package installer)
- Git (optional, for cloning)

### Installation

1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd news_classifier
   ```

2. **Run the setup script**
   ```bash
   python setup.py
   ```
   This will:
   - Install all required packages
   - Download NLTK data
   - Create necessary directories
   - Initialize the database
   - Generate sample training data
   - Train the initial model
   - Run basic tests

3. **Start the application**
   ```bash
   python app.py
   ```

4. **Open your browser**
   Navigate to `http://localhost:5000`

## 📖 Usage Guide

### Web Interface

#### Single Article Classification
1. Go to the home page
2. Paste your news article text in the text area
3. Click "Classify Article"
4. View the results with confidence scores

#### Batch Processing
1. Navigate to "Batch Process" page
2. Upload a .txt file with articles separated by empty lines
3. Click "Process Batch"
4. Download results in JSON or CSV format

#### Statistics Dashboard
- View classification statistics
- Analyze category distributions
- Monitor confidence scores
- Export data for further analysis

### API Usage

#### Classify Single Article
```bash
curl -X POST http://localhost:5000/api/classify \
  -H "Content-Type: application/json" \
  -d '{"text": "Your news article text here..."}'
```

#### Response Format
```json
{
  "predicted_category": "technology",
  "confidence": 0.85,
  "top_predictions": [
    ["technology", 0.85],
    ["science", 0.12],
    ["business", 0.03]
  ],
  "timestamp": "2024-01-01T12:00:00Z"
}
```

## 📁 Project Structure

```
news_classifier/
├── app.py                 # Main Flask application
├── config.py             # Configuration settings
├── setup.py              # Setup and installation script
├── requirements.txt      # Python dependencies
├── README.md            # This file
├── src/                 # Source code modules
│   ├── __init__.py
│   ├── text_processor.py      # Text preprocessing
│   ├── model_trainer.py       # ML model training
│   ├── data_handler.py        # Data operations
│   └── dataset_generator.py   # Sample data generation
├── templates/           # HTML templates
│   ├── base.html
│   ├── index.html
│   ├── result.html
│   ├── batch_classify.html
│   ├── batch_results.html
│   ├── statistics.html
│   ├── about.html
│   ├── 404.html
│   └── 500.html
├── data/               # Data storage
├── models/             # Trained models
├── logs/               # Application logs
└── uploads/            # Temporary file uploads
```

## 🔧 Configuration

### Environment Variables
- `FLASK_ENV`: Set to 'production' for production deployment
- `SECRET_KEY`: Flask secret key for security
- `PORT`: Port number for the application
- `DATABASE_URL`: Database connection string

### Model Configuration
Edit `config.py` to modify:
- ML algorithm parameters
- Text processing settings
- Feature extraction options
- Cross-validation settings

## 📊 Supported Categories

1. **Politics** - Government, elections, policy, legislation
2. **Technology** - AI, software, hardware, innovation
3. **Sports** - Games, competitions, athletes, tournaments
4. **Business** - Economy, finance, companies, markets
5. **Entertainment** - Movies, music, celebrities, shows
6. **Health** - Medicine, wellness, research, healthcare
7. **Science** - Research, discoveries, environment, space

## 🚀 Deployment

### Local Development
```bash
export FLASK_ENV=development
python app.py
```

### Production Deployment

#### Heroku
```bash
# Install Heroku CLI and login
heroku create your-app-name
git push heroku main
```

#### AWS EC2
1. Launch EC2 instance
2. Install Python and dependencies
3. Configure security groups
4. Use Gunicorn for production server

#### IBM Cloud
1. Create IBM Cloud account
2. Use Cloud Foundry or Kubernetes
3. Configure manifest.yml
4. Deploy using CLI

## 🧪 Testing

### Run Tests
```bash
python -m pytest tests/
```

### Manual Testing
1. Test single article classification
2. Test batch processing
3. Test API endpoints
4. Verify statistics dashboard
5. Check error handling

## 📈 Performance Metrics

- **Response Time**: < 1 second average
- **Accuracy**: 85%+ on test data
- **Throughput**: 100+ articles/minute
- **Categories**: 7 supported types
- **Languages**: English (extensible)

## 🔮 Future Enhancements

- [ ] Multi-language support
- [ ] Real-time news feed integration
- [ ] Advanced ML models (BERT, transformers)
- [ ] User feedback and model improvement
- [ ] Sentiment analysis integration
- [ ] News source credibility scoring
- [ ] Mobile application
- [ ] Advanced analytics and reporting

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

### Common Issues

**Issue**: NLTK data not found
**Solution**: Run `python -c "import nltk; nltk.download('all')"`

**Issue**: Model training fails
**Solution**: Ensure sufficient memory and check data format

**Issue**: Port already in use
**Solution**: Change port in config.py or kill existing process

### Getting Help

- Check the logs in the `logs/` directory
- Review the configuration in `config.py`
- Run the setup script again: `python setup.py`
- Check system requirements and dependencies

## 📞 Contact

For questions, issues, or contributions:
- Create an issue in the repository
- Check the documentation
- Review the code comments

---



Made with ❤️ for learning AI and Machine Learning
