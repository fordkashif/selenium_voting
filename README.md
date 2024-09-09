
# Voting Automation with Selenium

This project automates voting on the "Sterling Gospel Awards" website using **Selenium**. The script clicks through the voting process by selecting checkboxes and submitting the vote, and can be configured to run on a loop for a specified number of times. Additionally, it can be scheduled to run periodically using a task scheduler (e.g., Task Scheduler on Windows or cron on Linux/macOS).

## Table of Contents

- [Project Overview](#project-overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Automating the Script](#automating-the-script)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The script automates the voting process by:
1. Navigating to the voting page.
2. Clicking on the button to start voting.
3. Selecting the checkboxes for the nominees.
4. Submitting the vote.
5. Clearing cookies after each iteration to start a fresh session.

You can configure how many times the script runs and clear cookies between each run.

## Requirements

To run this project, you will need:
- **Python 3.x**
- **Selenium** Python library
- **ChromeDriver** for automating Google Chrome

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/voting-selenium-project.git
   cd voting-selenium-project
   ```

2. **Set up a virtual environment** (recommended):
   ```bash
   python -m venv selenium_env
   source selenium_env/bin/activate  # On Linux/macOS
   selenium_env\Scripts\activate      # On Windows
   ```

3. **Install the required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download ChromeDriver**:
   - Download the version of **ChromeDriver** that matches your version of Chrome from [here](https://sites.google.com/a/chromium.org/chromedriver/downloads).
   - Place `chromedriver.exe` in the `webdriver` folder.

5. **Edit the script if necessary**:
   - Ensure the path to `chromedriver.exe` is correctly set in `test_automation.py`.
   - For example:
     ```python
     service = Service(executable_path="../webdriver/chromedriver.exe")
     ```

## Usage

To run the script manually, simply execute the following command:

```bash
python tests/test_automation.py
```

The script will:
- Open the **Sterling Gospel Awards** voting page.
- Click on the "welcome" button.
- Select the checkboxes for "Sara-Ann Edwards-Miller" and "Alive - Sara-Ann Edwards-Miller - LOVE 101 F.M.".
- Submit the vote.
- Clear cookies after each iteration.

You can configure the number of times the script runs within the `test_automation.py` file by changing the loop count.

## Automating the Script

### On Windows (Task Scheduler):
1. Open **Task Scheduler** and create a new task.
2. Set the trigger to run the script every 2 hours between 9 AM and 5 PM.
3. Set the action to run the following command:
   ```bash
   C:\path\to\python.exe C:\path\to\your\project\tests\test_automation.py
   ```

### On Linux/macOS (cron job):
1. Open the crontab file:
   ```bash
   crontab -e
   ```
2. Add the following line to run the script every 2 hours between 9 AM and 5 PM:
   ```bash
   0 9-17/2 * * * /path/to/your/venv/bin/python3 /path/to/your/project/tests/test_automation.py
   ```

## Contributing

If you'd like to contribute to this project, feel free to submit a pull request. Before contributing, ensure that your code adheres to the following:
- Follows PEP8 coding standards.
- Includes comments for clarity.
- Has been tested on a local machine.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
