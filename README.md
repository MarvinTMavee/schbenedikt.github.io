<!DOCTYPE html>
<html>
<head>
  <title>My GitHub Projects</title>
  <style>
    body {
      background-color: #f0f0f0;
      font-family: Arial, sans-serif;
    }
    
    .container {
      display: flex;
      max-width: 70%;
      margin: 0 auto;
      padding: 40px;
      background-color: #f0f0f0;
      border-radius: 20px;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
      transform: scale(0.95);
      transition: transform 0.3s ease;
    }
    
    .container:hover {
      transform: scale(1);
    }
    
    .sidebar {
      flex-basis: 30%;
      padding-right: 20px;
    }
    
    .profile-img {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      margin-bottom: 20px;
      box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.1);
      transform: rotate(-2deg);
      transition: transform 0.3s ease;
    }
    
    .profile-img:hover {
      transform: rotate(0deg) scale(1.05);
      box-shadow: 6px 6px 12px rgba(0, 0, 0, 0.2);
    }
    
    .about {
      background-color: #f8f8f8;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
      cursor: pointer;
      position: relative;
    }
    
    .about:hover {
      transform: rotate(0deg) scale(1.02);
      box-shadow: 6px 6px 12px rgba(0, 0, 0, 0.2);
    }
    
    .about h2 {
      margin-top: 0;
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
      transition: text-shadow 0.3s ease;
    }
    
.about {
  position: relative;
  width: auto;
  height: 200px;
  background-color: #f8f8f8;
  border-radius: 8px;
  transition: transform 0.3s;
}

.about:hover {
  transform: scale(1.1);
  z-index: 2;
}
    
    .projects {
      flex-basis: 70%;
    }
    
    .project {
      background-color: #f8f8f8;
      padding: 20px;
      margin-bottom: 20px;
      border-radius: 10px;
      box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }
    
    .project:hover {
      transform: scale(1.09);
      box-shadow: 6px 6px 12px rgba(0, 0, 0, 0.2);
    }
    
    .project h2 {
      margin-top: 0;
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
      transition: text-shadow 0.3s ease;
    }
    
    .project:hover h2 {
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
    }
    
    .project p {
      margin-bottom: 10px;
      color: #666;
    }
    
    .project a {
      display: inline-block;
      padding: 8px 12px;
      background-color: #fff;
      color: #333;
      border-radius: 5px;
      box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
      text-decoration: none;
    }
    
    .project a:hover {
      transform: scale(1.05);
    }
    
    .overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      opacity: 0;
      visibility: hidden;
      transition: opacity 0.3s ease, visibility 0.3s ease;
    }
    
    .overlay.active {
      opacity: 1;
      visibility: visible;
    }
    
    .overlay-content {
      background-color: #fff;
      padding: 40px;
      border-radius: 10px;
      box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.1);
      transform: scale(0.9);
      transition: transform 0.3s ease;
      position: relative;
    }
    
    
    .overlay.active .overlay-content {
      transform: scale(1);
    }
    
    .close-btn {
  position: absolute;
  top: 10px;
  right: 10px;
  width: 24px;
  height: 24px;
  background-color: transparent;
  border: none;
  cursor: pointer;
}

.close-icon {
  position: relative;
  width: 100%;
  height: 100%;
}

.close-icon:before, .close-icon:after {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  width: 2px;
  height: 100%;
  background-color: #000;
  transform: translate(-50%, -50%) rotate(45deg);
  transition: background-color 0.3s, transform 0.3s;
}

.close-icon:after {
  transform: translate(-50%, -50%) rotate(-45deg);
}

.close-btn:hover .close-icon:before, .close-btn:hover .close-icon:after {
  background-color: #a30b0b;
  transform: translate(-50%, -50%) rotate(45deg) scale(1.1);
}

.close-btn:hover .close-icon:after {
  transform: translate(-50%, -50%) rotate(-45deg) scale(1.1);
}

  </style>
</head>
<body>
  <div class="container">
    <div class="sidebar">
      <div class="about" onclick="openOverlay('about')">
        <img class="profile-img" src="profile_picture.jpg" alt="Profile Picture">
        <h2>About Me</h2>
        <p>I'm a passionate developer with a love for coding and creating innovative solutions. I enjoy working on various projects and exploring new technologies.</p>
        <p>Feel free to explore my GitHub repositories and see the projects I've been working on.</p>
      </div>
    </div>
    <div class="projects">
      <div class="project" onclick="openOverlay('project1')">
        <h2>Project 1</h2>
        <p>This is the description of Project 1. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <a href="#">View Project</a>
      </div>
      <div class="project" onclick="openOverlay('project2')">
        <h2>Project 2</h2>
        <p>This is the description of Project 2. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <a href="#">View Project</a>
      </div>
      <div class="project" onclick="openOverlay('project3')">
        <h2>Project 3</h2>
        <p>This is the description of Project 3. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        <a href="#">View Project</a>
      </div>
    </div>
  </div>
  
  <div class="overlay" id="overlay">
    <div class="overlay-content" id="overlay-content">
      <div class="close-btn" onclick="closeOverlay()">
        <div class="close-icon"></div>
      </div>
      <h2 id="overlay-title">About Me</h2>
      <p id="overlay-description">I'm a passionate developer with a love for coding and creating innovative solutions. I enjoy working on various projects and exploring new technologies.</p>
      <p>Feel free to explore my GitHub repositories and see the projects I've been working on.</p>
    </div>
  </div>

  <script>
    function openOverlay(contentType) {
      var overlay = document.getElementById("overlay");
      var overlayContent = document.getElementById("overlay-content");
      var overlayTitle = document.getElementById("overlay-title");
      var overlayDescription = document.getElementById("overlay-description");

      if (contentType === "about") {
        overlayTitle.textContent = "About Me";
        overlayDescription.textContent = "I'm a passionate developer with a love for coding and creating innovative solutions. I enjoy working on various projects and exploring new technologies.";
      } else if (contentType === "project1") {
        overlayTitle.textContent = "Project 1";
        overlayDescription.textContent = "This is the description of Project 1. Lorem ipsum dolor sit amet, consectetur adipiscing elit.";
      } else if (contentType === "project2") {
        overlayTitle.textContent = "Project 2";
        overlayDescription.textContent = "This is the description of Project 2. Lorem ipsum dolor sit amet, consectetur adipiscing elit.";
      } else if (contentType === "project3") {
        overlayTitle.textContent = "Project 3";
        overlayDescription.textContent = "This is the description of Project 3. Lorem ipsum dolor sit amet, consectetur adipiscing elit.";
      }

      overlay.classList.add("active");
    }
    
    function closeOverlay() {
      var overlay = document.getElementById("overlay");
      overlay.classList.remove("active");
    }
  </script>
</body>
</html>
das ist mein neuer code
