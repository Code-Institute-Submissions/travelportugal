# Travel Portugal
<p align="center">
<img width="800" height="600" src="https://github.com/Brainvibe/travelportugal/blob/master/wireframes/website_screenshot.png">
</p>

Live version [here](https://brainvibe.github.io/travelportugal/)
## Index

* [Project description](#project-description)
* [UX](#ux)
* [Features](#features)
* [Wireframes](#wireframes)
* [Technologies](#technologies-used)
* [Testing](#testing)
* [Deployment](#deployment)
* [Credits](#credits)
* [Disclaimer](#disclaimer)

# Project description

Travel Portugal is a one page application designed to help users plan their next holidays and discover several touristic activities in Portugal. These activities include: accommodations, touristic attractions, restaurants, cafes, parks, bars and clubs. Users have available a list of recommendations of the most known places to visit in Portugal in order to help planning future holidays, with a brief description of each place.
Users can use the interactive map to search for all activities available in any city in portugal with more detailed information where it'll show all the information such as location, address, site and contact.

## UX

### Who is it for ? 

* Travel agencies that look to gather more information to create their holiday bundles.
* Tourists that want to plan their holidays or already booked a holiday to Portugal.
* Users curious about what Portugal has to offer as a holiday destination.

### User Stories

* As a tourist or Travel Agency, I want to find easily the information I need.
* As a general user, I want a contact option, in case I need more detailed information.
* As a tourist, I want to see recommended options to have an idea where to go or a starting point to plan my holidays.
* As a travel agency, I want to have information on all attractions or any specific activities in a certain location.
* As a tourist, I want to be able to find any commodities available to me on a specific city I want to visit.

## Features

### Existing Features

* Navbar 
    - Allows user to navigate easily through the different sections of the page.
* Weather 
    - Allows the user to know the current weather in the capital.
* Features section 
    - Gives a brief introduction on what the user can expect and search for using the interactive map, without overloading the user with a lot of information.
* Recommendations section 
    - A Carousel that shows the most visited attractions in Portugal, with a brief description on each one, easy to navigate, with arrows below the carousel or in a more interactive way, by dragging and moving the slides to pass through different attractions.
* Interactive map 
    - Using Google maps API, provides de user a map centered in Portugal. The user here is able to search for any city and any types of activities using the dropdown menu. 
* Autocomplete 
    - Integrated in the City input box, it helps the user choose the correct location when they type in what they're looking for.    
* Contact icon
    - Provides a simple way to contact Travel Portugal with a single click. It will show a simple form where the users can submit-request for information. User can close the form, and return to the page and keep browsing. EmailJS was used for the email send functionality.
* Footer - Provides links to the relevant social websites.

## Wireframes

* [Desktop](https://github.com/Brainvibe/travelportugal/blob/master/wireframes/desktop.png)
* [Mobile](https://github.com/Brainvibe/travelportugal/blob/master/wireframes/mobile.png)
* [Tablet](https://github.com/Brainvibe/travelportugal/blob/master/wireframes/tablet.png)

## Technologies Used

* **HTML** 
    - Used to create the main structure of the website.

* **CSS** 
    - Used to style and layout the website.

* [Bootstrap](https://getbootstrap.com/)
    - Framework used

* [JQuery](https://jquery.com)
    - The project uses **JQuery** to simplify DOM manipulation.

* [Font Awesome](https://fontawesome.com/)
    - All footer icons and contact bubble are from Font Awesome. 

* [Popper.js](https://popper.js.org/) 
    - Used for Navbar 

* [Github Pages](https://pages.github.com/) 
    - Used to host the live website. 

* [Google Fonts](https://fonts.google.com/) 
    - Pacifico and PT Sans Narrow fonts 

* [EmailJS](https://www.emailjs.com/)
    - Adds the ability to send emails from contact form.
* [Owl Carousel 2](https://owlcarousel2.github.io/OwlCarousel2/)
    - Touch enabled jQuery plugin that lets you create a responsive carousel slider.
* [Google Maps API](https://developers.google.com/maps/documentation/javascript/)
    - Used for the interactive map.
* [OpenWeather API](https://openweathermap.org/api)
    - To display current weather data

## Testing

* **W3C Validation Services**
  + Markup Validation Service 
    - It detected unused divs and alt="" missing from images tag. It was fixed.

  + W3C Link Checker 
    - No errors, all links working properly. Only two links were not able to be tested by the tool. Here's the console log:

            info Line: 333 https://www.facebook.com/
            Status: (N/A) Forbidden by robots.txt
            The link was not checked due to robots exclusion rules. Check the link manually. 
           
            info Line: 338 https://www.twitter.com/
            Status: (N/A) Forbidden by robots.txt
            The link was not checked due to robots exclusion rules. Check the link manually. 

    - Both links were tested manually and working.

  + CSS Validation service 
    - Warnings regarding Bootstrap and unknown vendor extensions. 
    - Detected unused classes. Removed and fixed. 

* **JSHint**
    - showed two errors with map.js:

            
            25	['pt'] is better written in dot notation.
            26	['pt'] is better written in dot notation.

    - changed and fixed the notation.

* **Google dev tools**
    - Audit tool
        - Accessibility - alt img tags were not correctly added for screen readers and lack of labels in contact form. Added the missing tags and fixed. It's now scored 100%.

        - SEO - It detected that there was no meta description, added meta description. It's now scored 100%.

        - Best Practices  
            - Images were not with the correct size. Resized all images with the correct resolution with [ResizeImage](https://resizeimage.net/).
            - The score is now 93%.

        - Performance 
            - Images were too big and therefore causing loading times to increase, converted all images to webp and used fall back option so they can be rendered the images in png on browsers that don't support webp like Apple devices. I used the image compression feature from [ResizeImage](https://resizeimage.net/). 

            - Perfomance score may vary since it depends on third party vendors and APIs to load 

            - Audit detected "Serve static assets with an efficient cache policy 20 resources found" , this can only be fixed on the server side which I don't have access to. The resolution would be to set a longer cache lifetime to speed up repeat visits to our page. I've researched and with the help of my mentor, and unfortunately there's no way to set it to a longer cache.

        
            

* **Non-automated testing:**

    - Links:

        - Checked all links especially the footer social icons, to make sure they were opening on a new tab correctly.

    - Contact form:

         -Tried to submit the empty form and verify that an error message about the required fields appears

        - Tried to submit the form with an invalid email address and verify that a relevant error message appears

        - Tried to submit the form with all inputs valid and verify that a success message appears with a alert message.

    - Carousel
        - Tested all buttons and dragging through different sections with no visibile errors in the console or on its function.

    - Map search

        - Input city - Searched for cities outside Portugal, to test if the country restriction was working.
        - Tested all different categories in the dropdown menus, while checking the console for any additional errors. 
        - Tested autocomplete by typing the first letters or any city from Portugal.

* **Tested Devices**
    - Apart from using the dev tools to see if the site was responsive across different resolutions I've tested all features on the following devices:
        + One Plus 7 pro
        + Fire HD 10
        + Ipad
        + Iphone 11
        + Macbook Pro 13"
        + Windows Desktop

* **Browsers**
    - To ensure browser compatibility I've tested all features above on the following browsers:
        + Edge
        + Chrome
        + Firefox
        + Safari

  

## Deployment

This page is hosted in GitHub Pages, here's how to deploy it.

    Log into GitHub.
    Go to settings and scroll down to GitHub Pages section.
    Select as a source master branch.
    The page is now automatically refreshed and the project is deployed.
    To access the project scroll down again to GitHub Pages section and click on the provided link.
    Link also at top of this Readme file.

How to run this project locally.

    Go to Travel Portugal repository page.
    Click on "Clone or download" green button.
    Copy the URL to the repository.
    Open the terminal in your local IDE.
    Choose the working directory where you would like to have the cloned repository.
    Type git clone, and add the URL you copied from Github: git clone https://github.com/brainvibe/travelportugal.git .
    Press Enter and your local clone will be created.

## Credits

### Content

* The text from *Recommendations* section was copied from [Google Travel](https://www.google.com/travel/)

### Media

* Recommendation section Photos were download from [Google Travel](https://www.google.com/travel)
* Main photos were downloaded from [Pexels](https://www.pexels.com/)

### Acknowledgements

* Auto-hide collapse menu code from [here](https://stackoverflow.com/questions/42401606/how-to-hide-collapsible-bootstrap-4-navbar-on-click).
* Smooth Scrolling from [W3schools](https://www.w3schools.com/howto/howto_css_smooth_scroll.asp).
* Opaque overlay from the Whiskey Drop Code institute mini-project.
* EmailJS implementation from Code institute MailJS lesson.
* Google maps API Part of the code was from documentation available from examples.
* Locations search adaptation from [stackoverflow](https://stackoverflow.com/)
* Webp fallback image load from [CSS-tricks](https://css-tricks.com/using-webp-images/)

As usual I want to thank my mentor *Victor Miclovich* for his great knowledge and experience with valuable feedback in our mentoring sessions.

## Disclaimer

### All content for educational use only.

