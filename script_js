// Toggle navigation menu for mobile
function toggleMenu() {
    const nav = document.querySelector("nav ul");
    nav.classList.toggle("show");
}

document.querySelector(".menu-icon").addEventListener("click", toggleMenu);

// Smooth scrolling for navigation links
document.querySelectorAll("nav a").forEach(anchor => {
    anchor.addEventListener("click", event => {
        event.preventDefault();
        const targetId = anchor.getAttribute("href").substring(1);
        document.getElementById(targetId).scrollIntoView({ behavior: "smooth" });
    });
});

// Filter projects by category
function filterProjects(category) {
    document.querySelectorAll(".project").forEach(project => {
        project.style.display = project.classList.contains(category) ? "block" : "none";
    });
}

// Lightbox effect for project images
function openLightbox(image) {
    const modal = document.createElement("div");
    modal.classList.add("lightbox");
    modal.innerHTML = `
        <div class="modal-content">
            <img src="${image.src}" alt="${image.alt}">
            <button onclick="closeModal()">Close</button>
        </div>`;
    document.body.appendChild(modal);
}

function closeModal() {
    document.querySelector(".lightbox").remove();
}

// Contact form validation
function validateForm(event) {
    event.preventDefault();
    let valid = true;

    document.querySelectorAll("input, textarea").forEach(field => {
        const errorSpan = field.nextElementSibling;
        if (!field.value.trim()) {
            valid = false;
            field.style.border = "2px solid red";
            errorSpan.innerText = "Required!";
        } else {
            field.style.border = "2px solid green";
            errorSpan.innerText = "";
        }
    });

    if (valid) alert("Form submitted successfully!");
}

// Ensure interactive elements load correctly
document.addEventListener("DOMContentLoaded", () => {
    console.log("JavaScript Loaded Successfully");
});
