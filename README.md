# git-remote-onedrive
A Git remote helper that allows you to use OneDrive folders as Git remotes, perfect for financial organizations and teams using Microsoft 365

## Here are the key highlights:

### 🏗️ Project Architecture

- Frontend: React with Tailwind CSS for a modern, responsive UI
- Backend: Flask API handling Microsoft Graph authentication and Git operations
- Structure: Professional open-source layout similar to git-remote-dropbox

### 🚀 Key Features

- OAuth2 authentication with Microsoft Graph API
- Visual folder selection (personal OneDrive + SharePoint)
- Git repository detection and remote setup
- Step-by-step guided UI workflow
- CI/CD pipeline with GitHub Actions
- PyPI package distribution ready

## Quick Start

### Installation


## Setup

### Register Azure App (one-time setup):

- Go to Azure Portal > App registrations
- Create new app with redirect URI: http://localhost:3000/callback
- Note your Client ID and Tenant ID


### Configure environment:
`
bashexport ONEDRIVE_CLIENT_ID="your-client-id"
export ONEDRIVE_TENANT_ID="your-tenant-id"
`

### Initialize with a repository:
`
bashcd your-git-repo
git remote add onedrive onedrive://path/to/folder
git push onedrive main
`

Usage
Adding OneDrive as a remote
bash# Add personal OneDrive folder
git remote add onedrive onedrive://Documents/MyProject

# Add SharePoint folder
git remote add sharepoint onedrive://sites/TeamSite/Shared%20Documents/Projects/MyProject

# Push to OneDrive
git push onedrive main

# Clone from OneDrive
git clone onedrive://Documents/MyProject local-folder
Web Interface
Launch the setup interface:
bashgit-remote-onedrive-setup
This opens a web browser where you can:

Authenticate with Microsoft
Browse and select OneDrive/SharePoint folders
Configure Git remotes with a visual interface

How It Works
This tool implements a Git remote helper that:

Authentication: Uses OAuth2 to authenticate with Microsoft Graph API
Storage: Stores Git data as compressed bundles in OneDrive folders
Synchronization: Handles concurrent access and conflict resolution
Metadata: Maintains refs and Git metadata in structured JSON files

Development
See docs/development.md for development setup and contributing guidelines.
License
MIT License - see LICENSE file.
Contributing

Fork the repository
Create your feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add some amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request

Security
For security concerns, please email security@yourdomain.com instead of using the issue tracker.
Acknowledgments

Inspired by git-remote-dropbox
Built with Microsoft Graph API
React frontend with modern UI/UX