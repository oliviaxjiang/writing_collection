Here are the instructions for getting started with the chemiSOLO project:

1. **Accept GitHub Invitation and Clone Project:**
   - Check your email for an invitation from GitHub to join the project. Accept the invitation.
   - Clone the repository to your local machine. You can use the following command in your terminal:
     ```
     git clone <repository-url>
     ```

2. **Open the Project in Visual Studio Code:**
   - Open Visual Studio Code.
   - Navigate to 'File' -> 'Open Folder'.
   - Select the `chemiSOLO` folder where you cloned the repository and open it.

3. **Install Node.js:**
   - Install Node.js on your computer if it's not already installed. The project may not allow the newest Node version. I use Node version 17 and it works fine. You can download it from [Node.js official website](https://nodejs.org/).

4. **Install Dependencies and Run Linting:**
   - Open the terminal in Visual Studio Code.
   - Execute the following commands to install project dependencies and run linting:
     ```
     yarn install
     yarn lint
     ```

5. **Serve the Project:**
   - In the terminal, enter the following command to start the server:
     ```
     yarn serve
     ```

6. **Modify Loading Behavior:**
   - After starting the project, if the web page is stuck in loading mode, follow these steps to adjust the code:
   - Navigate to `chemiSOLO/src/components/Layout.vue`.
   - Comment out lines 152 to 154.
   - Change line 173 from:
     ```
     ...mapState(["showloading"]),
     ```
     to:
     ```
     ...mapState({showloading: state => false}),
     ```
   - This modification prevents the page from indefinitely waiting for a device connection.
