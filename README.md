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

SCREENSHOT OF WIREFRAME HERE

### Colour Palette

Having completed my rough wireframe, I took some time to pick a colour scheme. I was aiming for a vivid, stylish and energising palette. Here is what I chose:

![Colour palette](assets/images/colourpalette.png)

## FEATURES

For each item here you need the feature title, a screenshot of the feature and a short paragraph of the value it gives the user. 

### Existing Features

#### Navigation Bar

#### Footer 

#### RSVP Form

Includes a thank you page 

#### Maps

#### 404 Page

### Features Left To Implement

#### Party Playlist Compiler

#### Gift Wishlist

## TESTING

REFACTORING BUT DO I NEED SEPARATE CSS FILES?

I completed the following types of testing throughout development and at the end of my project:

- **Manual feature testing:** I clicked through the whole site ensuring I met all user needs and that everything appeared as expected. 
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

1. The navigation bar does not have the semantic tag `<button>` to help screen readers.

2. The title above the YouTube video is not aligned with the left edge of the video, whereas the title above the image next to the YouTube video is. 

#### Screen Size Responsiveness

1. I found that when scaling the screen using the responsive setting in Chrome Devtools, a certain size between tablet and computer screens made the table on my 'The Details' page go off the edge. I found that removing the 'width: 100vh' property from the `<section>` that this table was in solved this. 

2. The super-wide screen made the All Bar One image on the homepage look small compared to the YouTube Video. I found that this was because the size of the image was too small, so I replaced it with a bigger image and this solved that issue. 

#### Accessibility Testing 
1. I originally had #372C57 colour text on a background of #E3705F got my navigation bar but this was flagged: 'Background and foreground colors do not have a sufficient contrast ratio.' So I changed this to black text.

##### BEFORE:

##### AFTER:


2. My iframes did not have titles. I added these.


3. My social media icons did not have names. I added these. 


4. I had used a h3 element to emphasise something on a page which was not in the sequentially-descending. 

5. Although lighthouse did not flag this to me, I saw that I had not added any aria-labels for images and links, so I added these too. 

### Unresolved Bugs


## DEPLOYMENT

This section should describe the process you went through to deploy the project to a hosting platform (e.g. GitHub)

The site was deployed to GitHub pages. The steps to deploy are as follows:
- In the GitHub repository, navigate to the Settings tab
- From the source section drop-down menu, select the Master Branch
- Once the master branch has been selected, the page will be automatically refreshed with a detailed ribbon display to indicate the successful deployment.

The live link can be found here: https://evitaknits.github.io/nigel-is-25/

## CREDITS

### Content


### Media


### Sources of Learning

Check I have enough references for all the things I did and enough commented explanations within the code too

For each credit, you need a title/description, a source or a link and the context (how it was used and what lessons we learnt from it)

- Favicon generator: https://realfavicongenerator.net/
- Favicon icon source: https://www.flaticon.com/free-icon/birthday-cake_1412443
- Nigel smiling on homepage: Photo by Stefan Stefancik: https://www.pexels.com/photo/man-on-gray-shirt-portrait-91227/
- Wording of homepage main content assisted by Chat GPT with the prompt: "Pretend you are inviting your friends to your birthday party. You are called Nigel, you are a man turning 25 years old. It should be a paragraph long"
- Font Awesome used for icons: https://fontawesome.com/
- W3 schools for making a responsive iframe for my youtube video: https://www.w3schools.com/howto/howto_css_responsive_iframes.asp
- All Bar One photo from: https://www.designmynight.com/brighton/bars/the-lanes/all-bar-one-brighton
- How to style tables: https://www.w3schools.com/html/html_table_borders.asp
- Wording of details main content assisted by Chat GPT, asking it to write my paragraph in the same voice as the homepage. My content before: Here is all the information you'll need to turn up in the right place at the right time! The axe throwing activity is optional so you can just turn up to the bar part if you like, or even join us for the activity but duck out after. It'd be lovely to see you at either or both! Make sure you tell me which its you'll be attending via the RSVP form. Cheers all.
- Where I learnt to add a text block over my bar image on the RSVP page: https://www.w3schools.com/howto/howto_css_image_text_blocks.asp
- Bar photo used on RSVP page: Photo by Kawasaki Toshihiro: https://unsplash.com/photos/brown-wooden-bottle-rack-with-bottles-X5upu8w0ZTc
- How to style forms: https://www.w3schools.com/css/css_form.asp
- How to make a shadow around my submit box: https://www.w3schools.com/css/css3_shadows_box.asp
- Thank you image: Photo by Gratisography: https://www.pexels.com/photo/light-sign-typography-lighting-519/ 
- How to prevent the text boxes from overflowing the form border: https://www.w3schools.com/css/css3_box-sizing.asp 