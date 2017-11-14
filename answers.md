<h1>PART 1</h1>
<p>
1.) Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
</p>

const profileImg = document.querySelector('.profile-image')


profileImg.src = "images/self-portrait-officebg.jpg"
"images/self-portrait-officebg.jpg"


1-b.) Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

const skyImg = document.querySelector('.photography')

skyImg.src = "https://picsum.photos/325/225/?random"
"https://picsum.photos/325/225/?random"

2.) Select the heading that says "Panda the Bear" and change it to your own name.

const heading = document.querySelector('h1.highlight')

heading.innerHTML = "Papa Sanch"



3.)Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

const employment = document.querySelector('#employment h3.info-title')

employment.innerHTML = "Jobs"

4.)Change the colour of the body.
const body = document.querySelector('body');

body.style.backgroundColor = "grey";




5.)Change the colour of each element using the highlight class. Use a for loop to do this.


let highlights = document.querySelectorAll('.highlight');
undefined
highlights

for (let highlight of highlights) {
    highlight.style.color = "red";
};



6.) Change the font family of the h1 to 'monospace'.

const h1 = document.querySelectorAll('h1');

for (let x of h1) {  
    x.style.fontFamily = "monospace"
};


7.) Find a way to select the round icons in the sidebar and then change their colour.

const circleIcon = document.querySelectorAll('.action-icon-bg');

for (let circle of circleIcon) {
    circle.style.backgroundColor = "blue";
};




8.) Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

const nameField = document.querySelector('#name');

nameField.placeholder = 'Identify Yo-Self Sucka!';



9.) Change the placeholder attribute of the message field to "state your business".

const messageField = document.querySelector('#message');

messageField.placeholder = "State Yo Biznazz!";



10.) Give the name field a "value" attribute of "your nemesis".

nameField.value = "your nemesis"
"your nemesis"


11.) Change the value attribute of the email field to "koalathebear@gmail.com".

const emailField = document.querySelector('#email');

emailField.value = "koalathebear@gmail.com";

12.) Change the value of the submit button on the contact form to "En garde!".

const submitButton = document.querySelector('#submit');

submitButton.value = "En garde!";


13.) We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

submitButton.disabled = true;


14.) We should help Panda protect their privacy by erasing their personal details from the sidebar.

const removeBio = document.querySelector('ul.bio-info');

removeBio.innerText = ""
