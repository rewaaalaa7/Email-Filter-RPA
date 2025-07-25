# Email Spam Deletion Automation with UiPath

## Overview

This UiPath project designed to connect to a Gmail account, access the Spam folder, and automatically delete spam emails. It uses UiPath's Gmail integration with OAuth 2.0 to securely authenticate and perform email cleanup in a few steps.

---

## Features

- Connects to Gmail using OAuth 2.0 authentication.
- Accesses the **Spam** folder directly.
- Deletes up to 100 spam emails per execution.
- Optionally deletes emails permanently.
- Logs each action for monitoring and traceability.

---

## Prerequisites

Before running this project, ensure the following:

- **UiPath Studio** installed on your machine.
- A valid **Gmail account**.
- `UiPath.Gmail.Activities` package installed:
  - Go to *Manage Packages* → *Official* → Search for `UiPath.Gmail.Activities` and install it.

---

## Setup Instructions

1. **Clone the repository**:
    ```bash
    git clone https://github.com/rewaaalaa7/Email-Filter-RPA.git
    cd Email-Filter-RPA
    ```

2. **Open `Main.xaml` in UiPath Studio.**

3. **Configure Gmail activities**:
   - Open the Gmail scope.
   - Use OAuth authentication.
   - Log in to your Gmail account securely.
   - Make sure the scope folder is set to `"SPAM"`.

4. **Adjust settings** *(optional)*:
   - You can change the number of emails to delete from the `Top` property in the **For Each Email** activity.
   - Default is set to delete **100 emails**.

---

## How to Run

1. Open the project in UiPath Studio.
2. Click **Run File** or **Debug File**.
3. The bot will:
   - Authenticate with Gmail.
   - Access the `Spam` folder.
   - Iterate through the emails.
   - Delete each one.
   - Log completion and count of deleted emails.

---

## Workflow Steps

1. **Gmail Application Scope**:
   - Uses OAuth to connect to the Gmail account.
   - Scope is set to the Spam folder (`SPAM`).

2. **For Each Email**:
   - Iterates over the top 100 spam emails.
   - Logs the subject and sender of each spam email.

3. **Delete Email Activity**:
   - Deletes each email during iteration.
   - Configured to **permanently delete** spam emails.
---
## Main Sequence
![main](https://github.com/rewaaalaa7/Email-Spam-Filter/blob/main/Main%20Sequence.jpg)
## Output
![output](https://github.com/rewaaalaa7/Email-Spam-Filter/blob/main/before.png)
![output](https://github.com/rewaaalaa7/Email-Spam-Filter/blob/main/after.png)

