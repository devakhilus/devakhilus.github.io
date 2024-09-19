---
# the default layout is 'page'
icon: fas fa-project-diagram
order: 6
---

<div class="project-showcase">
    <h2>Project Showcase</h2>
    
    <div class="projects">
        <div class="project-item" onclick="toggleInfo(this)">
            <strong>• Project 1</strong>
            <div class="project-info">
                <p>This is a brief description of Project 1.</p>
            </div>
        </div>
        
        <div class="project-item" onclick="toggleInfo(this)">
            <strong>• Project 2</strong>
            <div class="project-info">
                <p>This is a brief description of Project 2.</p>
            </div>
        </div>
        
        <div class="project-item" onclick="toggleInfo(this)">
            <strong>• Project 3</strong>
            <div class="project-info">
                <p>This is a brief description of Project 3.</p>
            </div>
        </div>
        <div class="project-item" onclick="toggleInfo(this)">
            <strong>• Project 4</strong>
            <div class="project-info">
                <p>This is a brief description of Project 4.</p>
            </div>
        </div>
        <div class="project-item" onclick="toggleInfo(this)">
            <strong>• Project 5</strong>
            <div class="project-info">
                <p>This is a brief description of Project 5.</p>
            </div>
        </div>
        <div class="project-item" onclick="toggleInfo(this)">
            <strong>• Project 6</strong>
            <div class="project-info">
                <p>This is a brief description of Project 6.</p>
            </div>
        </div>
    </div>
</div>

<style>
    .project-showcase {
        margin: 20px; /* Adjust margin to fit your layout */
        padding: 20px;
        background-color: rgba(128, 128, 128, 0.5); /* Gray and transparent background */
        border-radius: 8px;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    }

    .project-item {
        cursor: pointer;
        padding: 10px;
        border: 1px solid #ddd;
        border-radius: 5px;
        margin-bottom: 10px;
        transition: background-color 0.3s;
    }

    .project-item:hover {
        background-color: rgba(231, 241, 255, 0.8); /* Match hover effect to your design */
    }

    .project-info {
        max-height: 0;
        overflow: hidden;
        transition: max-height 0.3s ease-out;
        padding: 0 10px;
        color: #666;
    }

    .show {
        max-height: 100px; /* Adjust based on content */
        padding-top: 10px; /* Add some padding when shown */
    }
</style>

<script>
    function toggleInfo(currentProject) {
        // Get all project info sections
        const allProjects = document.querySelectorAll('.project-info');

        // Close all other project info sections
        allProjects.forEach(info => {
            const projectItem = info.parentNode; // Get the parent project element
            if (info !== currentProject.querySelector('.project-info')) {
                info.classList.remove('show');
                info.style.maxHeight = null; // Collapse it
            } else {
                // If it’s the clicked one, toggle its visibility
                if (info.classList.contains('show')) {
                    info.classList.remove('show');
                    info.style.maxHeight = null; // Collapse it
                } else {
                    info.classList.add('show');
                    info.style.maxHeight = info.scrollHeight + "px"; // Expand it
                }
            }
        });
    }
</script>
