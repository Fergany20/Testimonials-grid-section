# Frontend Mentor - Testimonials Grid Section Solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-N16631Sm_). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## 🔗 Links

- **Live Site URL:** [https://fergany20.github.io/Testimonials-grid-section/]
- **Solution URL:** [https://www.frontendmentor.io/profile/Fergany20]

---

## 🚀 The Challenge

The challenge was to build out this testimonials grid section and get it looking as close to the design as possible. Users should be able to:

- View the optimal layout for the site depending on their device's screen size.
- See hover states for all interactive elements.

---

## 🛠️ My Process

### Built With

✨ Modern Frontend Stack:

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)

- Semantic HTML5 markup
- Mobile-first workflow
- **CSS Grid** for the layout core
- **Sass (SCSS)** Architecture (BEM Methodology)
- Fluid Typography using CSS `clamp()`

---

## 💡 Key Implementations & What I Learned

In this project, I focused heavily on writing scalable and robust SCSS. Here are some of the key highlights from my code:

### 1. Robust Fluid Unit Conversion (PX to REM/EM)
Instead of hardcoding values, I built dynamic functions to ensure accessible text sizing that adapts perfectly to user browser settings:

```scss
@function rem($pixels) {
    @if type-of($pixels) == "number" {
        @return ($pixels / 16) * 1rem;
    } @else {
        @error "Please provide a number for the pixels.";
    }
}
2. Semantic & Accessible HTML

Leveraged the power of aria-labelledby to guarantee that screen readers can fully comprehend and contextually map each testimonial card to its corresponding user:
HTML

<article class="testimonial-card testimonial-card--purple" aria-labelledby="card-daniel">
  <h2 id="card-daniel" class="testimonial-card__name">Daniel Clifford</h2>
</article>

3. Dynamic Map-Driven Media Queries

Created a responsive mixin that safely extracts breakpoints from a Sass Map using modern configuration rules:
SCSS

@mixin breakpoints($size) {
    @if map-has-key($breakpoints-up, $size) {
        @media (min-width: map-get($breakpoints-up, $size)) {
            @content;
        }
    }
}

👤 Author

    GitHub - @Fergany20

    Frontend Mentor - @Fergany20