# Bonaventure Simeon: Student-Project-Tracker Web App

A simple FastAPI web application for registering students and tracking their weekly progress during the Cloud Native Series.

## 🚀 Key Features

- **Register new students**: Generates a unique ID for each student.
- **Track weekly progress**: Monitor individual student progress over time.
- **Centralized database**: All student data is stored in a single MongoDB instance (hosted on MongoDB Atlas or similar).
- **RESTful API**: Simple endpoints for registration, status check, and progress updates.

## 📦 Prerequisites

- Python 3.10+
- Git
- MongoDB Atlas account (to obtain your connection string)

## 💻 Local Development Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/bonaventuresimeon/student-progress-tracker2.git
   cd student-progress-tracker2

	2.	Create Virtual Environment & Install Dependencies

python3 -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
pip install -r requirements.txt


	3.	Configure Database Connection
	•	Navigate to app/main.py and update the Vault IP:

export VAULT_TOKEN=<your_vault_token>


	4.	Run the Application Locally

uvicorn app.main:app --host 0.0.0.0 --port 8011 --reload

Visit http://localhost:8011 to see your app in action.

🐳 Docker Instructions
	1.	Build Docker Image

docker build -t student-tracker .


	2.	Run Docker Container

docker run --env-file .env -p 8011:8000 student-tracker


	3.	Push to Docker Hub
Ensure you’re logged in:

docker login

Tag and push your image:

docker tag student-tracker your-dockerhub-username/student-tracker
docker push your-dockerhub-username/student-tracker



📬 API Endpoints

Method	Endpoint	Description
POST	/register?name=YourName	Register new student
GET	/status/{student_id}	View registration and progress
POST	/update/{student_id}?week=week1	Update progress by week

🌐 Deploying to Cloud (Optional)

You can deploy the app on platforms like:
	•	Render
	•	Railway
	•	Fly.io
	•	Azure App Service
	•	Elastic Beanstalk or more

👩🏽‍💻 Built for the Cloud Native Series by Bonaventure

This project is used for learning cloud-native tools and hands-on projects. Feel free to fork and extend it!

---

## 📄 LICENSE

To protect your rights as the author and allow others to use your code under specific conditions, consider using the **MIT License**. It's a permissive license that allows others to use, copy, modify, and distribute your code, provided they include the same license in their distributions.

### How to Add the MIT License to Your GitHub Repository

1. **Navigate to Your Repository**

   Go to your repository on GitHub.

2. **Create a New File**

   - Click on the "Add file" dropdown menu.
   - Select "Create new file".

3. **Name the File**

   In the file name field, type `LICENSE` (all uppercase).

4. **Choose a License Template**

   Under the file name, click "Choose a license template". GitHub will display a list of available licenses.

5. **Select MIT License**

   From the list, select the **MIT License**.

6. **Commit the Changes**

   - Scroll down to the "Commit new file" section.
   - Enter a commit message, such as "Add MIT License".
   - Click "Commit new file".

For more detailed instructions, refer to GitHub's documentation on [adding a license to a repository](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-license-to-a-repository).

---

If you need assistance with customizing the license or have further questions, feel free to ask! 
This project is used for learning cloud-native tools and Handson-Project.

Feel free to fork and extend it!
