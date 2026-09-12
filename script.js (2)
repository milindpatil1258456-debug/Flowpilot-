/* =========================
   FLOWPILOT JAVASCRIPT
========================= */


/* MOBILE MENU */

const menuBtn = document.getElementById("menuBtn");
const mobileMenu = document.getElementById("mobileMenu");

if (menuBtn && mobileMenu) {

    menuBtn.addEventListener("click", () => {

        mobileMenu.classList.toggle("open");

        menuBtn.textContent =
            mobileMenu.classList.contains("open")
            ? "✕"
            : "☰";
    });

    mobileMenu.querySelectorAll("a").forEach(link => {

        link.addEventListener("click", () => {

            mobileMenu.classList.remove("open");
            menuBtn.textContent = "☰";

        });

    });
}


/* =========================
   TASK PAGE
========================= */

const taskList = document.querySelector(".task-list");
const taskStatus = document.getElementById("taskStatus");
const addTaskBtn = document.getElementById("addTaskBtn");


function updateTasks() {

    if (!taskList || !taskStatus) return;

    const tasks = taskList.querySelectorAll(".task-check");

    let remaining = 0;

    tasks.forEach(task => {

        if (!task.classList.contains("checked")) {
            remaining++;
        }

    });

    taskStatus.textContent =
        remaining + (remaining === 1 ? " task remaining" : " tasks remaining");
}


function activateTaskButton(button) {

    button.addEventListener("click", () => {

        button.classList.toggle("checked");

        if (button.classList.contains("checked")) {

            button.textContent = "✓";

        } else {

            button.textContent = "";

        }

        updateTasks();

    });

}


/* Activate existing tasks */

if (taskList) {

    const taskButtons =
        taskList.querySelectorAll(".task-check");

    taskButtons.forEach(button => {

        activateTaskButton(button);

    });

    updateTasks();
}


/* Add new task */

if (addTaskBtn && taskList) {

    addTaskBtn.addEventListener("click", () => {

        const name = prompt("Enter task name:");

        if (!name || !name.trim()) return;

        const row = document.createElement("div");

        row.className = "task-row";

        row.innerHTML = `
            <button class="task-check"></button>

            <div>
                <strong>${name.trim()}</strong>
                <small>Today • New task</small>
            </div>

            <span class="task-tag medium">
                New
            </span>
        `;

        taskList.appendChild(row);

        const newButton =
            row.querySelector(".task-check");

        activateTaskButton(newButton);

        updateTasks();

    });
}


/* =========================
   NEW PROJECT BUTTON
========================= */

const newProjectBtn =
    document.getElementById("newProjectBtn");

if (newProjectBtn) {

    newProjectBtn.addEventListener("click", () => {

        const projectName =
            prompt("Enter your new project name:");

        if (!projectName || !projectName.trim()) return;

        alert(
            "Project '" +
            projectName.trim() +
            "' has been created!"
        );

    });
}


/* =========================
   BUTTON FEEDBACK
========================= */

const actionButtons =
    document.querySelectorAll(".price-btn");

actionButtons.forEach(button => {

    button.addEventListener("click", event => {

        event.preventDefault();

        const originalText =
            button.textContent;

        button.textContent =
            "Coming soon ✓";

        setTimeout(() => {

            button.textContent =
                originalText;

        }, 1500);

    });

});
/* =========================
   NEW PROJECT BUTTON
========================= */

document.addEventListener("DOMContentLoaded", function () {

    const addProjectBtn =
        document.getElementById("addProjectBtn");

    if (!addProjectBtn) return;

    addProjectBtn.onclick = function () {

        const projectName = prompt(
            "Enter your project name:"
        );

        if (projectName === null) return;

        const cleanName = projectName.trim();

        if (cleanName === "") {
            alert("Please enter a project name.");
            return;
        }

        alert(
            "✓ Project '" +
            cleanName +
            "' has been created successfully!"
        );
    };

});
/* =========================
   SETTINGS PAGE
========================= */

const saveProfile =
    document.getElementById("saveProfile");

if (saveProfile) {

    saveProfile.addEventListener("click", () => {

        const originalText =
            saveProfile.textContent;

        saveProfile.textContent =
            "✓ Changes Saved";

        setTimeout(() => {

            saveProfile.textContent =
                originalText;

        }, 1800);

    });

}


const logoutBtn =
    document.getElementById("logoutBtn");

if (logoutBtn) {

    logoutBtn.addEventListener("click", () => {

        alert("You have been logged out of the demo.");

    });

}
/* =========================
   NOTIFICATIONS
========================= */

const notificationBtn =
    document.getElementById("notificationBtn");

const notificationPanel =
    document.getElementById("notificationPanel");

if (notificationBtn && notificationPanel) {

    notificationBtn.addEventListener("click", () => {

        notificationPanel.classList.toggle("show");

    });

}
