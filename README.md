# Frontend Mentor - FAQ accordion card solution

This is a solution to the [FAQ accordion card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-card-XlyjD0Oam). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See hover states for all interactive elements on the page
- Hide/Show the answer to a question when the question is clicked

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [https://github.com/nathanieladiah/faq-accordion](https://github.com/nathanieladiah/faq-accordion)
- Live Site URL: [https://nathanieladiah.github.io/faq-accordion/](https://nathanieladiah.github.io/faq-accordion/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow


### What I learned

Styling the native `<details>` and `<summary>` tags for this accordion:

```scss
details {

	border-bottom: 1px solid $lightGrayishBlue;

	summary {

		padding: 1rem 0;
		position: relative;
		cursor: pointer;
		font-size: 0.875rem;
		letter-spacing: -.31px;
		font-weight: 400;
		list-style: none;
		margin-right: 2rem;
		outline: 0;

		@include breakpoint-up(medium) {
			letter-spacing: 0;
		}

		&:hover {
			color: $softRed;
		}

		&::-webkit-details-marker{
			display: none;
		}

		&::after {
			content: url(../images/icon-arrow-down.svg);
			position: absolute;
			line-height: 0;
			right: -2rem;
			top: 1.5rem;
			transform-origin: center;
			transition: 200ms linear;
		}

	}

	&[open] {

		summary {

			~ * {
				animation: open 0.3s ease-in-out;
			}

			font-weight: 700;
			padding-bottom: 0;

			&::after {
				transform: rotate(180deg);
				font-size: 2rem;
			}
		}
	}

	p {
		font-size: 0.75rem;
		margin-top: 0.6875rem;
		margin-bottom: 1rem;
		max-width: 16rem;
	}

}

```

## Author

- Website - [Nathaniel Adiah](https://nathanieladiah.github.io)
- Frontend Mentor - [@nathanieladiah](https://www.frontendmentor.io/profile/nathanieladiah)
