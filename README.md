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
   git clone https://github.com/fordkashif/selenium_voting.git
   cd voting-selenium-project
