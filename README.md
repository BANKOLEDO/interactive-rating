
---

# Frontend Mentor - Interactive Rating Component Solution

This is my solution to the [Interactive Rating Component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/interactive-rating-component-koxpeBUmI).
It’s a simple but engaging component that lets users pick a rating, submit it, and view a nice thank-you state.

## Table of Contents

* [Overview](#overview)

  * [The challenge](#the-challenge)
  * [Links](#links)
* [My process](#my-process)

  * [Built with](#built-with)
  * [What I learned](#what-i-learned)
  * [Continued development](#continued-development)
  * [Useful resources](#useful-resources)
* [Author](#author)

---

## Overview

### The Challenge

Users should be able to:

* View a responsive layout across devices
* See hover states for all interactive elements
* Select and submit a number rating
* View a “Thank you” card after submitting
* Navigate back to update their rating

### Links

* **Solution URL:** *Add when uploaded to Frontend Mentor*
* **Live Site URL:** []()

---

## My Process

### Built With

* Semantic HTML5
* CSS (Flexbox, transitions, custom properties)
* Mobile-first workflow
* Vanilla JavaScript (DOM manipulation, event handling)

### What I Learned

This project helped me practice:

* **Managing active states** using class toggles
* Handling user input and updating UI dynamically
* Switching between two component states (`rating` → `thank you`)
* Clean DOM querying and reset logic for going back

**Example logic from the project:**

```js
ratings.forEach(rating => {
  rating.addEventListener('click', () => {
    ratings.forEach(r => r.classList.remove('active'));
    rating.classList.add('active');
    selectedValue = rating.textContent;
  });
});
```

```js
submitBtn.addEventListener('click', () => {
  if (selectedValue) {
    selectedRating.textContent = selectedValue;
    ratingCard.style.display = 'none';
    thankYouCard.style.display = 'flex';
  }
});
```

### Continued Development

Going forward, I want to explore:

* Smoother animations between states
* Cleaner component architecture (possibly port this to React)
* More reusable styling patterns using utility classes or CSS variables

### Useful Resources

* MDN Web Docs – Event listeners and DOM manipulation
* Frontend Mentor community solutions (for styling inspiration)

---

## Author

* Website — [https://devolabanks.vercel.app](https://devolabanks.vercel.app)
* Frontend Mentor — [https://www.frontendmentor.io/profile/olabanks](https://www.frontendmentor.io/profile/BANKOLEDO)
* Twitter — [https://twitter.com/olabanks](https://twitter.com/olabanks)__
