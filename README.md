# 🚀 FTP Deployment Workflow

This GitHub Actions workflow automates the deployment of your project to an FTP server whenever changes are pushed to the `main` branch.

## Workflow Function

- **Trigger:** The workflow runs automatically on every push to the `main` branch.
- **Jobs:**
  - **Checkout Repository:** Checks out the latest code from the repository.
  - **Upload to FTP:** Uses the [FTP-Deploy-Action](https://github.com/SamKirkland/FTP-Deploy-Action) to upload the repository contents to a specified FTP server using FTPS protocol.

## Configuration

The workflow requires the following secrets to be set in your GitHub repository settings:

- `FTP_SERVER` - The FTP server address.
- `FTP_USERNAME` - The username for FTP authentication.
- `FTP_PASSWORD` - The password for FTP authentication.
- `FTP_PORT` - The port number for the FTP server.

The files are uploaded to the root directory (`/`) of the FTP server from the root of the repository (`./`).

This workflow helps streamline deployment by automatically uploading your project files to your FTP server on every update to the main branch.

## How to Use

1. Ensure your project repository is hosted on GitHub.
2. Push your code changes to the `main` branch to trigger the workflow automatically.
3. Set the required FTP secrets (`FTP_SERVER`, `FTP_USERNAME`, `FTP_PASSWORD`, `FTP_PORT`) in your GitHub repository settings under **Settings > Secrets and variables > Actions**.
4. The workflow will checkout your repository and upload the files to the specified FTP server using FTPS.
5. Monitor the workflow run in the **Actions** tab of your GitHub repository to verify successful deployment.

This setup allows you to automate deployment to your FTP server with every update to your main branch, reducing manual steps and ensuring your server is always up to date.
