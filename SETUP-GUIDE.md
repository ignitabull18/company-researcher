# Coolify Deployment Guide for Company Researcher

This guide provides step-by-step instructions for deploying the Company Researcher application to your Coolify instance.

## 1. Prerequisites

*   A running Coolify instance.
*   A private GitHub repository containing the application code.
*   The Coolify GitHub App installed and configured for your repository.
*   The necessary API keys for the application (e.g., Exa, Anthropic, YouTube, GitHub).
*   A domain name configured with a DNS A record pointing to your Coolify instance's IP address (`193.203.167.44`). For example, `company-researcher.ignitabull.org`.

## 2. Create a New Application in Coolify

1.  **Log in** to your Coolify dashboard.
2.  Navigate to the **Applications** section.
3.  Click the **+ New** button to create a new resource and select **Application**.

## 3. Configure the Source

1.  Select **GitHub App** as your source.
2.  Choose your private GitHub repository (`ignitabull18/company-researcher`).
3.  Select the **`main`** branch.

## 4. Configure Build Settings

Coolify's Nixpacks will automatically detect that this is a Next.js project and handle the build process for you. The default settings should work correctly.

*   **Build Pack**: **Nixpacks**
*   **Install Command**: (leave blank)
*   **Build Command**: (leave blank)
*   **Start Command**: (leave blank)

## 5. Configure Networking

*   **Port**: **`3000`** (This is the default port for a Next.js application).
*   **FQDN (Fully Qualified Domain Name)**: Enter the domain you configured in the prerequisites (e.g., `http://company-researcher.ignitabull.org`).

## 6. Configure Environment Variables

In the **Environment Variables** section of your application settings, add the following keys and their corresponding values:

*   `EXA_API_KEY`
*   `ANTHROPIC_API_KEY`
*   `YOUTUBE_API_KEY`
*   `NEXT_PUBLIC_GITHUB_TOKEN`

## 7. Save and Deploy

1.  Click the **Save** button to save your application configuration.
2.  Click the **Deploy** button to start the deployment process.

## 8. Monitor the Deployment

*   You can monitor the deployment process in the **Deployments** tab for your application.
*   If the deployment is successful, you will see a "running" status, and your application will be available at the FQDN you configured. 