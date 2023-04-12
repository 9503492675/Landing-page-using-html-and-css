# Landing-page-using-html-and-css
Internship project oasis infobyte 

Overview
Our landing page is crucial. By designing an impressive landing page, we can create compelling content, draw viewers, and turn them into potential clients. Therefore, it's essential to comprehend what makes a landing page remarkable and what to avoid while building the website.In this article, we'll learn how to use HTML and CSS to build a landing page.

Introduction
Any web page on which a customer can land is a landing page, but in the context of marketing, it's typically a standalone page. In contrast to web pages, we design our landing pages with a single emphasis or goal, known as a "call to action." In essence, it's the next phase before a visitor converts to a client. It enables us to exchange contact information for trade, unique offers, pieces of information, or transactions. Landing pages are the ideal option for increasing the conversion rates of our marketing campaigns.

Pre-requisites
Make sure you understand the following fundamental ideas of HTML & CSS before continuing :

Flex-box
pseudo elements
CSS Combinators
CSS Animations
CSS media queries
Hamburger menu CSS
How are We Going to Build the Landing Page?
In this article, we'll create a landing page for a restaurant.




Approach
We will walk through the following steps to create a captivating landing page with HTML and CSS.Create the basic structure using HTML.Build a responsive Hamburger navigation menu.Create a hero section.Beautify using CSS.The Best Practices When Creating a Landing PageClarify, on't omplicate: Our call to action (CTA) and unique selling proposition (USP) should be prominently displayed. We need not go too specific. We need to make it clear to visitors what we are offering and what they must contribute in exchange.
Make it neat: For maximum impact, we must keep our landing page basic and clean, with less text and carefully chosen images.
The test is vital: Testing is crucial to ensure that our landing page produces leads. We must create, put it into action, and then capture the results. We can change it if it's not working.
Final Output
After creating the landing page, we would arrive at something like this:

DESKTOP VIEW :

final-output-desktop-view

MOBILE VIEW :

final-output-mobile-view

Building the Landing Page Using HTML and CSS
1. Creating the Basic Structure Using HTML
The two primary sections of the landing page are the header and the hero sections. The header area contains the navigation menu, while the hero section has some text and images. We will learn more about the hero section later.

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="styles.css">
    <title>Document</title>
    
<!-- Include this CDN for using icons     -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">

</head>



<body>
    <!-- header section starts  -->
    

    <header>
<!--  This will contain the navigation menu -->
     
    </header>

    <!-- header section ends -->
    

    <!-- hero section starts  -->
<!-- This will contain the brief description about our product (here, restaurant)  -->

<!--  hero section ends -->


</body>

</html>
2. Adding the Basic CSS
The below code includes the necessary CSS. We have imported a Google font and created a dark background.

 @import url("https://fonts.googleapis.com/css2?family=Jacques+Francois+Shadow&display=swap");
    * {
        font-family: "Nunito", sans-serif;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        outline: none;
        border: none;
        text-decoration: none;
        text-transform: capitalize;
        transition: all 0.2s linear;
    }
    
    html {
        font-size: 62.5%;
        overflow: hidden;
    }
    
    body {
        background: #212531;
        margin: 0;
    }
    
    header {
        margin: 0px;
    }
3. Creating a Responsive Hamburger Menu
In the header's section we will create a responsive hamburger navigation menu . A hamburger menu turns the navigation bar on and off by hiding it behind the button or displaying it.Usually, it is for smaller displays and mobile devices. However, PC websites may also employ CSS hamburger menus.

Adding the HTML
We have the main navigation menu and a container for creating the hamburger icon.
The navigation menu consists of a few links.
Since we are using pure CSS, we will control the state of the icon, i.e., whether to show and hide the navbar using the HTML checkbox.
We will specify an id for the checkbox and associate it with the label using the for attribute. Clicking the will select and deselect the checkbox. Then we will toggle the checkbox using CSS.
   <!-- header section starts  -->

    <header>

        <section class="nav">
            <!-- We can also insert any logo here     -->

            <!-- We can also insert any logo here     -->
            <div class="logo">
                <a href="#"><i class="fas fa-utensils"></i>food</a>
            </div>

            <!--  checkbox to control the icon's state    -->
            <input id="menu-toggle" type="checkbox" />
            <label class='menu-button-container' for="menu-toggle">
                <div class='menu-button'></div>
              </label>
            <!--  main menu    -->
            <ul class="menu">
                 <li><a href="#home">Home</a></li>
                <li><a href="#speciality">About</a></li>
                <li> <a href="#popular">Popular</a></li>
                <li> <a href="#review">Contact</a></li>
                <li> <a href="#order" class="order">Menu</a></li>
            </ul>
        </section>




    </header>

    <!-- header section ends -->
Styling the Responsive Hamburger Menu with CSS
We will style the main menu nav and the hamburger menu-button-container.
To draw the three lines for the hamburger icon, we’ll use the ::before and ::after pseudo-elements. The CSS for this is:
    a {
        text-decoration: none;
        color: #000;
    }
    
    ul {
        list-style: none;
    }
    
/* styling the logo  */

    .logo {
        font-size: 2.5rem;
        font-weight: bolder;
        color: #666;
        display: inline-block;
    }
    
    .logo i {
        padding-right: 2rem;
        color: black;
    }
    
    .order {
        text-shadow: -1px -1px 0 yellow, 1px -1px 0 yellow, -1px 1px 0 yellow, 1px 1px yellow;
    }

/* Stying the navbar container */
    
    .nav {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        background: white;
        color: black;
        height: 65px;
        padding: 1em;
        font-size: 25px;
    }
    
    .menu li:hover {
        cursor: pointer;
        transform: scale(1.2);
    }
    
    .menu {
        display: flex;
        flex-direction: row;
        list-style-type: none;
        margin: 0;
    }
    
    .menu>li {
        margin: 0 1rem;
        overflow: hidden;
    }
    /*Container for menu button  */
    
    .menu-button-container {
        display: none;
        height: 100%;
        width: 30px;
        cursor: pointer;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    
    #menu-toggle {
        display: none;
    }
    /*  Creating the hamburger menu button  */
    
    .menu-button,
    .menu-button::before,
    .menu-button::after {
        display: block;
        background-color: black;
        position: absolute;
        height: 6px;
        width: 32px;
        border-radius: 3px;
        color: white;
    }
    
    .menu-button::before {
        content: "";
        margin-top: -8px;
    }
    
    .menu-button::after {
        content: "";
        margin-top: 8px;
    }
Adding Functionality to The Hamburger Menu with CSS
We will move the top and bottom bars or lines of the icon to the position of the middle line.
We will hide the middle line.
Lastly, we will rotate the top and bottom lines 45 degrees in opposite directions to create a cut/cross icon.
 /*  Adding Functionality to the Hamburger Menu with CSS  */
    
    #menu-toggle:checked+.menu-button-container .menu-button::before {
        margin-top: 0px;
        transform: rotate(45deg);
    }
    
    #menu-toggle:checked+.menu-button-container .menu-button {
        background: rgba(255, 255, 255, 0);
    }
    
    #menu-toggle:checked+.menu-button-container .menu-button::after {
        margin-top: 0px;
        /*  transforms the hamburger icon into a cross  */
        transform: rotate(-45deg);
    }
    
Responsive Navbar Using CSS Media Queries
We will add the CSS media queries to make our hamburger navbar responsive.
We must select a screen width that will toggle a full-width menu and the responsive CSS hamburger menu.
 /* media queries  */
    
    @media (max-width: 991px) {
        html {
            font-size: 55%;
        }
        header {
            padding: 2rem;
        }
        section {
            padding: 2rem;
        }
    }
    
    @media (max-width: 768px) {
        .menu-button-container {
            display: flex;
        }
        .menu {
            position: absolute;
            top: 0;
            margin-top: 50px;
            left: 0;
            flex-direction: column;
            width: 100%;
            justify-content: center;
            align-items: center;
            padding: 2rem
        }
        .menu li:hover {
            transform: scale(1);
        }
        #menu-toggle~.menu li {
            height: 0;
            margin: 0;
            padding: 0;
            border: 0;
        }
        #menu-toggle:checked~.menu li {
            border: 1px solid #9f9a9a;
            height: 2.5em;
            padding: 0.5em;
        }
        .menu>li {
            display: flex;
            justify-content: center;
            margin: 0;
            padding: 0.5em 0;
            width: 100%;
            color: black;
            background-color: #e8e8e8;
        }
        .menu>li:not(:last-child) {
            border-bottom: 1px solid #444;
        }
    }
NAVBAR OUTPUT
DESKTOP VIEW :
navbar-output-desktop-view

MOBILE VIEW :
navbar-output-mobile-view

4. Creating the Hero Section
What is a hero section ?
A backdrop image, video, illustration, or animation, along with text and occasionally a call to action, make up a hero section. A hero section is an area that appears on the screen beneath our logo and menu as the first thing visitors see when they arrive at our website.

This portion of the page should ideally cover the following information :

What services do we provide?
Why should others believe us?

What are the advantages of collaborating with us?

What should they do after that?

How to design a hero section ?

The Hero Image: Use a captivating graphic, also known as a "hero image." These are undoubtedly the most significant elements of the hero section since, in contrast to lines of text, consumers are typically more drawn to vibrant designs, captivating images, and movies that provide engaging information.

The powerful tagline: The headline of our hero section is crucial in determining whether a site visitor is interested or bored enough to click the "Back" button.

Subheadings: We should include concise descriptions of our services or products.

CTA: A bold, distinct, and engaging call to action is necessary.

Structure of the hero section - Adding HTML

In this example, our hero picture is a depiction of a burger. To make the image more memorable in the user's mind, we will animate it using CSS transitions. By staring at the colors and textures of the dish, one can quickly get hungry in no time.
We'll incorporate a catchy tagline and a brief explanation of the product.
The CTA, in this case, is the order now button. The "order now" button directs the user to order food from the restaurant.
<!--    hero section starts  -->

    <section class="home" id="home ">
      <div class="content">
          
        <!-- Tagline -->
        <h3 class="mainfont">
          The Ch<span class="yellowColor">ee</span>se Decker
        </h3>
        <h3>
          fastest f<span class="yellowColor">oo</span>d for , instant
          <span class="yellowColor">Hunger</span>
        </h3>
        <!--Description  -->
        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptas
          accusamus tempore temporibus rem amet laudantium animi optio
          voluptatum. Natus obcaecati unde porro nostrum ipsam itaque impedit
          incidunt rem quisquam eos!
        </p>

        <!-- CTA -->
        <a href="# " class="btn">ORDER NOW</a>
      </div>
        
      <!-- Hero image -->

      <div class="image">
        <img src="burger-img.png " alt=" " />
      </div>
    </section>

    <!-- hero section ends   -->

Adding CSS :

We'll make use of the flexbox to design our hero section.
We will display the tagline and description on the left, with the hero image on the right.
To highlight the essential elements of our design, we'll use the color yellow.
We will animate the image using keyframes and transforms.
 /* Styling the hero section */
    
    .home {
        display: flex;
        flex-wrap: wrap;
        gap: 1.5rem;
        min-height: 100vh;
        align-items: center;
    }
    
    .home .content {
        flex: 1 1 40rem;
        padding-top: 6.5rem;
    }
    /* Styling the main image */
    
    .home .image {
        flex: 1 1 30rem;
    }
    
    .home .image img {
        width: 90%;
        height: 90%;
        padding: 1rem;
        animation: float 3s linear infinite;
    }
    /* animating the main image   */
    
    @keyframes float {
        0%,
        100% {
            transform: translateY(0rem);
        }
        50% {
            transform: translateY(3rem);
        }
    }
    
    .home .content h3 {
        font-size: 5rem;
        color: white;
    }
    /* Styling the content */
    
    .yellowColor {
        color: yellow;
    }
    
    .mainfont {
        font-family: "Jacques Francois Shadow", cursive;
    }
    
    .home .content p {
        font-size: 1.7rem;
        color: white;
        padding: 1rem 0;
    }
    
    .heading {
        text-align: center;
        font-size: 3.5rem;
        padding: 1rem;
        color: #666;
    }
    /* Styling the button  */
    
    .btn {
        display: inline-block;
        padding: 0.8rem 3rem;
        border: 0.2rem solid white;
        color: white;
        cursor: pointer;
        font-size: 1.7rem;
        border-radius: 0.5rem;
        position: relative;
        overflow: hidden;
        z-index: 0;
        margin: 1rem 1rem 0 0;
    }
    
    .btn:hover {
        color: #fff;
    }
/* Adding media queries to make it responsive   */
 @media (max-width: 450px) {
        html {
            font-size: 50%;
            overflow-x: hidden;
            overflow-y: scroll;
            text-align: center;
        }
    }



Output:

DESKTOP VIEW :
final-desktop-view-landing-page

MOBILE VIEW :

final-mobile-view-landing-page

The landing page is now ready.

Final Code
HTML

<!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="styles.css" />
    <title>Document</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" />
</head>

<body>
    <!-- header section starts  -->

    <header>
        <section class="nav">
            <!-- We can also insert any logo here     -->

            <!-- We can also insert any logo here     -->
            <div class="logo">
                <a href="#"><i class="fas fa-utensils"></i>food</a>
            </div>

            <!--  checkbox to control the icon's state    -->
            <input id="menu-toggle" type="checkbox" />
            <label class="menu-button-container" for="menu-toggle">
          <div class="menu-button"></div>
        </label>
            <!--  main menu    -->
            <ul class="menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#speciality">About</a></li>
                <li><a href="#popular">Popular</a></li>
                <li><a href="#review">Contact</a></li>
                <li><a href="#order" class="order">Menu</a></li>
            </ul>
        </section>
    </header>

    <!-- header section ends -->

    <!-- hero section starts  -->

    <section class="home" id="home ">
        <div class="content">
            <!-- Tagline -->
            <h3 class="mainfont">
                The Ch<span class="yellowColor">ee</span>se Decker
            </h3>
            <h3>
                fastest f<span class="yellowColor">oo</span>d for , instant
                <span class="yellowColor">Hunger</span>
            </h3>
            <!--Description  -->
            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptas accusamus tempore temporibus rem amet laudantium animi optio voluptatum. Natus obcaecati unde porro nostrum ipsam itaque impedit incidunt rem quisquam eos!
            </p>

            <!-- CTA -->
            <a href="# " class="btn">ORDER NOW</a>
        </div>
        <!-- Hero image -->

        <div class="image">
            <img src="burger-img.png " alt=" " />
        </div>
    </section>

    <!-- hero section ends   -->
</body>

</html>
CSS
    @import url("https://fonts.googleapis.com/css2?family=Jacques+Francois+Shadow&display=swap");
    * {
        font-family: "Nunito", sans-serif;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        outline: none;
        border: none;
        text-decoration: none;
        text-transform: capitalize;
        transition: all 0.2s linear;
    }
    
    html {
        font-size: 62.5%;
        overflow: hidden;
    }
    
    body {
        background: #212531;
        margin: 0;
    }
    
    header {
        margin: 0px;
    }
    
<!--  styling the navigation menu -->
    
    a {
        text-decoration: none;
        color: #000;
    }
    
    ul {
        list-style: none;
    }
    
    section {
        padding: 2rem 9%;
    }
    
    .logo {
        font-size: 2.5rem;
        font-weight: bolder;
        color: #666;
        display: inline-block;
    }
    
    .logo i {
        padding-right: 2rem;
        color: black;
    }
    
    .order {
        text-shadow: -1px -1px 0 yellow, 1px -1px 0 yellow, -1px 1px 0 yellow, 1px 1px yellow;
    }
    
    .nav {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        background: white;
        color: black;
        height: 65px;
        padding: 1em;
        font-size: 25px;
    }
    
    .menu li:hover {
        cursor: pointer;
        transform: scale(1.2);
    }
    
    .menu {
        display: flex;
        flex-direction: row;
        list-style-type: none;
        margin: 0;
    }
    
    .menu>li {
        margin: 0 1rem;
        overflow: hidden;
    }
    /*Container for menu button  */
    
    .menu-button-container {
        display: none;
        height: 100%;
        width: 30px;
        cursor: pointer;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    
    #menu-toggle {
        display: none;
    }
    /*  Creating the menu button */
    
    .menu-button,
    .menu-button::before,
    .menu-button::after {
        display: block;
        background-color: black;
        position: absolute;
        height: 6px;
        width: 32px;
        border-radius: 3px;
        color: white;
    }
    
    .menu-button::before {
        content: "";
        margin-top: -8px;
    }
    
    .menu-button::after {
        content: "";
        margin-top: 8px;
    }
    /*  Adding Functionality to the Hamburger Menu with CSS  */
    
    #menu-toggle:checked+.menu-button-container .menu-button::before {
        margin-top: 0px;
        transform: rotate(45deg);
    }
    
    #menu-toggle:checked+.menu-button-container .menu-button {
        background: rgba(255, 255, 255, 0);
    }
    
    #menu-toggle:checked+.menu-button-container .menu-button::after {
        margin-top: 0px;
        /*  transforms the hamburger icon into a cross  */
        transform: rotate(-45deg);
    }
    /* Styling the hero section */
    
    .home {
        display: flex;
        flex-wrap: wrap;
        gap: 1.5rem;
        min-height: 100vh;
        align-items: center;
    }
    
    .home .content {
        flex: 1 1 40rem;
        padding-top: 6.5rem;
    }
    /* Styling the main image */
    
    .home .image {
        flex: 1 1 30rem;
    }
    
    .home .image img {
        width: 90%;
        height: 90%;
        padding: 1rem;
        animation: float 3s linear infinite;
    }
    /* animating the main image   */
    
    @keyframes float {
        0%,
        100% {
            transform: translateY(0rem);
        }
        50% {
            transform: translateY(3rem);
        }
    }
    
    .home .content h3 {
        font-size: 5rem;
        color: white;
    }
    /* Styling the content */
    
    .yellowColor {
        color: yellow;
    }
    
    .mainfont {
        font-family: "Jacques Francois Shadow", cursive;
    }
    
    .home .content p {
        font-size: 1.7rem;
        color: white;
        padding: 1rem 0;
    }
    
    .heading {
        text-align: center;
        font-size: 3.5rem;
        padding: 1rem;
        color: #666;
    }
    /* Styling the buttons  */
    
    .btn {
        display: inline-block;
        padding: 0.8rem 3rem;
        border: 0.2rem solid white;
        color: white;
        cursor: pointer;
        font-size: 1.7rem;
        border-radius: 0.5rem;
        position: relative;
        overflow: hidden;
        z-index: 0;
        margin: 1rem 1rem 0 0;
    }
    
    .btn:hover {
        color: #fff;
    }
    /* media queries  */
    
    @media (max-width: 991px) {
        html {
            font-size: 55%;
        }
        header {
            padding: 2rem;
        }
        section {
            padding: 2rem;
        }
    }
    
    @media (max-width: 768px) {
        .menu-button-container {
            display: flex;
        }
        .menu {
            position: absolute;
            top: 0;
            margin-top: 50px;
            left: 0;
            flex-direction: column;
            width: 100%;
            justify-content: center;
            align-items: center;
            padding: 2rem
        }
        .menu li:hover {
            transform: scale(1);
        }
        #menu-toggle~.menu li {
            height: 0;
            margin: 0;
            padding: 0;
            border: 0;
        }
        #menu-toggle:checked~.menu li {
            border: 1px solid #9f9a9a;
            height: 2.5em;
            padding: 0.5em;
        }
        .menu>li {
            display: flex;
            justify-content: center;
            margin: 0;
            padding: 0.5em 0;
            width: 100%;
            color: black;
            background-color: #e8e8e8;
        }
        .menu>li:not(:last-child) {
            border-bottom: 1px solid #444;
        }
    }
    
    @media (max-width: 450px) {
        html {
            font-size: 50%;
            overflow-x: hidden;
            overflow-y: scroll;
            text-align: center;
        }
    }

Conclusion
A landing page is a standalone page with a call to action goal.By designing a landing page, we can create compelling content, draw viewers, and turn them into potential clients.We should create a clean, organised landing page with fewer content and eye-catching graphics.The two primary sections of our landing page are the navigation menu and the hero section.
A backdrop image, video, illustration, or animation, along with text and occasionally a call to action, make up a hero section.A call to action (CTA) instructs the user to take some action on a website.Challenge Time!



