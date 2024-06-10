---
title: "Portfolio website design"
date: false
draft: false
tags: [projects]
publish: true
---

# Personal Portfolio Website

Welcome to my personal portfolio website! This website showcases my projects, skills, and experience. It is designed to be modern, professional, and visually appealing. **You can use my code adding reference**

>[!done] Live Demo
> Check out the live demo of my portfolio [here](https://sajib3489.github.io/my-portfolio-website/). You can download the full repository from my [github](https://github.com/SAJIB3489/my-portfolio-website.git)

Check the [GIF Live demo here](https://github.com/SAJIB3489/my-portfolio-website/blob/main/images/live_demo.gif)

## Features

- **Responsive Design:** The website is fully responsive and works seamlessly on different devices and screen sizes.
- **Modern UI:** A sleek and modern user interface that highlights my work.
- **Easy Navigation:** Simple and intuitive navigation to explore different sections of my portfolio.
- **Project Showcase:** Detailed sections for my projects with descriptions and links.

## Technologies Used

- HTML5
- CSS3

> ## Code

> #### HTML
`index.html`

```
<!DOCTYPE html>
<html lange="en">
<head>
    <meta charset="UTF-8">
    <link rel="shortcut icon" href="images/icon.png"/>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Md Sajib Pramanic</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://kit.fontawesome.com/f9036f1f6b.js" crossorigin="anonymous"></script>
</head>
<body>
<div id="header">
    <div class="container">
        <nav>
            <img src="images/logo.png" class="logo">
            <ul id="sidemenu">
                <li><a href="#header">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
                <i class="fa-solid fa-xmark" onclick="closemenu()"></i>
            </ul>
            <i class="fa-solid fa-bars" onclick="openmenu()"></i>
        </nav>
        <div class="header-text">
            <p>Software Developer</p>
            <h1>Hi, I'm <span>Sajib</span><br>Pramanic From Finland</h1>
        </div>
    </div>
</div>
<div id="about">
    <div class="container">
        <div class="row">
            <div class="about-col-1">
                <img src="images/user.png">
            </div>
            <div class="about-col-2">
                <h1 class="sub-title">About Me</h1>
                <p class="justified-text">Olen omistautunut oppimaan ja kasvamaan. Tärkein intohimoni
                kohde on pysyä mukana teknologian uusimman kehityksen
                mukana, ja olen innokas oppimaan uutta. Rakastan luistelua, ja
                jäällä olen oppinut eniten suomalaisista.</p>

                <div class="tab-titles">
                    <p class="tab-links active-link" onclick="opentab('skills')">Skills</p>
                    <p class="tab-links" onclick="opentab('experience')">Experience</p>
                    <p class="tab-links" onclick="opentab('education')">Education</p>
                </div>
                <div class="tab-contents active-tab" id="skills">
                    <ul>
                        <li><span>Software Development</span><br>Robotics Software Development</li>
                        <li><span>App Development</span><br>Building Android</li>
                        <li><span>Cloud Computing</span><br>Thingsboard</li>
                    </ul>
                </div>
                <div class="tab-contents" id="experience">
                    <ul>
						 <li><span>11/10/2023 - Present</span><br>Software Developer Trainee - University of Eastern Finland
                        <br><br>Developed a ROS-based navigation system for the Ceterio C-100 AMR robot
Leveraged ROS for sensor data acquisition, message passing, and actuator
control for the robot.
Developed a SLAM algorithm within the ROS framework for the Ceterio C-100 AMR
robot, enabling autonomous map building and localization. Performed
comprehensive testing.
                        
                        <br><br>Skills: ROS 1 ·  ROS 2 ·  SLAM ·  Simulation ·  Linux · Computer vision </li>
						
                        <li><span>01/06/2023 - 31/08/2023</span><br>IoT Trainee - Holobiont Oy
                        <br><br>Experienced in Mobile Application Development with a focus
                        on creating, testing, and deploying applications for IoT data collection.
                        Skilled in Cloud Structure Implementation, contributing to the design and 
                        implementation of secure and scalable solutions for data storage and analytics from IoT devices.
                        Proven ability in Team Collaboration, actively participating in coding,
                        debugging, and successful project execution within cross-functional teams.

                        <br><br>Skills: Holobiont device · BME280 · Temperature Sensors · Pressure Sensors · Thingsboard · ESP32 · Mobile Application Development · Cloud Computing </li>

                        <li><span>14/04/2023 - 30/06/2023</span><br>Intern- MindSphere Smart Factory cloud data analysis and create Augmented Reality(AR) 
                        <br><br>This internship presents the implementation and analysis
                        of a cloud-based data analysis system in a Smart Factory environment,
                        along with the development of an Augmented Reality (AR) system tailored
                        for the Savonia University of Applied Sciences Smart Factory. The primary
                        objective of this project was to leverage advanced technologies to enhance the
                        factory's capabilities in terms of visualization, monitoring, and decision making. 
                        
                            <br><br>Skills: MindSphere · Smart Factory · Aurgmented Reality(AR).</li>

                        <li><span>01/01/2023 - 31/03/2023</span><br>Intern- MindSphere Water Process 
                        Cloud Data Analysis at Savonia University of Applied Science
                        <br><br>I have contributed to the development of data analysis solutions for water
                        level processes and smart factories using the Mindsphere platform. I
                        collaborated with data engineers, automation engineers, and other
                        stakeholders to design, develop, and test data models and algorithms. I have
                        developed the digital Twin with an EXCEL simulator and MATLAB simulator.
                        Additionally, I conducted an analysis of large datasets, identified trends, and
                        patterns, and effectively communicated insights to stakeholders using
                        various data visualization tools and techniques. Lastly, I presented the
                        project in Germany.
                        <br><br>Skills: MindSphere · Digital Twin · Cloud Computing · Data Analytics · Water process.</li>

                        <li><span>PROJECT</span></li>
                        <li><span>09/01/2023 - 30/04/2023</span><br>ABB Robotics: Robot station to disassemble Smart factory products
                            <br><br>This project aimed to develop an efficient and accurate robotic
                            system for disassembling Smart Factory products, utilizing an ABB robot
                            for its precision and advanced control. The project was a response to the
                            growing need for sustainable manufacturing and waste reduction. The project
                            was conducted in phases, starting with system design and simulation, followed
                            by implementation and testing in RobotStudio. The system's performance was then
                            evaluated to identify areas for improvement. <a href="https://www.linkedin.com/feed/update/urn:li:activity:7057622866623635456/" target="_blank">See the Result</a>
                            <br><br>Skills: 3D Printing · Robot Programming · Robot Operating System (ROS) · Robotic Process Automation (RPA).</li>
                            
                        <li><span>01/09/2022 - 20/12/2022</span><br>Big data and Artificial Intelligence in IoT
                            <br><br>During the project, we gained hands-on experience in collecting,
                            processing, and analysing big data in IoT. We developed a solid understanding
                            of AI techniques and algorithms commonly used in IoT applications. Our skills in
                            data visualization and dashboard development for IoT were enhanced significantly.
                            Throughout the project, we delved into the challenges and opportunities of implementing
                            AI in IoT, including privacy and security concerns, which broadened our perspective on the
                            subject matter. As part of the project, we honed our written and verbal communication skills
                            by preparing reports and delivering presentations on the topics of big data and AI in IoT. This
                            allowed us to effectively convey our findings and insights to both technical and non-technical audiences. <a href="https://www.linkedin.com/in/md-sajib-pramanic-866849245/details/experience/1635524183781/single-media-viewer/?profileId=ACoAADzQtY4B1ReS9LJFQa6cs1Axo-5kB7pQ9E8" target="_blank">See the article</a>
                            <br><br>Skills: Artificial Intelligence (AI) · Internet of Things (IoT) · Big Data.</li>
                    </ul>
                </div>
                <div class="tab-contents" id="education">
                    <ul>
                        <li><span>2022-2025</span><br>B.Eng Information Technology (IoT) from Savonia UAS, Finland</li>
                        <li><span>03/2023</span><br>Erasmus Short Program(3 days), Carl-Benz-Schule Gaggenau, Germany</li>
                        <li><span>2015-2019</span><br>Vocational Degree in Civil Engineering, Faridpur Polytechnic Institute</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</div>
<!-----------------about---------------------->
<div id="services">
    <div class="container">
        <h1 class="sub-title">My Services</h1>
        <div class="services-list">
            <div>
                <i class="fa-solid fa-code"></i>
                <h2>Software Developer</h2>
                <p class="justified-text">Looking to elevate your software solution? I can develop
                Feel free to contact me to bring your vision to life!</p>
                <a href="#">Learn more</a>
            </div>
            <div>
                <i class="fa-brands fa-app-store"></i>
                <h2>Apps Development</h2>
                <p class="justified-text">Need sleek and user-friendly apps for your business? Look no further! I can develop customized apps to elevate
                 your customer experience. Feel free to contact me and let's turn your vision into reality!</p>
                <a href="#">Learn more</a>
            </div>
            <div>
                <i class="fa-solid fa-cloud"></i>
                <h2>Cloud Architect</h2>
                <p class="justified-text">Transform your business with cutting-edge cloud solutions! As a skilled Cloud Architect, I am here to optimize
                 your infrastructure, streamline operations, and maximize efficiency. Feel free to contact me, and let's take your business
                 to new heights in the cloud!</p>
                <a href="#">Learn more</a>
            </div>
        </dive>
    </div>
</div>

<!-----------------services---------------------->

<div id="portfolio">
    <div class="container">
        <h1 class="sub-title">My Work</h1>
        <div class="work-list">
            <div class="work">
                <img src="images/Image5.jpg">
                <div class="layer">
                    <h3>Self-Balancing Table</h3>
                    <p>A self-balancing table that can adapt to any uneven surface.</p>
                    <a href="https://github.com/SAJIB3489/Balancing_Table.git"target="_blank"><i class="fa-sharp fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>
            </div>
            <div class="work">
                <img src="images/image6.jpg">
                <div class="layer">
                    <h3>Health Monitoring Apps</h3>
                    <p>The innovative concept of health monitoring facilitated by mobile applications.</p>
                    <a href="https://github.com/SAJIB3489/Health_Monitoring.git"target="_blank"><i class="fa-sharp fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>
            </div>
            <div class="work">
                <img src="images/work-1.png">
                <div class="layer">
                    <h3>Disassemble the products</h3>
                    <p>Disassemble the smart factory product by using ABB Gofa CRB 15000</p>
                    <a href="https://www.linkedin.com/feed/update/urn:li:activity:7057622866623635456/"target="_blank"><i class="fa-sharp fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>
            </div>
            <div class="work">
                <img src="images/work-2.png">
                <div class="layer">
                    <h3>Develop a Augmented Reality(AR) </h3>
                    <p>Develop a Augmented Reality(AR) in Savonia Smart Factory</p>
                    <a href="https://amksavonia-my.sharepoint.com/personal/md_sajib_pramanic_edu_savonia_fi//_layouts/15/onedrive.aspx?login_hint=md%2Esajib%2Epramanic%40edu%2Esavonia%2Efi&id=%2Fpersonal%2Fmd%5Fsajib%5Fpramanic%5Fedu%5Fsavonia%5Ffi%2FDocuments%2FPractical%20Training%202b%2FInternship%20Report%2Epdf&parent=%2Fpersonal%2Fmd%5Fsajib%5Fpramanic%5Fedu%5Fsavonia%5Ffi%2FDocuments%2FPractical%20Training%202b"target="_blank"><i class="fa-sharp fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>
            </div>
            <div class="work">
                <img src="images/work-3.png">
                <div class="layer">
                    <h3>Online Shop</h3>
                    <p>It is a online E-Commerce Website. Currently the website is under construction.</p>
                    <a href="http://www.finnma.fi/"target="_blank"><i class="fa-sharp fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>
            </div>
        </div>
        <a href="#" class="btn">See more</a>
    </div>
</div>

<!-----------------portfolio---------------------->
<div id="contact">
    <div class="container">
        <div class="row">
            <div class="contact-left">
                <h1 class="sub-title">Contact Me</h1>
                <p><i class="fa-solid fa-paper-plane"></i> Md.Pramanic@edu.savonia.fi</p>
                <p><i class="fa-solid fa-mobile-screen-button"></i> +358 414703498</p>
                <div class="social-icons">
                    <a href="https://www.facebook.com/SajibPramanic"target="_blank"><i class="fa-brands fa-facebook"></i></a>
                    <a href=""><i class="fa-brands fa-twitter-square"></i></a>
                    <a href="https://www.instagram.com/msp_sajib/"target="_blank"><i class="fa-brands fa-instagram"></i></a>
                    <a href="https://www.linkedin.com/in/md-sajib-pramanic-866849245/"target="_blank"><i class="fa-brands fa-linkedin"></i></a>
                    <a href="https://github.com/SAJIB3489"target="_blank"><i class="fa-brands fa-github"></i></a>
                </div>
                <a href="images/Resume_Md_Sajib_Pramanic.pdf"target="_blank" download class="btn btn2">Download CV</a>
            </div>
            <div class="contact-right">
                <form name="submit-to-google-sheet">
                    <input type="text" name="Name" placeholder="Your Name" required>
                    <input type="email" name="Email" placeholder="Your Email" required>
                    <textarea name="Message" rows="6" placeholder="Your Message"></textarea>
                    <button type="submit" class="btn btn2">Submit</button>
                </form>
                <span id="msg"></span>
            </div>
        </div>
    </div>
    <div class="copyright">
        <p>Copyright © Sajib. <i class="fa-solid fa-heart"></i></p>
    </div>

</div>


<!-----------------contact---------------------->

<script>

    var tablinks = document.getElementsByClassName("tab-links");
    var tabcontents = document.getElementsByClassName("tab-contents");

    function opentab(tabname){
        for(tablink of tablinks){
            tablink.classList.remove("active-link");
        }
        for(tabcontent of tabcontents){
            tabcontent.classList.remove("active-tab");
        }
        event.currentTarget.classList.add("active-link")
        document.getElementById(tabname).classList.add("active-tab")
    }


</script>

<script>
    
    var sidemenu = document.getElementById("sidemenu");

    function openmenu(){
        sidemenu.style.right = "0";
    }
    function closemenu(){
        sidemenu.style.right = "-200px";
    }

</script>
<script>
    const scriptURL = 'https://script.google.com/macros/s/AKfycbyG5eO4sQItgfUBrf_7jNaiSVlLc0unaasPgjSaHzcRm9Hb4OSh-OMu-eMfc4vP1FRo/exec'
    const form = document.forms['submit-to-google-sheet']
    const msg = document.getElementById("msg")
  
    form.addEventListener('submit', e => {
      e.preventDefault()
      fetch(scriptURL, { method: 'POST', body: new FormData(form)})
        .then(response => {
            msg.innerHTML = "Message sent Successfully"
            setTimeout(function(){
                msg.innerHTML = ""
            },5000)
            form.reset()
        })
        .catch(error => console.error('Error!', error.message))
    })
  </script>
</body>
</html>
```


> #### CSS
`style.css`

```
*{
    margin: 0;
    padding: 0;
    font-family: 'Poppins', sans-serif;
    box-sizing: border-box;
}
html{
    scroll-behavior: smooth;
}
body{
    background: #080808;
    color: #fff;
}
#header{
    width: 100%;
    height: 100vh;
    background-image: url(images/background.png);
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
}
.container{
    padding: 10px 10%;
}
nav{
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
}
.logo{
    width: 140px;
}

nav ul li{
    display: inline-block;
    list-style: none;
    margin: 10px 20px;
}
nav ul li a{
    color: #fff;
    text-decoration: none;
    font-size: 18px;
    position:relative;
}
nav ul li a::after{
    content: '';
    width: 0%;
    height: 3px;
    background: #ff004f;
    position: absolute;
    left: 0;
    bottom: -6px;
}
nav ul li a:hover::after{
    width: 100%;
}
.header-text{
    margin-top: 20%;
    font-size: 30px;
}
.header-text h1{
    font-size: 60px;
    margin-top: 20px;
}
.header-text h1 span{
    color: #ff004f;
}
/*--------------------about------------------*/
#about{
    padding: 80px 0;
    color: #ababab;
}
.row{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.about-col-1{
    flex-basis: 35%;
}
.about-col-1 img{
    width: 100%;
    border-radius: 15px;
}
.about-col-2{
    flex-basis: 60%;
}
.sub-title{
    font-size: 60px;
    font-weight: 600;
    color: #fff;
}
.justified-text {
    text-align: justify;
}
.tab-titles{
    display: flex;
    margin: 20px 0 40px;
}
.tab-links{
    margin-right: 50px;
    font-size: 18px;
    font-weight: 500;
    cursor: pointer;
    position: relative;
}
.tab-links::after{
    content: '';
    width: 0;
    height: 3px;
    background: #ff004f;
    position: absolute;
    left: 0;
    bottom: -8px;
    transition: 0.5s;
}

.tab-links.active-link::after{
    width: 50%;
}
.tab-contents ul li{
    list-style: none;
    margin: 10px 0;
}
.tab-contents ul li span{
    color: #b54769;
    font-size: 16px;
}
.tab-contents{
    display: none;
}
.tab-contents.active-tab{
    display: block;
}

/*------------------------services---------------------------*/
#services{
    padding: 30px 0;
}
.services-list{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 40px;
    margin-top: 50px;
}
.services-list div{
    background: #262626;
    padding: 40px;
    font-size: 13px;
    font-size: 13px;
    font-weight: 300;
    border-radius: 10px;
    transition: background 0.5s, transform 0.5s;

}
.services-list div i{
    font-size: 50px;
    margin-bottom: 30px;
}
.services-list div h2{
    font-size: 30px;
    font-weight: 500;
    margin-bottom: 15px;
}
.services-list div a{
    text-decoration: none;
    color: #fff;
    font-size: 12px;
    margin-top: 20px;
    display: inline-block;
}
.services-list div:hover{
    background: #ff004f;
    transform: translateY(-10px);
}
#portfolio{
    padding: 50px 0;
}
.work-list{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 40px;
    margin-top: 50px;
}
.work{
    border-radius: 10px;
    position: relative;
    overflow: hidden;
}
.work img{
    width: 100%;
    border-radius: 10px;
    display: block;
    transition: transform 0.5s;
}
.layer{
    width: 100%;
    height: 0%;
    background: linear-gradient(rgba(0,0,0,0.6), #ff004f);
    border-radius: 10px;
    position: absolute;
    left: 0;
    bottom: 0;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 0 40px;
    text-align: center;
    font-size: 14px;
    transition: height 0.5s;
}
.layer h3{
    font-weight: 500;
    margin-bottom: 20px;
}
.layer a{
    margin-top: 20px;
    color: #ff004f;
    text-decoration: none;
    font-size: 18px;
    line-height: 60px;
    background: #fff;
    width: 60px;
    border-radius: 50%;
    text-align: center;
}
.work:hover img{
    transform: scale(1.1);
}
.work:hover .layer{
    height: 100%;
}
.btn{
    display: block;
    margin: 50px auto;
    width: fit-content;
    border: 1px solid #ff004f;
    padding: 14px 50px;
    border-radius: 6px;
    text-decoration: none;
    color: #fff;
    transition: background 0.5s;
}
.btn:hover{
    background: #ff004f;
}

/*------------------contact-------------*/
.contact-left{
    flex-basis: 35%;
}
.contact-right{
    flex-basis: 60%;
}
.contact-left p{
    margin-top: 30px;
}
.contact-left p i{
    color: #ff004f;
    margin-right: 15px;
    font-size: 25px;
}
.social-icons{
    margin-top: 30px;
}
.social-icons a{
    text-decoration: none;
    font-size: 30px;
    margin-right: 15px;
    color: #ababab;
    display: inline-block;
    transition: transform 0.5s;
}
.social-icons a:hover{
    color: #ff004f;
    transform: translateY(-5px);
}
.btn.btn2{
    display: inline-block;
    background: #ff004f;
}
.contact-right form{
    width: 100%;
}
form input, form textarea{
    width: 100%;
    border: 0;
    outline: none;
    background: #262626;
    padding: 15px;
    margin: 15px 0;
    color: #fff;
    font-size: 18px;
    border-radius: 6px;
}
form .btn2{
    padding: 14px 60px;
    font-size: 18px;
    margin-top: 20px;
    cursor: pointer;
}
.copyright{
    width: 100%;
    text-align: center;
    padding: 25px 0;
    background: #262626;
    font-weight: 300;
    margin-top: 20px;
}
.copyright i{
    color: #ff004f;
}
/* --------------------------css for small screen---------------- */
nav .fa-solid{
    display: none;
}

@media only screen and (max-width: 600px){
    #header{
        background-image: url(images/phone-background.png);
    }
    .header-text{
        margin-top: 100%;
        font-size: 16px;
    }
    .header-text h1{
        font-size: 30px;
    }
    nav .fa-solid{
        display: block;
        font-size: 25px;
    }
    nav ul{
        background: #ff004f;
        position: fixed;
        top: 0;
        right: -200px;
        width: 200px;
        height: 100vh;
        padding-top: 50px;
        z-index: 2;
        transition: right 0.5s;
    }
    nav ul li{
        display: block;
        margin: 25px;
    }
    nav ul .fa-solid{
        position: absolute;
        top: 25px;
        left: 25px;
        cursor: pointer;
    }
    .sub-title{
        font-size: 40px;
    }
    .about-col-1, .about-col-2{
        flex-basis: 100%;
    }
    .about-col-1{
        margin-bottom: 30px;
    }
    .about-col-2{
        font-size: 14px;
    }
    .tab-links{
        font-size: 16px;
        margin-right: 20px;
    }
    .contact-left, .contact-right{
        flex-basis: 100%;
    }
    .copyright{
        font-size: 14px;
    }
}
#msg{
    color: #61b752;
    margin-top: -40px;
    display: block;

}
```


> [!note] Note
> Before started using **Quartz**, I used it to showcase my profile. I got the design idea from [Avinash Kr](https://linktr.ee/iamavinashkr), Thanks to him.