# Activity 8 - Next Portfolio Website

**Deadline for Completion:** Friday, 22nd December 2023

## Overview
In this project, you will transform a portfolio website developed using HTML and CSS in Activity 3 into a server-rendered Next.js website. The focus is on applying the concepts of component-based architecture using the latest Next.js features, including the App Router for efficient routing and organization. The project will enrich your understanding of Next.js, React components, TypeScript, and CSS modules by breaking down the portfolio website into distinct components and styling them.

**ProTip**: You can refine and utilize existing codebase from Activity 3.

## Objectives
- Convert existing HTML/CSS website into a Next.js website.
- Implement the App Router directory structure.
- Create and use TypeScript components.
- Apply styling using CSS modules.

## Tasks and Mark Allocation
1. **Project Setup and Configuration (20%)**
   - Initialize a Next.js project with TypeScript.
   - Set up the required npm scripts and install dependencies.

2. **Component Creation (40%)**
   - Break down the UI into five main components: Header, About, Skills, Contact, and Footer.
   - Ensure each component is correctly typed with TypeScript.
   - Implement proper exporting and importing of components.

3. **Styling with CSS Modules (20%)**
   - Create and link CSS modules for each component.
   - Ensure styles closely match the provided design.

4. **App Router Implementation (10%)**
   - Use the App Router to set up routing for the portfolio website.
   - Correctly place components within the `app/` directory structure.

5. **Code Quality and Best Practice (10%)**
   - Write clear, maintainable code with proper comments.
   - Ensure the website is free from console errors and warnings.

## Implementation Details

Creating a portfolio website in Next.js involves breaking down the UI into reusable components. You will convert the following portfolio design into a Next.js website by creating five main components and styling them with CSS:

![Portfolio Design](/portfolio.png)

### Development Environment Setup
Set up Next.js for your portfolio website development by following the guidelines in the `Configuring the Development Environment` section of the week 8 lecture notes.

### Breakdown of Components
1. Header Component
2. About Component
3. Skills Component
4. Contact Component
5. Footer Component

### Header Component
The Header represents the top section of the portfolio, including the background image, display picture, name, description, and social links.

- **Steps to Build:**
  1. Create a file named `Header.tsx` in the `components` directory.
  2. Add the boilerplate code for the component.
  3. Import CSS module for styling.
  4. Add remaining codebase.

  **Example Boilerplate:**
  ```tsx
  import styles from './Header.module.css';

  const Header = () => {
      return (
          <header className={styles.header}>
              <h1>Nana Adjoa</h1>
              <p>A Beginner Web Developer at The PAD Forum</p>
              {/* Social links go here */}
          </header>
      );
  };

  export default Header;
  ```

  **CSS Module Example (`Header.module.css`):**
  ```css
  .header {
      background-color: #fff;
      padding: 1rem;
      text-align: center;
  }
  ```

### About Component
The About component contains the about section with a the explainer video, and a brief introduction.

- **Steps to Build:**
  1. Create a file named `About.tsx`.
  2. Write the JSX code to layout the about section.
  3. Import and apply CSS for styling.
  4. Add remaining codebase.

  **Example Boilerplate:**
  ```tsx
  import styles from './About.module.css';

  const About = () => {
      return (
          <section className={styles.about}>
              <h2>About</h2>
              <div>{/* Explainer video goes here */}</div>
              <p>{/* About text goes here */}</p>
          </section>
      );
  };

  export default About;
  ```

  **CSS Module Example (`About.module.css`):**
  ```css
  .about {
      padding: 2rem;
      background-color: #f3f3f3;
  }
  ```

### Skills Component
The Skills component displays a list of skills with corresponding proficiency levels.

- **Steps to Build:**
  1. Create a file named `Skills.tsx`.
  2. Implement the UI for listing skills and their levels.
  3. Style with CSS.
  4. Add remaining codebase.

  **Example Boilerplate:**
  ```tsx
  import styles from './Skills.module.css';

  const Skills = () => {
      return (
          <section className={styles.skills}>
              <h2>Skills</h2>
              {/* Skill contents go here */}
          </section>
      );
  };

  export default Skills;
  ```

  **CSS Module Example (`Skills.module.css`):**
  ```css
  .skills {
      padding: 2rem;
      background-color: #eaeaea;
  }
  ```

### Contact Component
The Contact component contains a contact form for visitors to send messages.

- **Steps to Build:**
  1. Create a file named `Contact.tsx`.
  2. Add the form elements with proper input fields.
  3. Apply CSS to style the form.
  4. Add remaining codebase.

  **Example Boilerplate:**
  ```tsx
  import styles from './Contact.module.css';

  const Contact = () => {
      return (
          <section className={styles.contact}>
              <h2>Contact</h2>
              <form>
                  {/* Form fields go here */}
              </form>
          </section>
      );
  };

  export default Contact;
  ```

  **CSS Module Example (`Contact.module.css`):**
  ```css
  .contact {
      padding: 2rem;
      background-color: #ddd;
  }
  ```

### Footer Component
The Footer component displays the footer with copyright and legal information.

- **Steps to Build:**
  1. Create a file named `Footer.tsx`.
  2. Write JSX for the footer content.
  3. Style using CSS module.
  4. Add remaining codebase.

  **Example Boilerplate:**
  ```tsx
  import styles from './Footer.module.css';

  const Footer = () => {
      return (
          <footer className={styles.footer}>
              ©2023, The PAD Program. All Rights Reserved.
          </footer>
      );
  };

  export default Footer;
  ```

  **CSS Module Example (`Footer.module.css`):**
  ```css
  .footer {
      padding: 1rem;
      background-color: #222;
      color: #fff;
      text-align: center;
  }
  ```

Once all components are created and styled with the example boilerplate code, you can import them into your `page.tsx` file to assemble the complete page and continue with development work:

```tsx
import Header from './components/Header';
import About from './components/About';
import Skills from './components/Skills';
import Contact from './components/Contact';
import Footer from './components/Footer';

const Home = () => {
  return (
    <>
      <Header />
      <About />
      <Skills />
      <Contact />
      <Footer />
    </>
  );
}

export default Home;
```

This modular approach in Next.js not only organizes your code better but also leverages the power of server-side rendering and optimization inherent in the framework.

## Folder Structure for the project

Your project should replicate/mirror the following directory organization:

```sh
activity8-your-github-repo/
│
├── .next/                             # Next.js build output (not tracked by git)
│
├── app/                               # Main directory for the App Router
│   ├── components/                    # Reusable components directory
│   │   ├── Header.tsx                 # Header component
│   │   ├── About.tsx                  # About section component
│   │   ├── Skills.tsx                 # Skills section component
│   │   ├── Contact.tsx                # Contact section component
│   │   └── Footer.tsx                 # Footer component
│   │
│   ├── styles/                        # Directory for CSS modules
│   │   ├── Header.module.css          # Styles for the Header component
│   │   ├── About.module.css           # Styles for the About component
│   │   ├── Skills.module.css          # Styles for the Skills component
│   │   ├── Contact.module.css         # Styles for the Contact component
│   │   └── Footer.module.css          # Styles for the Footer component
│   │
│   └── page.tsx                       # Entry point for the home page
│
├── node_modules/                      # Node.js modules (not tracked by git)
│
├── public/                            # Public folder for static files like images
│
├── package.json                       # Project metadata and dependencies
├── tsconfig.json                      # TypeScript configuration
├── README.md                          # Project README file
├── other files                        # Other files created by Next
├── other files                        # Other files created by Next
└── other file                         # Other files created by Next
```
