

# Gotto Job
**Gotto Online Job Portal  is a responsive job listing website designed to help users find job opportunities and employers to list job vacancies. This project was built using HTML, CSS, and little JavaScript.**

# Contributors
- **Nasro Muuse** - Developed the Home Page and Contact Page.
- **Masud Mohamed**- Developed the About Page.
 - **Abdimudalib Abdullahi** - Developed the Job Listings and Job Details Pages.

# Technologies Used
 - **HTML** - For structuring the content of the pages.
- **CSS** - For styling the website to match the design.
- **JavaScript** - Used for Responsive navavigation links and Testimonials.
## JavaScript Usage

JavaScript was used in only the following parts of the project:

- **Responsive Navigation Links**: Ensured the navigation links are responsive and function smoothly, especially on smartphones.
```javascript
    const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector(".nav-links");
        const icons = document.querySelectorAll("i");

        hamburger.addEventListener("click", function (event) {
            const isVisible = navLinks.getAttribute('data-visible');
            if (isVisible == "true") {
                navLinks.setAttribute('data-visible', "false");
                icons[0].setAttribute('data-visible', "true");
                icons[1].setAttribute('data-visible', "false");
            } else if (isVisible == "false") {
                navLinks.setAttribute('data-visible', "true");
                icons[0].setAttribute('data-visible', "false");
                icons[1].setAttribute('data-visible', "true");

            }
        });

```



- **Testimonials**: Added dynamic behavior to the testimonials section, such as sliding or fading effects.
```javascript 
    const testimonials = document.querySelectorAll('.testimonial');
        const dots = document.querySelectorAll('.dot');

        let currentIndex = 0;

        function showTestimonials(index) {
            testimonials.forEach((testimonial, i) => {
                testimonial.style.display = 'none';
            });
            for (let i = 0; i < 2; i++) {
                testimonials[(index + i) % testimonials.length].style.display = 'flex';
            }
            dots.forEach(dot => dot.classList.remove('active'));
            dots[Math.floor(index / 2) % dots.length].classList.add('active');
        }

        dots.forEach((dot, index) => {
            dot.addEventListener('click', () => {
                showTestimonials(index * 2);
                currentIndex = index * 2;
            });
        });

        setInterval(() => {
            currentIndex = (currentIndex + 2) % testimonials.length;
            showTestimonials(currentIndex);
        }, 5000);

        showTestimonials(currentIndex);
````




 
 # Pages

 ## 1. Home Page (index.html)
- **Description:** As the primary entry point to our job portal, the home page is crafted to captivate and inform visitors about our services. With a modern, responsive design, it ensures an engaging user experience from the get-go.
- **Content:**
   -**Hero Section:** Featuring a dynamic hero image with a powerful tagline and a call-to-action button that directs users to explore job listings.
I   - **Introduction:** A concise overview of our platform  benefits for job seekers and employers.
   - **Featured Jobs:** A spotlight on select job opportunities to immediately attract interest.
   - **Testimonials:** Real success stories from users who have found employment through our platform.
   - **Quick Links:** Easy navigation to key sections like job listings, about us, and contact.

## 2.About Page (about.html)
- **Description:** This page details our mission, vision, and the dedicated team behind the platform. It’s designed to build trust and provide transparency about our operations and goals.
 - **Content:**
Mission Statement: A clear and inspiring explanation of what drives us.
   - **Team Members**: Profiles and photos of our team, showcasing their roles and expertise.
  - **Journey:** A narrative of our platform’s development and milestones.
  - **Achievements:** Awards, recognitions, and significant accomplishments we’ve attained.
 - **Contact Info:** Multiple ways to get in touch with us or follow our social media channels.

## 3. Job Listings Page (job-listings.html)
- **Description:** This page is the hub for all available job opportunities. It’s designed for easy navigation and filtering to help users find the perfect job match.
- **Content:**
  - **Search Bar:** An intuitive search function to find jobs by keyword.
   - **Filters:** Options to filter jobs by location, industry, job type, and more.
  - **Job Listings:** A comprehensive list of job postings with brief descriptions, company names, and apply buttons.
  - **Pagination:** Smooth navigation through multiple pages of job listings to enhance user experience.

## 4. Job Details Page (job-details.html)
- **Description:** This page provides in-depth information about specific job postings, ensuring potential applicants have all the details they need to make an informed decision.
- **Content:**
  - **Job Title and Company:** Prominently displayed at the top for immediate recognition.
  - **Job Description:** Detailed overview of the role, responsibilities, and expectations.
  - **Requirements:** Clearly listed qualifications and skills needed for the job.
  - **Application Instructions:** Step-by-step guide on how to apply, including necessary documents or links.
  - **Company Information:** Background details about the hiring company with a link to their website.

## 5. Contact Page (contact.html)
- **Description:** Our contact page is designed to make it easy for users to reach out to us. It includes various contact methods to suit different preferences.
- **Content:**
  - **Contact Form:** User-friendly form fields for name, email, subject, and message.
 - **Contact Details:** Direct email addresses, phone numbers, and possibly a physical address.
 - **Map:** An embedded Google Map showing our office location for in-person visits.
 - **Social Media Links:** Icons and links to our social media profiles to foster further engagement.




# Features
The main features of the `Gotto Job` website template focusing on responsive design, flexbox, and grid layout:

 ## 1. Responsive Design
We ensured the website design is responsive across various devices by implementing CSS media queries with a **max-width: 768px** breakpoint. This strategy allows our layout to adapt seamlessly to different screen sizes, enhancing user experience on smartphones and smaller tablets.

- **Media Queries:** Utilizing @media (max-width: 768px), we tailored styles specifically for screens up to 768 pixels wide.

- **Adaptive Design:** Within these media queries, elements are intelligently restructured. For example, our navigation menu switches to a collapsible icon for easier access on mobile devices, and content reflows into single-column layouts for improved readability.

- **User-Centric Approach:** By prioritizing max-width: 768px, we ensure that users can comfortably navigate and engage with our website regardless of the device they are using.

## 2. Flexbox
We employed CSS Flexbox extensively throughout the website to create flexible and responsive layouts. This powerful layout model allowed us to efficiently organize and align elements within our design, ensuring a consistent and visually appealing user experience across different screen sizes.
#### **Key Benefits of Flexbox:**
- **Flexible Alignment:** Flexbox enabled us to easily align elements horizontally and vertically, adjusting spacing and distribution as needed.
- **Responsive Design:** By utilizing Flexbox properties like justify-content and align-items, we ensured that content adapts fluidly to varying viewport sizes.
- **Simplified Structure:** Flexbox intuitive structure reduced the need for complex CSS hacks, making our layout code cleaner and more maintainable.
- **Example:** For instance, Flexbox was instrumental in creating our navigation bar, where items are evenly spaced and aligned neatly even as the screen size changes.

## 3. Grid Layout
We implemented CSS Grid  our website to create structured and versatile layouts. CSS Grid provided us with a robust framework for organizing content into defined grids, offering precise control over the placement and alignment of elements.

### **Key Benefits of Grid Layout:**

- **Grid Structure:** CSS Grid allowed us to divide our layout into rows and columns, providing a systematic approach to arranging content.

- **Example:** For example, our home page's hero section utilized CSS Grid to create a responsive and visually appealing form, ensuring a seamless user experience across different devices.



# Installation

To run the project locally, follow these steps:

1.  Clone the repository:
    ```git
    git clone https://github.com/dugsiiyeinc/Gotto-Job.git

    ```

2. Navigate to the project directory:

```git
    cd Gotto-job
```

3. Open `index.html` in your web browser.
