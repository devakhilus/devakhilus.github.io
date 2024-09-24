---
icon: fas fa-stream
icon: fas fa-project-diagram
order: 6
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project Showcase</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <style>
        /* Style for the project items */
        .project-item summary {
            font-size: 18px;
            font-weight: bold;
            padding: 10px;
            background-color: rgba(100, 149, 237, 0.2);
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease, color 0.3s ease;
            margin-bottom: 8px;
        }

        .project-item[open] summary {
            background-color: rgba(100, 149, 237, 0.7);
            color: #fff;
        }

        .project-item div {
            padding: 10px;
            background-color: rgba(245, 245, 245, 0.2); /* Lighter inner background */
            border-radius: 5px;
            transition: max-height 0.4s ease-in-out;
            overflow: hidden;
            max-height: 0;
        }

        .project-item[open] div {
            max-height: 1000px; /* Allows space for expanded content */
            padding: 15px;
        }

        .project-item {
            border: 1px solid #ddd;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            border-radius: 8px;
            margin-bottom: 15px;
            transition: transform 0.2s ease;
        }

        .project-item summary:hover {
            background-color: rgba(100, 149, 237, 0.5);
            color: #fff;
        }

        .project-item:hover {
            transform: translateY(-5px);
        }
    </style>
</head>
<body>

<h2><i class="fas fa-stream"></i> Project Showcase</h2>
<div id="github-projects">
    <!-- Projects will be injected here -->
</div>

<script>
    async function loadProjects() {
        try {
            const response = await fetch('{{ "/assets/projects.json" | relative_url }}');
            const repos = await response.json();

            const excludedRepos = ['devakhilus.github.io', 'devakhilus']; // Repos to exclude
            const projectContainer = document.getElementById('github-projects');

            repos
                .filter(repo => !excludedRepos.includes(repo.name)) // Filter out the excluded repos
                .forEach(repo => {
                    // Create the structure for each project item
                    const projectItem = document.createElement('details');
                    projectItem.classList.add('project-item');

                    const projectSummary = document.createElement('summary');
                    projectSummary.textContent = repo.name;

                    const projectInfo = document.createElement('div');
                    projectInfo.innerHTML = `
                        <p><strong>Description:</strong> ${repo.description || 'No description available.'}</p>
                        <p><strong>Language:</strong> ${repo.language || 'N/A'}</p>
                        <p><a href="${repo.html_url}" target="_blank">View Repository</a></p>
                    `;

                    // Append summary and info to the project item
                    projectItem.appendChild(projectSummary);
                    projectItem.appendChild(projectInfo);

                    // Append the project item to the container
                    projectContainer.appendChild(projectItem);
                });
        } catch (error) {
            console.error('Error loading projects:', error);
        }
    }

    // Load projects when the page loads
    document.addEventListener('DOMContentLoaded', loadProjects);
</script>

</body>
</html>
