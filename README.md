# 🔍 Fake News Headline Detector

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

A rule-based Java application that analyzes news headlines to detect potential fake news using pattern matching, regex, and string analytics—no machine learning required!

## 📖 Table of Contents

- [About](#about)
- [Features](#features)
- [Demo](#demo)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🎯 About

This project demonstrates how to build an intelligent headline analyzer without using machine learning. It uses rule-based detection to identify suspicious patterns commonly found in fake news and clickbait headlines. Perfect for learning text processing, regex, and Java fundamentals!

**Why Rule-Based?**
- Fast and efficient
- No training data required
- Transparent decision-making
- Easy to understand and modify
- Great for educational purposes

## ✨ Features

- 🎯 **Sensational Word Detection** - Identifies emotionally charged words
- 📢 **ALL CAPS Analysis** - Flags excessive capitalization
- ❗ **Punctuation Pattern Matching** - Detects overuse of exclamation/question marks
- 🎣 **Clickbait Phrase Recognition** - Identifies common clickbait patterns
- 📊 **Scoring System** - Assigns suspicion scores from 0-100
- ⚡ **Real-time Analysis** - Interactive command-line interface
- 🏷️ **Classification Categories** - 4-tier classification system

## 🎬 Demo

```
=== FAKE NEWS HEADLINE DETECTOR ===

Enter a headline (or type 'exit' to quit): Scientists discover new planet in solar system

================================================================================
Headline: Scientists discover new planet in solar system
Suspicion Score: 0/100
Classification: LEGITIMATE
Flags: None
================================================================================

Enter a headline (or type 'exit' to quit): SHOCKING: This MIRACLE cure will CHANGE YOUR LIFE!!!

================================================================================
Headline: SHOCKING: This MIRACLE cure will CHANGE YOUR LIFE!!!
Suspicion Score: 95/100
Classification: HIGHLY SUSPICIOUS
Flags: [Contains 2 sensational word(s), Multiple words in ALL CAPS, 
       Excessive punctuation (!!!, ???), Excessive exclamation marks]
================================================================================
```

## 🛠️ Technologies

- **Language**: Java 8+
- **Core APIs**: 
  - `java.util.regex` - Pattern matching
  - `java.util.stream` - Functional operations
  - `java.util.Scanner` - User input

## 📥 Installation

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- Any Java IDE (IntelliJ IDEA, Eclipse, VS Code) or text editor

### Steps

1. Clone the repository
```bash
git clone https://github.com/yourusername/fake-news-detector.git
```

2. Navigate to the project directory
```bash
cd fake-news-detector
```

3. Compile the Java file
```bash
javac FakeNewsDetector.java
```

4. Run the application
```bash
java FakeNewsDetector
```

## 🚀 Usage

1. Run the application
2. Enter a news headline when prompted
3. View the analysis results including:
   - Suspicion score (0-100)
   - Classification level
   - Specific flags detected
4. Continue analyzing more headlines
5. Type `exit` to quit

### Example Headlines to Try

**Legitimate:**
- "Scientists discover new planet in solar system"
- "Government announces new policy changes"
- "Local team wins championship game"

**Suspicious:**
- "SHOCKING: This MIRACLE cure will CHANGE YOUR LIFE!!!"
- "You Won't Believe What This Celebrity Did Next!!"
- "DOCTORS HATE HIM! One simple trick to lose weight!!!"

## 🔧 How It Works

### Detection Rules

1. **Sensational Words** (20 points each)
   - Words like: shocking, unbelievable, miracle, exposed, conspiracy
   
2. **ALL CAPS** (15-25 points)
   - Single ALL CAPS word: 15 points
   - Multiple ALL CAPS words: 25 points

3. **Excessive Punctuation** (20 points)
   - Patterns like `!!!`, `???`, `!?!?`

4. **Clickbait Phrases** (30 points)
   - "you won't believe"
   - "what happens next"
   - "doctors hate"
   - "one simple trick"

5. **Excessive Exclamations** (15 points)
   - 3 or more exclamation marks

### Classification Thresholds

| Score Range | Classification |
|-------------|----------------|
| 0-29 | LEGITIMATE |
| 30-49 | SOMEWHAT SUSPICIOUS |
| 50-69 | SUSPICIOUS |
| 70-100 | HIGHLY SUSPICIOUS |

## 🎨 Customization

### Add More Sensational Words

```java
private static final Set<String> SENSATIONAL_WORDS = new HashSet<>(Arrays.asList(
    "shocking", "unbelievable", "amazing", "incredible", "miracle",
    "yourword1", "yourword2"  // Add your words here
));
```

### Adjust Scoring Weights

Modify the point values in the `analyzeHeadline()` method:

```java
if (sensationalCount > 0) {
    score += (int)(sensationalCount * 20);  // Change this value
}
```

### Add New Detection Rules

Create new regex patterns:

```java
private static final Pattern YOUR_PATTERN = Pattern.compile("your_regex");
```

## 📊 Project Stats

- **Development Time**: ~45 minutes
- **Lines of Code**: ~100
- **Difficulty**: Beginner to Intermediate
- **Concepts Covered**: 7+ core Java concepts

## 🎓 Learning Outcomes

By building/studying this project, you'll learn:

- ✅ Regular expressions in Java
- ✅ Stream API and functional programming
- ✅ Pattern matching techniques
- ✅ String manipulation and analysis
- ✅ Rule-based classification systems
- ✅ Interactive console applications
- ✅ Code organization and best practices

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Create a Pull Request

### Ideas for Contributions

- Add more sensational word patterns
- Implement sentiment analysis
- Add support for multiple languages
- Create a GUI version
- Add file input/output capabilities
- Implement statistics tracking
- Add unit tests

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by the growing need for media literacy
- Built as a learning project to understand text processing
- Thanks to the Java community for excellent documentation

---

<div align="center">

**If you found this project helpful, please give it a ⭐!**

Made with ❤️ and Java

</div>
