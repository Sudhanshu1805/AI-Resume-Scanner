# AI Resume Scanner

A Java-based automation pipeline to parse resumes, match them against job descriptions, and generate structured reports with 90%+ accuracy. Built on MVC architecture for scalability and modularity, this project simulates large-scale corpora (100K+ resumes) and integrates with MySQL for persistent storage and recruiter query support.

-------------------------------------------------------------------------------

## Features

- Resume Parsing: Extracts key information (name, skills, experience, etc.) with high accuracy
- Scoring Engine: Matches resumes to job descriptions with optimized logic for time complexity
- MVC Architecture: Ensures modular, maintainable, and scalable design
- Database Integration: Stores reports in MySQL for real-time recruiter access
- Interactive UI: Upload resumes, generate reports, and download results directly
- Scalable Simulation: Tested on large datasets (100K+ resumes and JDs)

-------------------------------------------------------------------------------

## Project Structure (MVC)

AI-Resume-Scanner/
│── src/
│   ├── Model/         
│   ├── View/           
│   ├── Controller/     
│   └── ResumeScannerApp.java   # Entry point
│
│── bin/                
│── lib/                
│── data/reports/

-------------------------------------------------------------------------------

## Installation & Setup

# 1. Clone the Repository
git clone https://github.com/Sudhanshu1805/AI-Resume-Scanner.git
cd AI-Resume-Scanner

# 2. Compile the Project
javac -cp ".:lib/" -d bin src/Model/*.java src/Controller/*.java src/View/*.java ResumeScannerApp.java

# 3. Run the Application
java -cp ".:bin:lib/*" ResumeScannerApp

# UI Workflow:
# - Enter user name
# - Upload a resume
# - Generate a report
# 
# Report will:
# - Display on the UI
# - Save under data/reports/
# - Be available for download from the UI

-------------------------------------------------------------------------------

## Database Setup (MySQL)

# 1. Install MySQL (if not already installed)
sudo apt update
sudo apt install mysql-server
sudo mysql -u root -p

# 2. Create Database & Table
CREATE DATABASE resumescanner;

USE resumescanner;

CREATE TABLE reports (
    id INT NOT NULL AUTO_INCREMENT,
    username VARCHAR(255) DEFAULT NULL,
    filename VARCHAR(255) DEFAULT NULL,
    generated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    PRIMARY KEY (id)
) AUTO_INCREMENT = 1;

# 3. Verify Reports
SELECT * FROM reports;

-------------------------------------------------------------------------------

## Workflow

# Process Flow:
# 1. User uploads resume
# 2. Resume Parsing
# 3. Scoring Engine
# 4. Generate Report
# 5. UI Display
# 6. Save in data/reports/
# 7. Insert into MySQL reports Table

-------------------------------------------------------------------------------

## Technologies Used

- Java (JDK 8+) – Core language
- Swing / JavaFX – User interface
- MySQL – Database integration
- MVC Pattern – Architecture for maintainability
- External Libraries – (list from lib/ folder if relevant)

-------------------------------------------------------------------------------

## Scalability

- Tested on 100K+ simulated resumes & job descriptions
- Optimized scoring logic for performance under large inputs
- Designed for potential DBaaS integration to support recruiter platforms

-------------------------------------------------------------------------------

## Contributing

# Step 1: Fork the repo
# Step 2: Create a feature branch
git checkout -b feature-name

# Step 3: Commit changes
git commit -m "Add feature"

# Step 4: Push branch
git push origin feature-name

# Step 5: Open a Pull Request

-------------------------------------------------------------------------------

## License

This project is licensed under the MIT License – see the LICENSE file for details.
