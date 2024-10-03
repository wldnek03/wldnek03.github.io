---
# Use the Intro widget of the Blog template
widget: about.avatar

# This file represents a page section.
headless: true

# Order that this section will appear in.
weight: 10

author: admin

#design:
#  background:
#    color: '#090a0b'
#    text_color_light: true
#    video:
#      path:  # enter filename of a video in /assets/media
#  css_class: fullscreen
---

<form>
    <input type="radio" name="fancy" autofocus value="clubs" id="clubs" />
    <input type="radio" name="fancy" value="hearts" id="hearts" />
    <input type="radio" name="fancy" value="spades" id="spades" />
    <input type="radio" name="fancy" value="diamonds" id="diamonds" />      

    <label for="clubs">&#9827; Clubs</label>
    <label for="hearts">&#9829; Hearts</label>
    <label for="spades">&#9824; Spades</label>
    <label for="diamonds">&#9830; Diamonds</label>

    <div class="keys">Use left and right keys to navigate</div>
</form>

<style>
    * {
        box-sizing: border-box;
    }

    body {
        font-family: sans-serif;
        overflow: hidden;
    }

    label {
        background: #444;
        color: #fff;
        transition: transform 400ms ease-out;
        display: inline-block;
        min-height: 100%;
        width: 100vw;
        height: 100vh;
        position: relative;
        z-index: 1;
        text-align: center;
        line-height: 100vh;
        font-size: 3rem;
    }

    form {
        position: absolute;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
        white-space: nowrap;
    }

    input {
        position: absolute;
    }

    .keys {
        position: fixed;
        z-index: 10;
        bottom: 0;
        left: 0;
        right: 0;
        padding: 1rem;
        color: #fff;
        text-align: center;
        transition: all 300ms linear;
        opacity: 0;
    }

    input:focus ~ .keys {
        opacity: 0.8;
    }

    input:nth-of-type(1):checked ~ label:nth-of-type(1), 
    input:nth-of-type(2):checked ~ label:nth-of-type(2),
    input:nth-of-type(3):checked ~ label:nth-of-type(3),
    input:nth-of-type(4):checked ~ label:nth-of-type(4) {
        z-index: 0;
    }

    input:nth-of-type(1):checked ~ label {
        transform: translate3d(0, 0, 0);
    }

    input:nth-of-type(2):checked ~ label {
        transform: translate3d(-100%, 0, 0);
    }

    input:nth-of-type(3):checked ~ label {
        transform: translate3d(-200%, 0, 0);
    }

    input:nth-of-type(4):checked ~ label {
        transform: translate3d(-300%, 0, 0);
    }

    label[for="diamonds"],
    label[for="hearts"] {
        background: #cc0000;
    }

    label:before,
    label:after {
        color: white;
        display: block;
        background: rgba(255, 255, 255, 0.2);
        position: absolute;
        padding: 1rem;
        font-size: 3rem;
        height: 10rem;
        vertical-align: middle;
        line-height: 10rem;
        top: 50%;
        transform: translate3d(0, -50%, 0);
        cursor: pointer;
    }

    label:before {
        content: "\276D"; /* Left arrow */
        right: 100%;
        border-top-left-radius: 50%;
        border-bottom-left-radius: 50%;
    }

    label:after {
        content: "\276C"; /* Right arrow */
        left: 100%;
        border-top-right-radius: 50%;
        border-bottom-right-radius: 50%;
    }
</style>


👋 Hi, I'm **Jiwoo**. I'm doing research regarding communications and networks.
{style="font-size: 1.2rem; background: #FFB76B; background: linear-gradient(to right, #FFB76B 0%, #FFA73D 30%, #FF7C00 60%, #FF7F04 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent;"}


Check out my [resume](about/) and the portfolio below.✔️
