![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# Nigel is 25: a birthday party invitation site

'Nigel is 25' is a site for a private client to send to his friends and family to invite them to his birthday celebration. It includes information about the activities and locations, as well as providing a quick and easy method of responding to the invite via the website. It will be useful for Nigel's friends and family to have a one-stop digital place they can go to learn about and remind themselves about his birthday celebration. It will also be useful for Nigel as a client to collect RSVP information including dietary requirements to inform his caterer in advance. 

AM I RESPONSIVE SCREENSHOT HERE

## REQUIREMENT GATHERING AND PLANNING

Before starting this project, I took some time to think about what the client needed and what the users (the people the client is inviting) needed from the website. I wrote a few user stories and extracted the user needs from them. These needs will also be a part of my manual testing plan. 

### User Stories:

As a birthday party host 
I want a birthday party website with all the information relating to my party
So that my potential guests can be easily kept informed from one central location

As a birthday party host
I want a stylish birthday party website 
So that my potential guests enjoy visiting it and get a good impression of my event

As a birthday party host
I want a responsive birthday party website
So that my potential guests have a good experience of my website from whichever device they choose to access it from

As a birthday party invitee
I want to be able to access all the information about the party in an easy, intuitive and complete way
So that I am fully informed and can communicate the information required from me

### User Needs:

- Information about the activity
- Information about the location
- Information about the date and time
- The ability to RSVP quickly and easily
- The ability to inform the host about dietary requirements quickly and easily
- Viewable on any device so it does not matter which device the website is accessed on
- Clear display and intuitive navigation for ease of use

### Initial Wireframe

With my list of requirements, I then created a very rough wireframe of the homepage on Balsamiq to inform the basic structure of my website: 

![Wireframe](assets/images/wireframe.png)

This evolved as I worked through the project. I chose to combine certain pages due to there not being enough content for the number of pages I initially planned. I also removed some features that I didn't think were needed to achieve the project, that I have put into the 'Features Left to Implement' section of this document. 

### Colour Palette

Having completed my rough wireframe, I took some time to pick a colour scheme. I was aiming for a vivid, stylish and energising palette. Here is what I chose:

![Colour palette](assets/images/colourpalette.png)

## FEATURES

For each item here you need the feature title, a screenshot of the feature and a short paragraph of the value it gives the user. 

### Existing Features

#### Logo

#### Navigation Bar

#### Footer 

#### RSVP Form

Includes a thank you page 

#### Maps

#### 404 Page

### Features Left To Implement

#### Party Playlist Compiler
This could either be some sort of simple form for people to submit their song requests in a text input, or it could be more sophisticated and allow people to add songs directly to a Spotify playlist. This would depend on the needs of the user and the time available. 

#### Gift Wishlist
Again, this could be kept simple with just an unordered list on the page, or an iframe to an external wishlist site, or it could be more complex with checkboxes and names to claim certain items so there is no duplication of gifts. This would depend on the user needs when fully scoped out. 

## TESTING

I completed the following types of testing throughout development and at the end of my project:

### Manual Feature Testing

As well as running through the list of user needs and ensuring all the features collectively meet all of the needs, I completed the following manual feature testing: 


| Feature           | Test Case | Outcome |
| ----------------  | -------   | ----    |
| Logo  |  Click on the logo     | The user is taken to the homepage  |
| Navigation Bar  |  Click on each of the three navigation items from each of the five pages   | The user is taken to the correct page each time   |
| RSVP Form |  Submit an empty form   | The mandatory fields (first three inputs) indicate they need filling in |
|   | Submit a filled in form | The user is taken to the form submission 'thank you' page |
| Footer| Click on each of the social media icons  | The user is taken to the correct social media platform each time. |
| Maps  | Click on the zoom in and out buttons | The map shows a zoomed in or zoomed out scale according to the which button is pressed      |
| | Click on the directions button | The user is taken to Google Maps with the destination pre-filled in the destination field |
| | Click on the 'View Larger Map' link | The user is taken to a full screen Google Maps of the same location |
| 404 Page | Add some random letters to the end of the url in the browser| The user is taken to the custom 404 page      |

###


- **Screen size responsiveness:** I used Chrome Devtools to check three key screen sizes (mobile, tablet and computer), as well as using the responsive setting to slide the width from narrow all the way through to wide to check the transition points.
- **Performance and accessibility testing:** I used Lighthouse in Chrome Devtools to detect any issues.
- **Code validator testing**
    - HTML via [W3C](https://validator.w3.org/)
    - CSS via [Jigsaw](https://jigsaw.w3.org/css-validator/)
- **Browser compatibility testing:** I clicked through my whole site in each of the three key screen sizes on Chrome, Safari, Firefox and Edge.

Below is a list of bugs with the type of testing they were found via. 

(Add screenshots before and after to make your readme as visual as possible)

### Resolved Bugs

#### Manual Testing

1. The title above the YouTube video is not aligned with the left edge of the video, whereas the title above the image next to the YouTube video is (see image below).

#### Screen Size Responsiveness

2. The super-wide screen made the All Bar One image on the homepage look small compared to the YouTube Video. I found that this was because the size of the image was too small, so I replaced it with a bigger image and this solved that issue (see image below).

**BEFORE**
![Bugs One + Two](assets/images/bug-one-two.png)

**AFTER**

3. I found that when scaling the screen using the responsive setting in Chrome Devtools, a certain size between tablet and computer screens made the table on my 'The Details' page go off the edge. I found that removing the 'width: 100vh' property from the `<section>` that this table was in for my largest screen media query solved this. 

**BEFORE**
![Bug Three](assets/images/bug-three.png)

**AFTER**


#### Accessibility Testing 
4. I originally had #372C57 colour text on a background of #E3705F got my navigation bar but this was flagged: 'Background and foreground colors do not have a sufficient contrast ratio.' So I changed this to black text.

**BEFORE**
![Bug Four](assets/images/bug-four.png)

**AFTER**

5. My iframes did not have titles. I added these.

**BEFORE**

```
<section id="axe-map">
            <h2>HATCHET HARRY'S</h2>
            <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1490.086074424065!2d-0.14141171848554995!3d50.822537632392745!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487585653b74d2bd%3A0x332a353bf7d065c6!2sHatchet%20Harry%E2%80%99s%20Axe%20Throwing%20-%20Brighton!5e0!3m2!1sen!2suk!4v1706522841105!5m2!1sen!2suk"
                width="100%" height="350" class="embedded-map" loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"></iframe>
        </section>
        <hr>
        <section id="bar-map">
            <h2>ALL BAR ONE</h2>
            <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2520.4795604140204!2d-0.14118602241553058!3d50.822280560520504!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4875850a7d29e78d%3A0x94943c4bcb70d18d!2sAll%20Bar%20One%20Brighton!5e0!3m2!1sen!2suk!4v1706522950686!5m2!1sen!2suk"
                width="100%" height="350" class="embedded-map" allowfullscreen="" loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"></iframe>
        </section>
```

**AFTER**


6. My social media icons did not have names. I added these. 

**BEFORE**
```
        <div>
            <a href="www.instagram.com" target="_blank"><i class="fa-brands fa-square-instagram"></i></a>
            <a href="www.facebook.com" target="_blank"><i class="fa-brands fa-square-facebook"></i></a>
            <a href="www.twitter.com" target="_blank"><i class="fa-brands fa-square-x-twitter"></i></a>
        </div>
```
**AFTER**

7. I had used h3 elements to emphasise something on a page which was not in-keeping with the sequentially-descending headings rule. 

**BEFORE**
![Bug Seven](assets/images/bug-seven.png)

**AFTER**

8. Although lighthouse did not flag this to me, I saw that I had not added any aria-labels for images and links, so I added these too. 

**BEFORE**
![Bug Eight](assets/images/bug-eight.png)

**AFTER**

9. Although Lighthouse did not flag this to me, I noticed that the navigation bar does not have the semantic tag `<button>` to help screen readers.

**BEFORE**
![Bug Nine](assets/images/bug-nine.png)

**AFTER**

10. The footer did not remain at the bottom of the page on the 404.html page. I saw that this was because the property to do this was assigned to the `<body>` tag but I had accidentally omitted this tag in the 404.html file. 

**BEFORE**
![Bug Ten](assets/images/bug-ten.png)

**AFTER**

### Unresolved Bugs

I don't believe I have left any of my bugs unresolved.

## DEPLOYMENT

The site was deployed to GitHub pages. 

The steps to deploy are as follows:
- In the GitHub repository, navigate to the Settings tab
- Under 'Code and automation' in the left hand menu, click on 'Pages'
- Make sure the 'Source' and 'Branch' fields are set to 'Deploy from branch' and 'Main' respectively.
- Click save. 
- If the page does not automatically refresh, manually refresh it and at the top there should be a box that states 'Your site is live at' followed by the URL. 

The live link can be found here: https://evitaknits.github.io/nigel-is-25/

## CREDITS

### Content

**Homepage Text Wording**
To write this, I was assisted by Chat GPT with the prompt: "Pretend you are inviting your friends to your birthday party. You are called Nigel, you are a man turning 25 years old. It should be a paragraph long". I tweaked the text it gave me slightly. 

**Details Page Text Wording**
I used Chat GPT again for this wording. This time I wrote a paragraph of content that included the information I wanted on the page: 

'Here is all the information you'll need to turn up in the right place at the right time! The axe throwing activity is optional so you can just turn up to the bar part if you like, or even join us for the activity but duck out after. It'd be lovely to see you at either or both! Make sure you tell me which its you'll be attending via the RSVP form. Cheers all.'

I then gave Chat GPT the content it wrote from the homepage along with my content and asked it to write my paragraph in the same voice as the homepage content. 

**Colours**
I used this page to finesse my chosen colour scheme: https://color.adobe.com/create/color-wheel
I used this page to get the lighter shades of my base colour #71B2B5, that I used in the different states of my submit button on my RSVP form: https://mdigi.tools/lighten-color/#71b2b5 

### Media

**Favicon**
I got my icon from here: https://www.flaticon.com/free-icon/birthday-cake_1412443
I generated the code to paste in the head of my HTML files here: https://realfavicongenerator.net/

**Nigel Photo on the Homepage**
I got the photo from Pexels: https://www.pexels.com/photo/man-on-gray-shirt-portrait-91227/
It is by Stefan Stefancik.

**All Bar One Photo on the Homepage**
I got the photo from Design My Night, here: https://www.designmynight.com/brighton/bars/the-lanes/all-bar-one-brighton

**Bar Picture on the RSVP Page**
I got the photo from Unsplash: https://unsplash.com/photos/brown-wooden-bottle-rack-with-bottles-X5upu8w0ZTc 
It is by Kawasaki Toshihiro.

**Thank You Picture on the Form Submission Page**
I got the photo from Pexels: https://www.pexels.com/photo/light-sign-typography-lighting-519/ 
It is by Gratisography.

**Footer Icons**
I got the icons to use in my footer contact information from: https://fontawesome.com/ 
I learnt about this source from the Love Running Walkthrough module in the Code Institute coursework.

### Sources of Learning

**Responsive iframe**
I learnt how to make my YouTube video iframe responsive with this source: https://www.w3schools.com/howto/howto_css_responsive_iframes.asp

**Table Styling**
I learnt how to style tables from this page: https://www.w3schools.com/html/html_table_borders.asp

**Text over Image**
I learnt to add a text block over my bar image on the RSVP page with this source: https://www.w3schools.com/howto/howto_css_image_text_blocks.asp

**Form Styling**
I learnt how to style forms in general from this page: https://www.w3schools.com/css/css_form.asp
I learnt how to prevent the text input boxes overflowing the border of the form from this page: https://www.w3schools.com/css/css3_box-sizing.asp 

**Box Shadow**
I learnt how to make a shadow around my submit box from here: https://www.w3schools.com/css/css3_shadows_box.asp