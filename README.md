My Portfolio Website
🚀 Project Overview
Welcome to my portfolio website! This site showcases my skills, projects, and services as a web developer, mobile app developer, IT support specialist, and more. It's built with Vue.js and includes a contact form integrated with EmailJS to send confirmation emails when a user submits the form.

🛠️ Technologies Used
Vue.js - Frontend framework for building the user interface.

Node.js & npm - For managing the project and dependencies.

EmailJS - For handling form submissions and sending confirmation emails.

HTML/CSS - For structuring and styling the website.

JavaScript - For interactive elements on the page.

📥 Installation
To run this project locally, follow the instructions below:

Prerequisites:
Make sure you have Node.js and npm installed. If not, download and install them from Node.js official website.

Step 1: Clone the repository
bash
Copy
Edit
git clone https://github.com/your-username/my-portfolio.git
Replace your-username with your GitHub username.

Step 2: Navigate to the project directory
bash
Copy
Edit
cd my-portfolio
Step 3: Install dependencies
Run the following command to install the required dependencies:

bash
Copy
Edit
npm install
Step 4: Set up EmailJS
Go to EmailJS and sign up for an account.

Set up a new email service and obtain your Service ID, Template ID, and User ID.

Replace YOUR_SERVICE_ID, YOUR_TEMPLATE_ID, and YOUR_USER_ID in the ContactForm.vue component with your actual EmailJS credentials.

Step 5: Run the project
Once everything is set up, start the local development server:

bash
Copy
Edit
npm run serve
Your portfolio should now be running at http://localhost:8080/.

💌 Contact Form
The contact form allows visitors to send messages directly to me. Upon submission, users will receive a thank-you email via EmailJS. The form uses the following fields:

Name

Email

Message

⚙️ How to Use the Portfolio
Home: Welcome section introducing who I am and what I do.

About: Information about my skills and background.

Portfolio: A collection of the projects I’ve worked on.

Services: List of services I offer to clients.

Contact: A form to get in touch with me directly.