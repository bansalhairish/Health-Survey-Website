# Public Health Survey Platform

A single-page web application for creating and taking simple public health surveys. Built with plain HTML, CSS, and JavaScript, with no frameworks, libraries, or backend required.

Part of the **Community Health Awareness Project**.

---

## Features

- **Role-based access**: log in as an Admin with a password, or continue as a regular User.
- **Create surveys** (Admin only): each survey has a title, one question, and two answer options.
- **Take surveys** (everyone): pick a survey from a dropdown, choose an answer, and submit.
- **Dashboard** (Admin only): view total responses and the count for each option, per survey.
- **Home page**: lists all available surveys with their questions.
- **Form validation**: all fields are required when creating a survey.
- **Responsive layout**: centered container that adapts to smaller screens.

---

## Access Levels

| Page            | User | Admin |
|-----------------|:----:|:-----:|
| Home            | Yes  | Yes   |
| Take Survey     | Yes  | Yes   |
| Create Survey   | No   | Yes   |
| Dashboard       | No   | Yes   |

**Default admin password:** `1234`

---

## Getting Started

No installation or build step is needed.

1. Download or clone the project.
2. Open `project.html` in any modern web browser (Chrome, Firefox, Edge, Safari).
3. Choose **Continue as User** or enter the admin password and click **Login**.

---

## How to Use

### As Admin
1. Enter the admin password and click **Login**.
2. Go to **Create Survey**, fill in the title, question, and both options, then click **Save Survey**.
3. Go to **Take Survey** to answer surveys (you can test your own).
4. Open **Dashboard** to see response counts.

### As User
1. Click **Continue as User**.
2. Go to **Take Survey**, select a survey, choose an answer, and click **Submit Answer**.

---

## Project Structure

```
project.html    # HTML, CSS, and JavaScript, all in one file
README.md       # Project documentation
```

### Main JavaScript Functions

| Function            | Purpose                                              |
|---------------------|------------------------------------------------------|
| `login()`           | Checks the admin password and grants admin access    |
| `continueAsUser()`  | Enters the site with user-level access               |
| `logout()`          | Returns to the login screen                          |
| `showPage(page)`    | Switches between pages and enforces admin permissions|
| `createSurvey()`    | Validates input and saves a new survey               |
| `showSurveys()`     | Displays surveys on the Home page                    |
| `loadSurveys()`     | Fills the survey dropdown on the Take Survey page    |
| `showQuestion()`    | Shows the selected survey's question and options     |
| `submitAnswer()`    | Records a user's answer                              |
| `showResults()`     | Calculates and displays results on the Dashboard     |

---

## Technologies Used

- **HTML5**: structure
- **CSS3**: styling and layout
- **JavaScript (ES6)**: logic and DOM manipulation

---

## Known Limitations

- **No data persistence**: surveys and responses are stored in JavaScript variables, so they are lost when the page is refreshed or closed.
- **Client-side authentication only**: the admin password is hardcoded in the source, so this is not secure and is suitable for demonstration only.
- **Fixed survey format**: each survey supports one question with exactly two options.
- **No duplicate-response prevention**: the same user can submit multiple answers.
- **Unsanitized input**: survey text is inserted into the page using `innerHTML`, which could allow HTML injection.

---

## Future Improvements

- Save data using `localStorage` or a backend database
- Secure authentication with a server-side login
- Support multiple questions and more than two options
- Add charts (bar or pie) to the dashboard
- Prevent duplicate submissions
- Sanitize user input
- Export results as CSV

---

## License

This project is intended for educational purposes.
