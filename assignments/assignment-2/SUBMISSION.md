# CSC 317 Assignment 2 Submission

**Name:** Kevin Chang
**Student ID:** 922123914  
**GitHub Username:** kchang13  
**Assignment Number:** 2  


##  HTML Personal Portfolio Website Assignment

### Description:
A personal porfolio website demonstrating HTML basics.



## Approach / What I Did:
I went with a simple look as I am new to HTML and struggled with keeping my code organized.



## Code Explanation:
5 list anchors are created below along with their href tags, which will take you to their respective sections.

```html
<div>
    <div class="table">
        <nav>
            <ul id="nav-menu">
                <li><a href="#biography">BIOGRAPHY</a></li>
                <li><a href="#education">EDUCATION</a></li>
                <li><a href="#experience">EXPERIENCE</a></li>
                <li><a href="#projects">PROJECTS</a></li>
                <li><a href="#contact">CONTACT</a></li>
            </ul>
        </nav>
    </div>
</div>

I made the list horizontal and styled them as buttons near the top of the page. They dilate when hovered over and contract when disengaged.

        ul#nav-menu
        {
            margin: 0;
            padding: 25px 0 0 0;
            list-style: none;
        }
        /* Makes the list horizontal with 10px between each item */
        ul#nav-menu li
        {
            display: inline-block;
            margin: 10px;
        }
        ul#nav-menu li a
        {
            color: white;
            display: inline-block;
            transition: transform 0.2s ease-in-out;
            text-decoration: none; /* Removes the underline */
        }
        /* When hovering over the anchor, dilate it by 10% */
        ul#nav-menu li a:hover
        {
            transform: scale(1.1);
        }

Two tables are created below with 2 and 3 columns, respectively.

        <table>
            <tr>
                <th>CLASS</th>
                <th>STATUS</th>
            </tr>
            <tr>
                <td>CSC 210</td>
                <td>Complete</td>
            </tr>
            <tr>
                <td>CSC 220</td>
                <td>In progress</td>
            </tr>
            <tr>
                <td>CSC 300</td>
                <td>In progress</td>
            </tr>
            <tr>
                <td>CSC 317</td>
                <td>In progress</td>
            </tr>
        </table>

        ...

        <table>
            <tr>
                <th>POSITION</th>
                <th>COMPANY</th>
                <th>DATE</th>
            </tr>
            <tr>
                <td>T2 Customer Service</td>
                <td>SK Hosting</td>
                <td>2019-2020</td>
            </tr>
            <tr>
                <td>Specialty Sales</td>
                <td>Target</td>
                <td>2021-2022</td>
            </tr>
            <tr>
                <td>Sales Representative</td>
                <td>Pacific Bridge</td>
                <td>2020-present</td>
            </tr>
        </table>


Both tables are centered and use a width of 25% (along with iframes) for uniformity.

        table
        {
            margin: 0 auto;
            width: 25%;
            border-collapse: collapse; /* Consolidates cell borders */
        }

A submission form is created below, with fields for your name, email, subject and message. The email field must receive an input matching the standard email format (example@mail.com), as indicated by  type="email". The subject and message fields have character requirements. All fields must be filled to submit the form.

I used 2 divs because I could not align the form to the center of the page without distorting its contents.

        <div class="form-wrapper"> <!-- Contact form-->
            <div class="container">
                <form>
                    <!-- Name field (required)-->
                    <label for="name">Name</label>
                    <input type="text" id="name" name="name" placeholder="Enter your name..." required>

                    <!-- Email field (required; must be correct format) -->
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" placeholder="Enter your email..." required>

                    <!-- Subject field (required; 2-100 characters) -->
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" name="subject" placeholder="Enter a subject..." required minlength="2" maxlength="100">

                    <!-- Message box (required; 20-1,000 characters) -->
                    <label for="message">Message</label>
                    <textarea id="message" name="message" placeholder="Enter your message here..." style="height:250px" required minlength="20" maxlength="1000"></textarea>

                    <!-- Submit button -->
                    <input type="submit" value="Submit">
                </form>
            </div>
        </div>