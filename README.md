# SAP GUI DevOps Test

This repository contains a 'DevOps Test Performance' schedule template which can be used to execute an existing 'SAP GUI' test on a DevOpsTest server. As of 11.0.2, SAP GUI tests can not execute directly on the server because it requires a Windows agent machine with SAP GUI runtime installed. To enable this use-case, a Performance Tester schedule is required which allows the execution to occur on an external Performance Tester agent machine.

## Prerequisites

- Access to a DevOpsTest server.
- An existing Functional Test based installation.
- A working 'SAP GUI' test project.

## Getting Started

1. **Clone this repository**

    Use the following command to clone this repository:

    ```bash
    git clone <repository-url>
    ```

2. **Copy the schedule and location files**

    Open your file explorer and copy the `SAPGUI_Schedule.testsuite` and `10.1.1.1.location` files.

3. **Paste the files into your Functional Tester project**

    In your Functional Tester project that contains the SAP GUI test, paste the files into the project base.

4. **Update the schedule**

    Open `SAPGUI_Schedule.testsuite` and add your existing SAP GUI test.

5. **Check in the project into GIT**

    Use the following commands to add your changes and push them to the repository:

    ```bash
    git add .
    git commit -m "Add SAP GUI test"
    git push
    ```

6. **Clone the repository on the server**

    On the DevOpsTest server, clone the repository.

7. **Connect a Performance Agent**

    Connect a Performance Agent that has the SAP GUI runtime installed.

8. **Execute the schedule on the server**

    Execute `SAPGUI_Schedule.testsuite` on the server.
