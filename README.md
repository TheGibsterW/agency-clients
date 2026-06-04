# Agency Clients Dashboard

A dedicated repository for hosting automatically generated client dashboards through GitHub Pages. Each new client receives a personalized dashboard containing project status, important resources, onboarding progress, and agency materials—all automatically created and deployed.

## Purpose

This repository provides a centralized hub where clients can access their project information at any time. Every client dashboard includes:

- **Project Status** – Current phase and progress overview
- **Important Links** – Quick access to project resources and deliverables
- **Onboarding Progress** – Clear visibility into the implementation timeline
- **Agency Resources** – Relevant documents, guides, and support materials

## Repository Structure

Dashboards are organized with a simple, scalable folder structure:

```
agency-clients/
├── index.html
└── clients/
    ├── client-a/
    │   └── index.html
    ├── client-b/
    │   └── index.html
    └── ...
```

Each client receives their own dedicated folder within the `clients/` directory, containing a self-contained `index.html` file. This structure ensures clean organization as the agency onboards new clients.

## GitHub Pages

This repository uses GitHub Pages to automatically publish client dashboards as static websites. 

**Configuration:**
- **Settings** → Pages
- **Source** → Deploy from branch
- **Branch** → main
- **Folder** → / (root)

Once configured, dashboards become immediately accessible via URLs like:

```
https://username.github.io/agency-clients/clients/client-name/
```

Any changes committed to the main branch are automatically published within seconds.

## Creating a New Client Dashboard

Adding a new client dashboard is straightforward:

1. **Create a folder** – Add a new directory under `clients/` with the client name (e.g., `clients/acme-corp/`)
2. **Add index.html** – Place a dashboard HTML file in the new folder
3. **Commit and push** – Commit the changes to the main branch
4. **Published automatically** – GitHub Pages deploys the dashboard immediately

## Dashboard Content

Each client dashboard typically displays:

- **Company Name** – Client identifier
- **Package Type** – Service tier or offering
- **Start Date** – Project commencement date
- **Status** – Current project phase (e.g., In Progress, Completed)
- **Project Links** – URLs to deliverables and resources
- **Checklist** – Key milestones and completion status
- **Notes** – Important updates and next steps

## Example Structure

Here's a basic HTML structure for a client dashboard:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Client Dashboard</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            border-radius: 8px;
            margin-bottom: 30px;
        }
        .section {
            background: white;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .status-badge {
            display: inline-block;
            padding: 8px 12px;
            border-radius: 4px;
            font-weight: 600;
            font-size: 0.875rem;
        }
        .status-active {
            background-color: #d4edda;
            color: #155724;
        }
        .checklist {
            list-style: none;
            padding: 0;
        }
        .checklist li {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
        }
        .checklist li:before {
            content: "✓ ";
            color: #28a745;
            font-weight: bold;
            margin-right: 8px;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Client Name</h1>
        <p>Your Project Dashboard</p>
    </div>

    <div class="section">
        <h2>Project Overview</h2>
        <p><strong>Package Type:</strong> Premium</p>
        <p><strong>Start Date:</strong> January 15, 2024</p>
        <p><strong>Status:</strong> <span class="status-badge status-active">In Progress</span></p>
    </div>

    <div class="section">
        <h2>Onboarding Progress</h2>
        <ul class="checklist">
            <li>Initial consultation completed</li>
            <li>Strategy development</li>
            <li>Implementation phase</li>
        </ul>
    </div>

    <div class="section">
        <h2>Resources & Links</h2>
        <ul>
            <li><a href="#">Project Documentation</a></li>
            <li><a href="#">Support Portal</a></li>
            <li><a href="#">Performance Reports</a></li>
        </ul>
    </div>

    <div class="section">
        <p style="color: #666; font-size: 0.875rem; margin: 0;">
            For support inquiries, contact your account manager.
        </p>
    </div>
</body>
</html>
```

## Security Notes

⚠️ **Important:** This is a public repository accessible to the internet. Never commit sensitive information:

- **Do not store secrets** – API keys, tokens, or credentials
- **Do not store API keys** – Use secure, private systems for authentication
- **Do not store customer credentials** – Passwords and personal data must be kept confidential
- **Use private systems** – Store all sensitive information in secure platforms external to this repository

If sensitive data is accidentally committed, remove it immediately and rotate any exposed credentials.

## License

MIT License

---

For questions or contributions, please open an issue or contact the development team.
