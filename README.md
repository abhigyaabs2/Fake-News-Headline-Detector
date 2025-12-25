Fake News Headline Detector 
A rule-based Java application that analyzes news headlines to detect potential fake news using pattern matching, regex, and string analytics.
📋 Overview
This project demonstrates how to build an intelligent headline analyzer without using machine learning. It uses rule-based detection to identify suspicious patterns commonly found in fake news and clickbait headlines.
✨ Features

Sensational Word Detection: Identifies emotionally charged words like "shocking", "unbelievable", "miracle"
ALL CAPS Analysis: Flags headlines with excessive capitalization
Punctuation Pattern Matching: Detects overuse of exclamation marks and question marks
Clickbait Phrase Recognition: Identifies common clickbait patterns like "you won't believe" or "doctors hate"
Scoring System: Assigns suspicion scores from 0-100
Real-time Analysis: Interactive command-line interface for instant feedback

🛠️ Technologies Used

Java
Regular Expressions (Regex)
Java Streams API
Pattern Matching
Scanner for user input

🎯 Concepts Demonstrated

String analytics and text processing
Pattern matching with regex
Stream operations and functional programming
Rule-based classification systems
Input validation and error handling

📊 Classification Categories

LEGITIMATE (0-29): Appears to be a genuine news headline
SOMEWHAT SUSPICIOUS (30-49): Contains some questionable elements
SUSPICIOUS (50-69): Multiple red flags detected
HIGHLY SUSPICIOUS (70-100): Strong indicators of fake news/clickbait

🚀 How to Run

Clone or download the repository
Open the project in IntelliJ IDEA or any Java IDE
Run the FakeNewsDetector.java file
Enter headlines when prompted
Type 'exit' to quit the application

💡 Example Usage
Enter a headline: Scientists discover new planet in solar system
Classification: LEGITIMATE
Suspicion Score: 0/100

Enter a headline: SHOCKING: This MIRACLE cure will CHANGE YOUR LIFE!!!
Classification: HIGHLY SUSPICIOUS
Suspicion Score: 95/100
Flags: [Contains 2 sensational word(s), Multiple words in ALL CAPS, Excessive punctuation]
🔧 Customization
You can easily customize the detector by:

Adding more sensational words to the SENSATIONAL_WORDS set
Adjusting scoring weights in the analyzeHeadline() method
Creating new regex patterns for additional detection rules
Modifying classification thresholds

📈 Project Scope
Time to Build: ~45 minutes
Difficulty Level: Beginner to Intermediate
Lines of Code: ~100
🎓 Learning Outcomes

Understanding regex patterns in Java
Working with Java Streams API
Building rule-based classification systems
String manipulation and analysis
Interactive console application development

🤝 Contributing
Feel free to fork this project and add your own detection rules or improvements!
📝 License
This project is open source and available for educational purposes.
