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
│   └── ResumeScannerApp.java 
│
│── bin/                
│── lib/                
│── data/reports/

-------------------------------------------------------------------------------

## Scalability

- Tested on 100K+ simulated resumes & job descriptions
- Optimized scoring logic for performance under large inputs
- Designed for potential DBaaS integration to support recruiter platforms

-------------------------------------------------------------------------------

## License

This project is licensed under the MIT License – see the LICENSE file for details.
