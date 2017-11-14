<h1>PART 1</h1>
<p>
1.) Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
</p>

```
const profileImg = document.querySelector('.profile-image')


profileImg.src = "images/self-portrait-officebg.jpg"
"images/self-portrait-officebg.jpg"
```

1-b.) Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.
```
const skyImg = document.querySelector('.photography')

skyImg.src = "https://picsum.photos/325/225/?random"
"https://picsum.photos/325/225/?random"
```


2.) Select the heading that says "Panda the Bear" and change it to your own name.


```
const heading = document.querySelector('h1.highlight')

heading.innerHTML = "Papa Sanch"
```


3.)Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

```
const employment = document.querySelector('#employment h3.info-title')

employment.innerHTML = "Jobs"
```

4.)Change the colour of the body.
const body = document.querySelector('body');
```
body.style.backgroundColor = "grey";
```



5.)Change the colour of each element using the highlight class. Use a for loop to do this.

```
let highlights = document.querySelectorAll('.highlight');
undefined
highlights

for (let highlight of highlights) {
    highlight.style.color = "red";
};
```


6.) Change the font family of the h1 to 'monospace'.
```
const h1 = document.querySelectorAll('h1');

for (let x of h1) {  
    x.style.fontFamily = "monospace"
};
```

7.) Find a way to select the round icons in the sidebar and then change their colour.
```
const circleIcon = document.querySelectorAll('.action-icon-bg');

for (let circle of circleIcon) {
    circle.style.backgroundColor = "blue";
};
```



8.) Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".
```
const nameField = document.querySelector('#name');

nameField.placeholder = 'Identify Yo-Self Sucka!';
```


9.) Change the placeholder attribute of the message field to "state your business".
```
const messageField = document.querySelector('#message');

messageField.placeholder = "State Yo Biznazz!";
```


10.) Give the name field a "value" attribute of "your nemesis".
```
nameField.value = "your nemesis"
"your nemesis"
```

11.) Change the value attribute of the email field to "koalathebear@gmail.com".
```
const emailField = document.querySelector('#email');

emailField.value = "koalathebear@gmail.com";
```
12.) Change the value of the submit button on the contact form to "En garde!".
```
const submitButton = document.querySelector('#submit');

submitButton.value = "En garde!";
```

13.) We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).
```
submitButton.disabled = true;
```

14.) We should help Panda protect their privacy by erasing their personal details from the sidebar.
```
const removeBio = document.querySelector('ul.bio-info');

removeBio.innerText = ""
```

<h1>Part 2</h1>

<h4>Removing Elements from the DOM</h4>

1. Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)

```
const timeTravel = $('#time-travel').parent('.bar-default');

timeTravel.remove();
```


<h4>Adding Elements to the DOM</h4>

1. that drawing of Pikachu is really cute. Let’s duplicate it using cloneNode()

select item to clone & save to variable
```
const pikachu = document.querySelector("#right-image img");

const pikachuClone = pikachu.cloneNode();
```

insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().
```
const portfolioContainer = document.querySelector(".portfolio-container")

portfolioContainer.appendChild(pikachuClone);
```


2. Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.
```
for (let i=0; i < 10; i++) {
  portfolioContainer.appendChild(pikachu.cloneNode());
};
```

3. Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

```
const listItem = document.createElement('li');
```

It isn't part of the DOM yet, it's just floating in the void. We'll eventually attach it to the ```<ul>``` in the sidebar, below Panda's name, location, and phone number.

Now we need a new ```<span>``` tag to go inside the ```<li>``` we just made. This span will eventually go in the left column below 'Phone'.

```
const leftSpan = document.createElement('span');
````

Next we need to make a "text node" in order to put text inside our new span. A text node is a chunk of plain text that lives inside some HTML tag in the DOM.
```
cosnt lastUpdated = document.createTextNode('Page last updated  on');
```

We're ready to put that new text node inside our new ``<span>`` using `appendChild`.

```
leftSpan.appendChild(lastUpdated);
```

And we'll put the <span> inside the <li>, again using appendChild.

```
listItem.appendChild(leftSpan);
```


At this point our new elements are attached to each other but are still floating in the void separate from our webpage's DOM.

It's up to you to go through the same process for the second span that will go in the right-hand column of the <ul> (below Panda's phone number). Look up the docs for the Date class to find a way of displaying the current date inside your next text node.

```
const rightSpan = document.createElement('span');

const dateUpdated = document.createTextNode(Date());

rightSpan.appendChild(dateUpdated);

listItem.appendChild(rightSpan);

```




After that, find a way of selecting the <ul> and append the new <li> to it. For bonus marks, apply the correct classes to these new elements of yours so the styling is consistent with the rest of the list items.

```
const bioInfoList = document.querySelector('.bio-info');
bioInfoList.appendChild(listItem);
```

Bonus - adding Classes to elements

```
rightSpan.className = "bio-info-value bio-info-updatedAt"
leftSpan.className = "bio-info-value bio-info-title"
listItem.className = "bio-info-item"
```
