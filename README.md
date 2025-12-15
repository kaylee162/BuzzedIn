**Project Overview**
---
BuzzedIn is a full-stack Django web application designed to connect job seekers and recruiters through a skills-based, location-aware hiring platform. The goal is to make early-career job searching more transparent, structured, and human, while giving recruiters better tools to discover and manage candidates.  
This project was built as part of a software design course and follows a role-based architecture with distinct experiences for job seekers and recruiters.  

**Features**
---
**Job Seekers**  
Account creation and authentication  
Customizable profiles including:    
- Headline and bio  
- Skills  
- Education and work experience  
- Projects and external links  
- Location with map integration  
- Privacy and visibility settings

Browse and search job postings  
Filter jobs by skills, location, and other criteria  
View job details and apply directly  
Track application status through a Kanban-style workflow  
Connect with recruiters and other users  

**Recruiters**  
Recruiter account creation and authentication  
Company profiles with descriptions and external links  
Post and manage job listings  
Define required skills, salary ranges, and job locations  
Browse candidates using:  
  - Skills-based search
  - Location and map view
  - Saved filters
  - Recommended matches  

View and manage applicants using a Kanban board:
  - Applied
  - In Review
  - Interview
  - Offer
  - Closed  

Connect with candidates directly through Twilio SMS and email messaging  

**Tech Stack**  
---
**Backend**  
Python  
Django  
Django ORM  
SQLite (development)  

**Frontend**  
Django Templates  
HTML, CSS  
Bootstrap  
JavaScript  

**APIs & Integrations**  
Google Maps API for location and radius-based search  
Optional messaging and communication features  
Role-based access control throughout the app  

**Tools & Workflow**
---
Git and GitHub for version control  
Scrum-based development process  
User stories, sprint planning, and backlog tracking  
Branch-based development and pull requests  

**Project Structure (High Level)** 
---
```bash
GTJobSearch/
│
├── accounts/        # Authentication and user accounts
├── profiles/        # Job seeker and recruiter profiles
├── jobs/            # Job postings and job browsing
├── applications/    # Job applications and status tracking
├── candidates/      # Recruiter-side candidate search
├── communication/   # User connections and messaging
├── home/             # Landing pages and static views
├── static/           # CSS, JS, images
├── templates/        # Shared templates
└── manage.py
```
**Getting Started**
---
**Prerequisites**  
Python 3.10+  
pip  
Virtual environment tool (recommended)  
Google Maps API key (for location features)  

**Installation**  
Clone the repository:
```bash
git clone https://github.com/your-username/GTJobSeekers.git
cd GTJobSeekers
```

Create and activate a virtual environment:  
```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows
```
Install dependencies:  
```bash
pip install -r requirements.txt
```
Create a .env file and add required environment variables:  
```bash
SECRET_KEY=your_django_secret_key
GOOGLE_MAPS_API_KEY=your_google_maps_api_key
```
Run migrations:  
```bash
python manage.py makemigrations
python manage.py migrate
```
Start the development server:  
```bash
python manage.py runserver
```
Open the app in your browser:  
```bash
http://127.0.0.1:8000/
```
**Design & Architecture**
---
Role-based system separating job seeker and recruiter functionality  
Clear separation of concerns between apps  
Skills-first matching model instead of keyword-only search  
Kanban-style workflows to visualize application progress  
Scalable structure for adding messaging, recommendations, and analytics  

**Development Process**
---
The project followed an Agile Scrum workflow:  
- Sprint-based development  
- Clearly defined user stories and acceptance criteria  
- Sprint planning and retrospectives  
- Task tracking with a shared backlog  
- Frequent integration and testing  
- Design decisions prioritized usability, clarity, and real-world hiring workflows.  

**Future Improvements**
---
Recommendation engine for jobs and candidates  
Messaging and notifications  
Resume uploads and parsing  
Advanced analytics for recruiters  
Deployment to a production environment  
Improved accessibility and UI polish  
