# Design Course for Developers - Platzi

## Overview

This document serves as a comprehensive reference for all the concepts learned in the course. Please note that some content may be in Spanish.

## Steps to Create an Effective Creative Design Process

1. **Preparation** - Investigate and Compile
2. **Incubation** - Experiment and Synthesize
3. **Illumination** - Create and Imagine
4. **Evaluation** - Criticize and Recreate
5. **Implementation** - Build and Work

## Creative Process

- *(Investigation)* Olga needs to make a birthday cake. Before starting, she creates an inventory list and explores a few recipes.
- *(Experimentation/Incubation)* After investigating, Olga realizes that all cake recipes require an oven. She focuses on finding recipes that do not require an oven.
- *(Illumination)* After considering several options, she decides to create a strawberry cheesecake.
- *(Evaluation)* Before starting, she realizes that she doesn't have enough inventory, so she decides to make one with grapes instead.
- *(Implementation)* Once everything is ready, Olga prepares a wonderful birthday cheesecake!

## Technical Requirements

- Client or Product Description
- Objectives and Challenges
- Target Audience
- Distribution or Delivery Approach

> It is crucial that this document is visually appealing for the customer.

For more details, refer to the [brief document](https://github.com/mssroboto/diseno-para-programadores/blob/master/1-brief/Brief..pdf).

## Definition of UX Design

1. **Research** ⇒ Collect information to understand what users primarily need. Leveraging existing applications is beneficial in creating a good UX design.
2. **Analysis** ⇒ Once the information is collected, analyze it to identify crucial points to consider when designing.
3. **Design** ⇒ Create prototypes or sketches to visualize the final result.
4. **User Testing** ⇒ Usually conducted on sketches to make necessary adjustments before transitioning to the actual design and coding.

## Flow chart

1. must include a clear path that the cusotmer will follow, for example

1. Home/start -> Menu/index -> product details -> add item to the cart -> check the product or order -> pay the item -> add delivery details
    1. if correct proceed to payment platform and complete payment - > payment successful -> confirmation -> homepage
    2. if any of the steps are incorrect, indicate the error and ask the customer to deliver a corrected address format/payment method

## importance of UX & UI

### UX

    1. design and interaction.
    2. Prototyping
    3. Information Architechture
    4. Insvestigation and user testing

### UI

    1. Visual design
    2. Colors
    3. Layouts
    4. Typography

## Color Relationship - Latam culture

1. Red
    - passion
        - food
        - sports
        - entertainment
2. Orange
    - Fun
        - Art
        - Food
        - Events
3. Yellow
    - Happiness
        - Food
        - Shopping
        - Socialization
4. Light Green
    - Harmony
        - Environment
        - Food
        - Education
5. Dark Green
    - Security
        - Agriculture
        - Banks
        - Real State
6. Light blue
    - Knowledge/wisdom
        - Children products
        - health
        - Technology
7. Dark blue
    - Confidence
        - Finances
        - Health
        - Insurances
8. Purple
    - Mystery
        - Religion
        - Products
        - Alternatives
9. Pink
    - Love
        - Beauty
        - Style
        - Children products
10. Brown
    - Stability
        - Agriculture
        - Legal
        - Construction
11. Gray
    - Neutral
        - All industries
12. Black
    - Elegance
        - All industries

### Colors

    - Use Hexagecimal or RGB colors
    - Create a consisten color code
    - Avoid Color excess, to avoid confusion and overwhelm the customer
    - Accessible (readable) Color code
    - Define a color pallette

### Typography

    - font number to the minimum
    - Use preferably standard fonts
    - limit text quantity
    - Typography must be legible in different font sizes
    - High values of Line Height
    - High contrast
    - avoid using intermittent animation, and avoid incuding information hidden behind them

## This is a .scss (Sass) example

    $xs: 360px;
    $s: 440px;
    $m: 768px;
    $l: 1280px;
    $xl: 1440px;

    @mixin for-size($size) {
        @if $size == xs {
            @media (max-width: $s) {
            @content;
            }
        } @else if $size == m {
            @media (min-width: $m) {
            @content;
            }
        } @else if $size == l {
            @media (min-width: $l) {
            @content;
            }
        } @else if $size == xl {
            @media (min-width: $xl) {
                @content;
            }
        }
    }

    :root {
        --columns: 4;
        --column-gap: 6.67%;

        @include for-size(m) {
            --columns: 12;
            --column-gap: 2.27%;
        }

        @include for-size(l) {
            --columns: 12;
            --column-gap: 2.19%;
        }
    }

        .grid {
        margin: 0 16px;

        @include for-size(m) {
            margin: 0 32px;
        }

        @include for-size(l) {
            margin: 0 80px;
        }

        @include for-size(xl) {
            margin: 0 auto;
            max-width: 1280px;
        }
    }

    .grid,
    .subgrid {
        display: grid;
        grid-column-gap: var(--column-gap);
        grid-template-columns: repeat(var(--columns), minmax(0, 1fr));
        position: relative;
    }

## MOVING GRAPHICS FOR THE WEB

## Formats for Moving Graphics

- **Animated CSS:** Suitable for simple animations and transitions.

- **Animated SVG:** Suitable for vector element animations.

- **JS (Canvas, WebGL):** Suitable for complex animations like data animations or 3D. There are JS libraries that can be used for this type of animation.

- **Videos:** Suitable for filming or high-complexity short animations. Always ask yourself: Do I really need this video? Because they are heavy and slow down the site's loading.

## How to Choose Moving Graphics?

- Choose animations that contribute to the content. Avoid overloading with too many animations.

- Ensure that they do not play automatically, and if they do, ensure they have no sound.

- Avoid animations with flashes. Continuous flashes are annoying and can be harmful.

- If your animations provide content, add subtitles or transcriptions so that screen readers can read them.

- Prevent animations from blocking basic content reading. An animation during reading is annoying, and screen readers won't be able to access that content.

- Remember that animations and videos slow down page loading. Less is more, once again.
